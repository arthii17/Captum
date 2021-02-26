# Captum
Exploring interpretability of PyTorch models using Captum

Captum helps ML researchers more easily implement interpretability algorithms that can interact with PyTorch models.For model developers, Captum can be used to improve and troubleshoot models by facilitating the identification of different features that contribute to a model’s output in order to design better models and troubleshoot unexpected model outputs.(https://captum.ai/)

Here we are interpreting the Resnet model's prediction of images and comparing the resuts using attribution techniques such as 'Integrated Gradients' & 'Occlusion' provided by Captum. 

Scenario 1 - Correct Prediction by PyTorch model 
Here the input image is penguin and the model prediction is "king penguin" as expected. 

Attribution Outputs Integrated Gradients 
![image](https://github.com/arthii17/Captum/blob/main/Images/IntegratedGradient_Penguin.JPG)
 
Occlusion Graph Large Window size
![image](https://github.com/arthii17/Captum/blob/main/Images/OcclusionLarge_Penguin.JPG)

Occlusion Graph Small Window size
![image](https://github.com/arthii17/Captum/blob/main/Images/OcclusionSmall_Penguin.JPG)

Scenario 2 - Incorrect Prediction by PyTorch model 
Here the input image is of swan but the model wrongly interprets it as penguin. In scenarios like this, captum's attribution graphs are very helpful to figure out why the model wrongly interpreted it and where was it actually looking at. Let us see the outputs of Integrated gradients graph and occlusion graphs to figure out why it identified swan as penguin. 

Attribution Outputs Integrated Gradients 
![image](https://github.com/arthii17/Captum/blob/main/Images/IntegratedGradient_Swan.JPG)
 
Occlusion Graph Large Window size
![image](https://github.com/arthii17/Captum/blob/main/Images/OcclusionLarge_Swan.JPG)

Occlusion Graph Small Window size
![image](https://github.com/arthii17/Captum/blob/main/Images/OcclusionSmall_Swan.JPG)

As we could clearly see from the graphs that the upper part of the goose, espectially the beak, seems to be the most critical for the model to predict this class. Since it highly resembles penguin's head shape and beak, the swan is wrongly interpreted as penguin.
