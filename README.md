# Captum
Exploring interpretability of PyTorch models using Captum

Captum helps ML researchers more easily implement interpretability algorithms that can interact with PyTorch models.For model developers, Captum can be used to improve and troubleshoot models by facilitating the identification of different features that contribute to a model’s output in order to design better models and troubleshoot unexpected model outputs.(https://captum.ai/)

Here we are interpreting the Resnet model's prediction of images and comparing the resuts using attribution techniques such as 'Integrated Gradients' & 'Occlusion' provided by Captum. 

Scenario 1 - Correct Prediction by PyTorch model 
Here the input image is penguin and the model prediction is "king penguin" as expected. 
Attribution Outputs-Integrated Gradients:
![image](https://github.com/arthii17/Captum/blob/main/Images/IntegratedGradient_Penguin.JPG)
 

Occlusion Graph(Large Window size):
![image](https://github.com/arthii17/Captum/blob/main/Images/OcclusionLarge_Penguin.JPG)

Occlusion Graphs(Small Window size):
![image](https://github.com/arthii17/Captum/blob/main/Images/OcclusionSmall_Penguin.JPG)





