# Machine Learning Assignments Repo

##### Assignments from Machine Learning subject at Universidad Nacional del Sur.

## Final *Machine Learning* Project: *Transfer Learning* con las redes neuronales MobileNetV3 y EfficientNetV2B0

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
#### Using pre-trained weights with a new classifier

    > Epoch 8/8 346/346 [==============================] - 44s 125ms/step 
    > loss: 0.523 - accuracy: 0.851 - val_loss: 0.423 - val_accuracy: 0.885
    
<p align="center">
  <img src="https://user-images.githubusercontent.com/71747228/179805665-f9477f78-414b-4e2f-8ef5-e2694514b705.png" />
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/71747228/179805719-70fef0d7-a16a-4b76-9723-79796451985b.png" />
</p>

#### Fine-tuning last layers

    # Fine-tune desde aca en adelante
    fine_tune_at = 160

    base_model.trainable = True

    # Freeze todas las capas anteriores a fine_tune_at
    for layer in base_model.layers[:fine_tune_at]:
      layer.trainable = False
      
###### After re-training accuracy

    > Epoch 15/15 346/346 [==============================] - 70s 200ms/step - 
    > loss: 0.169 - accuracy: 0.946 - val_loss: 0.184 - val_accuracy: 0.943

There was good improvement, and after a few epochs the model was starting to overfit.

<p align="center">
  <img src="https://user-images.githubusercontent.com/71747228/179807224-6233e8ab-097e-4c6d-a62c-4f037be2d0cd.png" />
</p>

#### Test set results

    loss, accuracy = model.evaluate(test_dataset)
    print('Test accuracy :', accuracy)

    > 17/17 [==============================] - 2s 95ms/step - 
    > loss: 0.165 - accuracy: 0.945 Test accuracy : 0.945
