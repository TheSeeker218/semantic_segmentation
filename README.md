# semantic_segmentation

## Approach:-
- Replicae U-net architecture in tensorflow 
  - This architecture merges spatial details at High resolution (from encoding layer) and  different features extracted at lower resolution  in decoding layer.
  - Suitable for localizing the specific feature we want to extract.

## Augmentation
- CenterCrop
- RandomRotate90
- GridDistortion
- HorizontalFlip
- VerticalFlip



## Training and validation metrics
- ### loss function
  - consideration
    - mean sqaured error
    - binary cross entropy
      - works well with output layer giving probabilities
      - when a neuron has a value close to 0 or 1, the gradient  becomes very small in case of mean squared loss
      
- ### optimizer
  - Adam

- ### 
## Evaluation metrics 
## Hyperparameters choices 
- relu_alpha = 0.2 (trial and error)
- drop_out = 0.5 (network size too big to extract more features , values chosen by trial and error)

## TODO 
  - Augmentation -- RandomCrop
  - LearningRate(iteration) schedule
  - try  Mask_RCNN, unsupervise masking(L_ACWE), Fast_SCNN
