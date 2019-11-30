#### The validation accuracy of the base model at 50th epoch is 0.8238

#### Results of my network beating the base model
- Final Validation accuracy at 50th epoch = **82.93%**
- Max Validation accuracy at 49th epoch = **83.01%**
- Total params in the model = **88,461**

#### **Model definition**

 ##### Define the dep_sep_model - # Output size, Receptive field
dep_sep_model = Sequential()
dep_sep_model.add(SeparableConv2D(32, (3, 3), border_mode='same', input_shape=(32, 32, 3),activation = 'relu')) # 30, 3
dep_sep_model.add(BatchNormalization())
dep_sep_model.add(SeparableConv2D(32, (3, 3),activation = 'relu')) # 28, 5
dep_sep_model.add(MaxPooling2D(pool_size=(2, 2))) # 14, 5
dep_sep_model.add(Dropout(0.25))

dep_sep_model.add(SeparableConv2D(48, 3, 3, border_mode='same',activation = 'relu')) # 12, 7
dep_sep_model.add(BatchNormalization())
dep_sep_model.add(Dropout(0.1))

dep_sep_model.add(SeparableConv2D(64,(1,1),activation = 'relu')) # 10, 9
dep_sep_model.add(BatchNormalization())
dep_sep_model.add(Dropout(0.1))

dep_sep_model.add(SeparableConv2D(96,(3,3), border_mode='same',activation = 'relu'))
dep_sep_model.add(MaxPooling2D(pool_size=(2, 2)))
dep_sep_model.add(Dropout(0.25))

dep_sep_model.add(SeparableConv2D(192,(3,3),activation = 'relu', border_mode='same'))
dep_sep_model.add(BatchNormalization())
dep_sep_model.add(Dropout(0.1))

dep_sep_model.add(SeparableConv2D(128,(1,1),activation = 'relu', border_mode='same'))
dep_sep_model.add(BatchNormalization())
dep_sep_model.add(Dropout(0.1))

dep_sep_model.add(SeparableConv2D(192, (3, 3),activation = 'relu'))
dep_sep_model.add(BatchNormalization())
dep_sep_model.add(Dropout(0.1))

dep_sep_model.add(SeparableConv2D(10,(1,1),activation = 'relu'))
dep_sep_model.add(BatchNormalization())
dep_sep_model.add(GlobalAveragePooling2D())
dep_sep_model.add(Activation('softmax'))

#### Compile the dep_sep_model
dep_sep_model.compile(optimizer='adam', loss='categorical_crossentropy', metrics=['accuracy'])

#### Summary of the model
dep_sep_model.summary()

### Training logs of 50 epochs

Epoch 1/50

Epoch 00001: LearningRateScheduler setting learning rate to 0.003.
390/390 [==============================] - 30s 77ms/step - loss: 1.5221 - acc: 0.4615 - val_loss: 1.9293 - val_acc: 0.4591
Epoch 2/50

Epoch 00002: LearningRateScheduler setting learning rate to 0.0022744503.
390/390 [==============================] - 24s 62ms/step - loss: 1.1112 - acc: 0.6141 - val_loss: 1.2022 - val_acc: 0.5935
Epoch 3/50

Epoch 00003: LearningRateScheduler setting learning rate to 0.0018315018.
390/390 [==============================] - 24s 62ms/step - loss: 0.9617 - acc: 0.6666 - val_loss: 1.0757 - val_acc: 0.6296
Epoch 4/50

Epoch 00004: LearningRateScheduler setting learning rate to 0.0015329586.
390/390 [==============================] - 24s 62ms/step - loss: 0.8646 - acc: 0.7021 - val_loss: 0.9152 - val_acc: 0.6856
Epoch 5/50

Epoch 00005: LearningRateScheduler setting learning rate to 0.0013181019.
390/390 [==============================] - 24s 62ms/step - loss: 0.8015 - acc: 0.7245 - val_loss: 0.8113 - val_acc: 0.7182
Epoch 6/50

