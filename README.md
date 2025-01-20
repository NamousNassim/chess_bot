
## CHESS AI

## Data 
 Lichess <a href="https://database.lichess.org">database</a>

## GUI
`pygame`  `python-chess` modules.

## Model
 architecture  <a href="http://cs231n.stanford.edu/reports/2015/pdfs/ConvChess.pdf">Link</a>.


```
Model: "model"
__________________________________________________________________________________________________
 Layer (type)                   Output Shape         Param #     Connected to                     
==================================================================================================
 input_1 (InputLayer)           [(None, 8, 8, 12)]   0           []                               
                                                                                                  
 conv2d (Conv2D)                (None, 8, 8, 32)     3488        ['input_1[0][0]']                
                                                                                                  
 batch_normalization (BatchNorm  (None, 8, 8, 32)    128         ['conv2d[0][0]']                 
 alization)                                                                                       
                                                                                                  
 activation (Activation)        (None, 8, 8, 32)     0           ['batch_normalization[0][0]']    
                                                                                                  
 conv2d_1 (Conv2D)              (None, 8, 8, 64)     18496       ['activation[0][0]']             
                                                                                                  
 batch_normalization_1 (BatchNo  (None, 8, 8, 64)    256         ['conv2d_1[0][0]']               
 rmalization)                                                                                     
                                                                                                  
 activation_1 (Activation)      (None, 8, 8, 64)     0           ['batch_normalization_1[0][0]']  
                                                                                                  
 conv2d_2 (Conv2D)              (None, 8, 8, 256)    147712      ['activation_1[0][0]']           
                                                                                                  
 batch_normalization_2 (BatchNo  (None, 8, 8, 256)   1024        ['conv2d_2[0][0]']               
 rmalization)                                                                                     
                                                                                                  
 activation_2 (Activation)      (None, 8, 8, 256)    0           ['batch_normalization_2[0][0]']  
                                                                                                  
 concatenate (Concatenate)      (None, 8, 8, 512)    0           ['activation_2[0][0]',           
                                                                  'activation_2[0][0]']           
                                                                                                  
 conv2d_3 (Conv2D)              (None, 8, 8, 256)    1179904     ['concatenate[0][0]']            
                                                                                                  
 batch_normalization_3 (BatchNo  (None, 8, 8, 256)   1024        ['conv2d_3[0][0]']               
 rmalization)                                                                                     
                                                                                                  
 activation_3 (Activation)      (None, 8, 8, 256)    0           ['batch_normalization_3[0][0]']  
                                                                                                  
 concatenate_1 (Concatenate)    (None, 8, 8, 320)    0           ['activation_3[0][0]',           
                                                                  'activation_1[0][0]']           
                                                                                                  
 conv2d_4 (Conv2D)              (None, 8, 8, 256)    737536      ['concatenate_1[0][0]']          
                                                                                                  
 batch_normalization_4 (BatchNo  (None, 8, 8, 256)   1024        ['conv2d_4[0][0]']               
 rmalization)                                                                                     
                                                                                                  
 activation_4 (Activation)      (None, 8, 8, 256)    0           ['batch_normalization_4[0][0]']  
                                                                                                  
 concatenate_2 (Concatenate)    (None, 8, 8, 288)    0           ['activation_4[0][0]',           
                                                                  'activation[0][0]']             
                                                                                                  
 conv2d_5 (Conv2D)              (None, 8, 8, 256)    663808      ['concatenate_2[0][0]']          
                                                                                                  
 batch_normalization_5 (BatchNo  (None, 8, 8, 256)   1024        ['conv2d_5[0][0]']               
 rmalization)                                                                                     
                                                                                                  
 activation_5 (Activation)      (None, 8, 8, 256)    0           ['batch_normalization_5[0][0]']  
                                                                                                  
 dense (Dense)                  (None, 8, 8, 256)    65792       ['activation_5[0][0]']           
                                                                                                  
 batch_normalization_6 (BatchNo  (None, 8, 8, 256)   1024        ['dense[0][0]']                  
 rmalization)                                                                                     
                                                                                                  
 dense_1 (Dense)                (None, 8, 8, 64)     16448       ['batch_normalization_6[0][0]']  
                                                                                                  
 batch_normalization_7 (BatchNo  (None, 8, 8, 64)    256         ['dense_1[0][0]']                
 rmalization)                                                                                     
                                                                                                  
 dense_2 (Dense)                (None, 8, 8, 1)      65          ['batch_normalization_7[0][0]']  
                                                                                                  
 batch_normalization_8 (BatchNo  (None, 8, 8, 1)     4           ['dense_2[0][0]']                
 rmalization)                                                                                     
                                                                                                  
 softmax (Softmax)              (None, 8, 8, 1)      0           ['batch_normalization_8[0][0]']  
                                                                                                  
==================================================================================================
Total params: 2,839,013
Trainable params: 2,836,131
Non-trainable params: 2,882
__________________________________________________________________________________________________
```
