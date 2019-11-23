1. The result of model.evaluate (on test data) : 
  [0.019479754745168613, 0.9942]
  
2. Strategy to achieve ~0.9942 score with <15K Parameters
  - Increased the dropout percentage a bit.
  - Decreased the Number of filters used in a few layers.
  - Tried changing the epoch size but no impact. 20 was giving good accuracy.

3. Logs of 20 Epochs for a model of 14,535 Parameters:

Train on 60000 samples, validate on 10000 samples
Epoch 1/20

Epoch 00001: LearningRateScheduler setting learning rate to 0.003.
60000/60000 [==============================] - 13s 221us/step - loss: 0.6720 - acc: 0.7793 - val_loss: 0.1294 - val_acc: 0.9760
Epoch 2/20

Epoch 00002: LearningRateScheduler setting learning rate to 0.0022744503.
60000/60000 [==============================] - 9s 147us/step - loss: 0.3905 - acc: 0.8573 - val_loss: 0.0611 - val_acc: 0.9859
Epoch 3/20

Epoch 00003: LearningRateScheduler setting learning rate to 0.0018315018.
60000/60000 [==============================] - 9s 145us/step - loss: 0.3292 - acc: 0.8697 - val_loss: 0.0476 - val_acc: 0.9880
Epoch 4/20

Epoch 00004: LearningRateScheduler setting learning rate to 0.0015329586.
60000/60000 [==============================] - 9s 145us/step - loss: 0.2985 - acc: 0.8738 - val_loss: 0.0454 - val_acc: 0.9892
Epoch 5/20

Epoch 00005: LearningRateScheduler setting learning rate to 0.0013181019.
60000/60000 [==============================] - 9s 146us/step - loss: 0.2808 - acc: 0.8766 - val_loss: 0.0368 - val_acc: 0.9902
Epoch 6/20

Epoch 00006: LearningRateScheduler setting learning rate to 0.0011560694.
60000/60000 [==============================] - 9s 148us/step - loss: 0.2671 - acc: 0.8778 - val_loss: 0.0313 - val_acc: 0.9912
Epoch 7/20

Epoch 00007: LearningRateScheduler setting learning rate to 0.0010295127.
60000/60000 [==============================] - 9s 146us/step - loss: 0.2612 - acc: 0.8771 - val_loss: 0.0346 - val_acc: 0.9905
Epoch 8/20

Epoch 00008: LearningRateScheduler setting learning rate to 0.0009279307.
60000/60000 [==============================] - 9s 146us/step - loss: 0.2507 - acc: 0.8808 - val_loss: 0.0315 - val_acc: 0.9915
Epoch 9/20

Epoch 00009: LearningRateScheduler setting learning rate to 0.0008445946.
60000/60000 [==============================] - 9s 144us/step - loss: 0.2504 - acc: 0.8797 - val_loss: 0.0241 - val_acc: 0.9931
Epoch 10/20

Epoch 00010: LearningRateScheduler setting learning rate to 0.0007749935.
60000/60000 [==============================] - 9s 145us/step - loss: 0.2451 - acc: 0.8815 - val_loss: 0.0265 - val_acc: 0.9920
Epoch 11/20

Epoch 00011: LearningRateScheduler setting learning rate to 0.0007159905.
60000/60000 [==============================] - 9s 146us/step - loss: 0.2418 - acc: 0.8804 - val_loss: 0.0279 - val_acc: 0.9923
Epoch 12/20

Epoch 00012: LearningRateScheduler setting learning rate to 0.000665336.
60000/60000 [==============================] - 9s 145us/step - loss: 0.2393 - acc: 0.8808 - val_loss: 0.0232 - val_acc: 0.9931
Epoch 13/20

Epoch 00013: LearningRateScheduler setting learning rate to 0.0006213753.
60000/60000 [==============================] - 9s 145us/step - loss: 0.2367 - acc: 0.8828 - val_loss: 0.0225 - val_acc: 0.9934
Epoch 14/20

Epoch 00014: LearningRateScheduler setting learning rate to 0.0005828638.
60000/60000 [==============================] - 9s 144us/step - loss: 0.2333 - acc: 0.8824 - val_loss: 0.0233 - val_acc: 0.9927
Epoch 15/20

Epoch 00015: LearningRateScheduler setting learning rate to 0.0005488474.
60000/60000 [==============================] - 9s 144us/step - loss: 0.2301 - acc: 0.8842 - val_loss: 0.0249 - val_acc: 0.9926
Epoch 16/20

Epoch 00016: LearningRateScheduler setting learning rate to 0.0005185825.
60000/60000 [==============================] - 9s 147us/step - loss: 0.2313 - acc: 0.8818 - val_loss: 0.0209 - val_acc: 0.9938
Epoch 17/20

Epoch 00017: LearningRateScheduler setting learning rate to 0.000491481.
60000/60000 [==============================] - 9s 146us/step - loss: 0.2273 - acc: 0.8842 - val_loss: 0.0224 - val_acc: 0.9939
Epoch 18/20

Epoch 00018: LearningRateScheduler setting learning rate to 0.0004670715.
60000/60000 [==============================] - 9s 144us/step - loss: 0.2253 - acc: 0.8848 - val_loss: 0.0201 - val_acc: 0.9936
Epoch 19/20

Epoch 00019: LearningRateScheduler setting learning rate to 0.0004449718.
60000/60000 [==============================] - 9s 144us/step - loss: 0.2284 - acc: 0.8817 - val_loss: 0.0192 - val_acc: 0.9944
Epoch 20/20

Epoch 00020: LearningRateScheduler setting learning rate to 0.000424869.
60000/60000 [==============================] - 9s 143us/step - loss: 0.2252 - acc: 0.8816 - val_loss: 0.0195 - val_acc: 0.9942

<keras.callbacks.History at 0x7fc971a35080>