Epoch 00006: LearningRateScheduler setting learning rate to 0.0011560694.
390/390 [==============================] - 24s 62ms/step - loss: 0.7531 - acc: 0.7408 - val_loss: 0.7778 - val_acc: 0.7294
Epoch 7/50

Epoch 00007: LearningRateScheduler setting learning rate to 0.0010295127.
390/390 [==============================] - 24s 62ms/step - loss: 0.7192 - acc: 0.7514 - val_loss: 0.7443 - val_acc: 0.7480
Epoch 8/50

Epoch 00008: LearningRateScheduler setting learning rate to 0.0009279307.
390/390 [==============================] - 24s 62ms/step - loss: 0.6813 - acc: 0.7651 - val_loss: 0.7266 - val_acc: 0.7528
Epoch 9/50

Epoch 00009: LearningRateScheduler setting learning rate to 0.0008445946.
390/390 [==============================] - 24s 62ms/step - loss: 0.6574 - acc: 0.7749 - val_loss: 0.7135 - val_acc: 0.7582
Epoch 10/50

Epoch 00010: LearningRateScheduler setting learning rate to 0.0007749935.
390/390 [==============================] - 24s 62ms/step - loss: 0.6360 - acc: 0.7817 - val_loss: 0.6396 - val_acc: 0.7827
Epoch 11/50

Epoch 00011: LearningRateScheduler setting learning rate to 0.0007159905.
390/390 [==============================] - 24s 62ms/step - loss: 0.6171 - acc: 0.7883 - val_loss: 0.6892 - val_acc: 0.7670
Epoch 12/50

Epoch 00012: LearningRateScheduler setting learning rate to 0.000665336.
390/390 [==============================] - 24s 62ms/step - loss: 0.6061 - acc: 0.7913 - val_loss: 0.6078 - val_acc: 0.7961
Epoch 13/50

Epoch 00013: LearningRateScheduler setting learning rate to 0.0006213753.
390/390 [==============================] - 24s 62ms/step - loss: 0.5936 - acc: 0.7945 - val_loss: 0.6753 - val_acc: 0.7751
Epoch 14/50

Epoch 00014: LearningRateScheduler setting learning rate to 0.0005828638.
390/390 [==============================] - 24s 62ms/step - loss: 0.5829 - acc: 0.8010 - val_loss: 0.5773 - val_acc: 0.8043
Epoch 15/50

Epoch 00015: LearningRateScheduler setting learning rate to 0.0005488474.
390/390 [==============================] - 24s 61ms/step - loss: 0.5704 - acc: 0.8036 - val_loss: 0.5894 - val_acc: 0.8022
Epoch 16/50

Epoch 00016: LearningRateScheduler setting learning rate to 0.0005185825.
390/390 [==============================] - 25s 63ms/step - loss: 0.5574 - acc: 0.8080 - val_loss: 0.6041 - val_acc: 0.7958
Epoch 17/50

Epoch 00017: LearningRateScheduler setting learning rate to 0.000491481.
390/390 [==============================] - 25s 64ms/step - loss: 0.5558 - acc: 0.8095 - val_loss: 0.5654 - val_acc: 0.8062
Epoch 18/50

Epoch 00018: LearningRateScheduler setting learning rate to 0.0004670715.
390/390 [==============================] - 24s 63ms/step - loss: 0.5374 - acc: 0.8164 - val_loss: 0.6052 - val_acc: 0.7954
Epoch 19/50

Epoch 00019: LearningRateScheduler setting learning rate to 0.0004449718.
390/390 [==============================] - 24s 63ms/step - loss: 0.5354 - acc: 0.8160 - val_loss: 0.5767 - val_acc: 0.8072
Epoch 20/50

Epoch 00020: LearningRateScheduler setting learning rate to 0.000424869.
390/390 [==============================] - 24s 62ms/step - loss: 0.5271 - acc: 0.8190 - val_loss: 0.5814 - val_acc: 0.8018
Epoch 21/50

