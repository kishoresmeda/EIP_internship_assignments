1. The result of model.evaluate (on test data) : 
  [0.017587539112311788, 0.9953]
  
2. Strategy to achieve ~0.9953 score with <15K Parameters
  - Increased the dropout percentage a bit.
  - Decreased the Number of filters used in a few layers.
  - Tried changing the epoch size but no impact. 20 was giving good accuracy.

3. Logs of 20 Epochs for a model of 14,900 Parameters:

Train on 60000 samples, validate on 10000 samples
Epoch 1/20

Epoch 00001: LearningRateScheduler setting learning rate to 0.003.
60000/60000 [==============================] - 15s 251us/step - loss: 0.2455 - acc: 0.8779 - val_loss: 0.0378 - val_acc: 0.9884
Epoch 2/20

Epoch 00002: LearningRateScheduler setting learning rate to 0.0022744503.
60000/60000 [==============================] - 8s 140us/step - loss: 0.2371 - acc: 0.8804 - val_loss: 0.0284 - val_acc: 0.9909
Epoch 3/20

Epoch 00003: LearningRateScheduler setting learning rate to 0.0018315018.
60000/60000 [==============================] - 8s 141us/step - loss: 0.2344 - acc: 0.8798 - val_loss: 0.0206 - val_acc: 0.9931
Epoch 4/20

Epoch 00004: LearningRateScheduler setting learning rate to 0.0015329586.
60000/60000 [==============================] - 8s 140us/step - loss: 0.2253 - acc: 0.8822 - val_loss: 0.0227 - val_acc: 0.9935
Epoch 5/20

Epoch 00005: LearningRateScheduler setting learning rate to 0.0013181019.
60000/60000 [==============================] - 9s 142us/step - loss: 0.2230 - acc: 0.8837 - val_loss: 0.0219 - val_acc: 0.9929
Epoch 6/20

Epoch 00006: LearningRateScheduler setting learning rate to 0.0011560694.
60000/60000 [==============================] - 9s 143us/step - loss: 0.2249 - acc: 0.8824 - val_loss: 0.0174 - val_acc: 0.9946
Epoch 7/20

Epoch 00007: LearningRateScheduler setting learning rate to 0.0010295127.
60000/60000 [==============================] - 8s 139us/step - loss: 0.2219 - acc: 0.8829 - val_loss: 0.0207 - val_acc: 0.9938
Epoch 8/20

Epoch 00008: LearningRateScheduler setting learning rate to 0.0009279307.
60000/60000 [==============================] - 8s 141us/step - loss: 0.2206 - acc: 0.8822 - val_loss: 0.0188 - val_acc: 0.9942
Epoch 9/20

Epoch 00009: LearningRateScheduler setting learning rate to 0.0008445946.
60000/60000 [==============================] - 8s 140us/step - loss: 0.2156 - acc: 0.8849 - val_loss: 0.0179 - val_acc: 0.9945
Epoch 10/20

Epoch 00010: LearningRateScheduler setting learning rate to 0.0007749935.
60000/60000 [==============================] - 8s 140us/step - loss: 0.2152 - acc: 0.8837 - val_loss: 0.0198 - val_acc: 0.9936
Epoch 11/20

Epoch 00011: LearningRateScheduler setting learning rate to 0.0007159905.
60000/60000 [==============================] - 8s 139us/step - loss: 0.2171 - acc: 0.8831 - val_loss: 0.0188 - val_acc: 0.9942
Epoch 12/20

Epoch 00012: LearningRateScheduler setting learning rate to 0.000665336.
60000/60000 [==============================] - 8s 141us/step - loss: 0.2140 - acc: 0.8835 - val_loss: 0.0200 - val_acc: 0.9934
Epoch 13/20

Epoch 00013: LearningRateScheduler setting learning rate to 0.0006213753.
60000/60000 [==============================] - 8s 138us/step - loss: 0.2158 - acc: 0.8841 - val_loss: 0.0178 - val_acc: 0.9950
Epoch 14/20

Epoch 00014: LearningRateScheduler setting learning rate to 0.0005828638.
60000/60000 [==============================] - 8s 140us/step - loss: 0.2147 - acc: 0.8822 - val_loss: 0.0185 - val_acc: 0.9944
Epoch 15/20

Epoch 00015: LearningRateScheduler setting learning rate to 0.0005488474.
60000/60000 [==============================] - 9s 143us/step - loss: 0.2107 - acc: 0.8851 - val_loss: 0.0205 - val_acc: 0.9943
Epoch 16/20

Epoch 00016: LearningRateScheduler setting learning rate to 0.0005185825.
60000/60000 [==============================] - 8s 140us/step - loss: 0.2131 - acc: 0.8859 - val_loss: 0.0190 - val_acc: 0.9951
Epoch 17/20

Epoch 00017: LearningRateScheduler setting learning rate to 0.000491481.
60000/60000 [==============================] - 8s 140us/step - loss: 0.2117 - acc: 0.8847 - val_loss: 0.0165 - val_acc: 0.9952
Epoch 18/20

Epoch 00018: LearningRateScheduler setting learning rate to 0.0004670715.
60000/60000 [==============================] - 8s 138us/step - loss: 0.2155 - acc: 0.8832 - val_loss: 0.0190 - val_acc: 0.9950
Epoch 19/20

Epoch 00019: LearningRateScheduler setting learning rate to 0.0004449718.
60000/60000 [==============================] - 8s 140us/step - loss: 0.2095 - acc: 0.8855 - val_loss: 0.0159 - val_acc: 0.9953
Epoch 20/20

Epoch 00020: LearningRateScheduler setting learning rate to 0.000424869.
60000/60000 [==============================] - 8s 141us/step - loss: 0.2120 - acc: 0.8854 - val_loss: 0.0176 - val_acc: 0.9953

<keras.callbacks.History at 0x7fc9711a9198>
