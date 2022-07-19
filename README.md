# Machine Learning Assignments

##### Assignments from Machine Learning subject at Universidad Nacional del Sur.

## Trabajo Final de *Machine Learning*: *Transfer Learning* con las redes neuronales MobileNetV3 y EfficientNetV2B0

#### Abstract
I used transfer learning on image classification Convolutional
Neural Networks in TensorFlow. Images of fourteen types of
flowers were classified with great accuracy.

### Preprocessing
#### Data augmentation: flipping and rotations

<p align="center">
  <img src="https://user-images.githubusercontent.com/71747228/179804260-901ee156-7e5d-49c1-98cc-c8ba5f302477.png" />
</p>

### Transfer learning
#### Using pre-trained weights with a different classifier

    Epoch 8/8 346/346 [==============================] - 44s 125ms/step 
    loss: 0.5227 - accuracy: 0.8506 - val_loss: 0.4225 - val_accuracy: 0.8848
    
<p align="center">
  <img src="https://user-images.githubusercontent.com/71747228/179805665-f9477f78-414b-4e2f-8ef5-e2694514b705.png" />
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/71747228/179805719-70fef0d7-a16a-4b76-9723-79796451985b.png" />
</p>

#### Fine-tuning last layers