Epoch 00021: LearningRateScheduler setting learning rate to 0.0004065041.
390/390 [==============================] - 25s 63ms/step - loss: 0.5206 - acc: 0.8195 - val_loss: 0.5557 - val_acc: 0.8127
Epoch 22/50

Epoch 00022: LearningRateScheduler setting learning rate to 0.000389661.
390/390 [==============================] - 25s 63ms/step - loss: 0.5129 - acc: 0.8232 - val_loss: 0.5667 - val_acc: 0.8135
Epoch 23/50

Epoch 00023: LearningRateScheduler setting learning rate to 0.0003741581.
390/390 [==============================] - 24s 63ms/step - loss: 0.5076 - acc: 0.8255 - val_loss: 0.5459 - val_acc: 0.8171
Epoch 24/50

Epoch 00024: LearningRateScheduler setting learning rate to 0.0003598417.
390/390 [==============================] - 24s 62ms/step - loss: 0.5051 - acc: 0.8276 - val_loss: 0.5496 - val_acc: 0.8169
Epoch 25/50

Epoch 00025: LearningRateScheduler setting learning rate to 0.0003465804.
390/390 [==============================] - 25s 63ms/step - loss: 0.4981 - acc: 0.8288 - val_loss: 0.5252 - val_acc: 0.8248
Epoch 26/50

Epoch 00026: LearningRateScheduler setting learning rate to 0.0003342618.
390/390 [==============================] - 25s 63ms/step - loss: 0.4955 - acc: 0.8301 - val_loss: 0.5516 - val_acc: 0.8172
Epoch 27/50

Epoch 00027: LearningRateScheduler setting learning rate to 0.0003227889.
390/390 [==============================] - 25s 63ms/step - loss: 0.4908 - acc: 0.8329 - val_loss: 0.5694 - val_acc: 0.8115
Epoch 28/50

Epoch 00028: LearningRateScheduler setting learning rate to 0.0003120774.
390/390 [==============================] - 25s 63ms/step - loss: 0.4813 - acc: 0.8351 - val_loss: 0.5313 - val_acc: 0.8235
Epoch 29/50

Epoch 00029: LearningRateScheduler setting learning rate to 0.000302054.
390/390 [==============================] - 24s 63ms/step - loss: 0.4792 - acc: 0.8361 - val_loss: 0.5690 - val_acc: 0.8141
Epoch 30/50

Epoch 00030: LearningRateScheduler setting learning rate to 0.0002926544.
390/390 [==============================] - 24s 63ms/step - loss: 0.4759 - acc: 0.8365 - val_loss: 0.5358 - val_acc: 0.8238
Epoch 31/50

Epoch 00031: LearningRateScheduler setting learning rate to 0.0002838221.
390/390 [==============================] - 24s 62ms/step - loss: 0.4738 - acc: 0.8371 - val_loss: 0.5303 - val_acc: 0.8265
Epoch 32/50

Epoch 00032: LearningRateScheduler setting learning rate to 0.0002755074.
390/390 [==============================] - 24s 62ms/step - loss: 0.4700 - acc: 0.8386 - val_loss: 0.5317 - val_acc: 0.8275
Epoch 33/50

Epoch 00033: LearningRateScheduler setting learning rate to 0.000267666.
390/390 [==============================] - 24s 63ms/step - loss: 0.4690 - acc: 0.8385 - val_loss: 0.5521 - val_acc: 0.8198
Epoch 34/50

Epoch 00034: LearningRateScheduler setting learning rate to 0.0002602585.
390/390 [==============================] - 24s 62ms/step - loss: 0.4642 - acc: 0.8402 - val_loss: 0.5423 - val_acc: 0.8202
Epoch 35/50

Epoch 00035: LearningRateScheduler setting learning rate to 0.00025325.
390/390 [==============================] - 24s 63ms/step - loss: 0.4587 - acc: 0.8434 - val_loss: 0.5175 - val_acc: 0.8320
Epoch 36/50

Epoch 00036: LearningRateScheduler setting learning rate to 0.0002466091.
390/390 [==============================] - 24s 62ms/step - loss: 0.4583 - acc: 0.8415 - val_loss: 0.5390 - val_acc: 0.8247
Epoch 37/50

Epoch 00037: LearningRateScheduler setting learning rate to 0.0002403076.
390/390 [==============================] - 24s 62ms/step - loss: 0.4554 - acc: 0.8418 - val_loss: 0.5348 - val_acc: 0.8260
Epoch 38/50

Epoch 00038: LearningRateScheduler setting learning rate to 0.0002343201.
390/390 [==============================] - 24s 62ms/step - loss: 0.4507 - acc: 0.8432 - val_loss: 0.5265 - val_acc: 0.8281
Epoch 39/50

Epoch 00039: LearningRateScheduler setting learning rate to 0.0002286237.
390/390 [==============================] - 24s 63ms/step - loss: 0.4507 - acc: 0.8433 - val_loss: 0.5350 - val_acc: 0.8264
Epoch 40/50

Epoch 00040: LearningRateScheduler setting learning rate to 0.0002231977.
390/390 [==============================] - 25s 63ms/step - loss: 0.4452 - acc: 0.8472 - val_loss: 0.5390 - val_acc: 0.8235
Epoch 41/50

Epoch 00041: LearningRateScheduler setting learning rate to 0.0002180233.
390/390 [==============================] - 24s 62ms/step - loss: 0.4499 - acc: 0.8450 - val_loss: 0.5331 - val_acc: 0.8234
Epoch 42/50

Epoch 00042: LearningRateScheduler setting learning rate to 0.0002130833.
390/390 [==============================] - 24s 62ms/step - loss: 0.4401 - acc: 0.8481 - val_loss: 0.5288 - val_acc: 0.8270
Epoch 43/50

Epoch 00043: LearningRateScheduler setting learning rate to 0.0002083623.
390/390 [==============================] - 24s 63ms/step - loss: 0.4350 - acc: 0.8506 - val_loss: 0.5326 - val_acc: 0.8277
Epoch 44/50

Epoch 00044: LearningRateScheduler setting learning rate to 0.0002038459.
390/390 [==============================] - 24s 62ms/step - loss: 0.4367 - acc: 0.8492 - val_loss: 0.5254 - val_acc: 0.8279
Epoch 45/50

Epoch 00045: LearningRateScheduler setting learning rate to 0.0001995211.
390/390 [==============================] - 24s 62ms/step - loss: 0.4356 - acc: 0.8487 - val_loss: 0.5284 - val_acc: 0.8270
Epoch 46/50

Epoch 00046: LearningRateScheduler setting learning rate to 0.0001953761.
390/390 [==============================] - 24s 62ms/step - loss: 0.4335 - acc: 0.8497 - val_loss: 0.5336 - val_acc: 0.8255
Epoch 47/50

Epoch 00047: LearningRateScheduler setting learning rate to 0.0001913998.
390/390 [==============================] - 24s 62ms/step - loss: 0.4264 - acc: 0.8550 - val_loss: 0.5424 - val_acc: 0.8221
Epoch 48/50

Epoch 00048: LearningRateScheduler setting learning rate to 0.0001875821.
390/390 [==============================] - 24s 62ms/step - loss: 0.4291 - acc: 0.8526 - val_loss: 0.5231 - val_acc: 0.8297
Epoch 49/50

Epoch 00049: LearningRateScheduler setting learning rate to 0.0001839137.
390/390 [==============================] - 24s 62ms/step - loss: 0.4292 - acc: 0.8533 - val_loss: 0.5248 - **val_acc: 0.8301**
Epoch 50/50

Epoch 00050: LearningRateScheduler setting learning rate to 0.000180386.
390/390 [==============================] - 25s 63ms/step - loss: 0.4282 - acc: 0.8519 - val_loss: 0.5255 - **val_acc: 0.8293**
dep_sep_model took 1224.13 seconds to train



