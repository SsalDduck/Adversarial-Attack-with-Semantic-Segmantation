# Dense-Adversarial-Attack-in-Semantic-Segmantation

  This repository generate Adversarial Attack Image by using Dense Adversarial Attack in Semantic Segmantation Method (papaer : https://arxiv.org/abs/1703.08603 ).

---
# Demo

# Original Image 
![image](https://github.com/SsalDduck/Adversarial-Attack-with-Semantic-Segmantation/assets/124281401/14878e59-2c92-42b5-ac63-44483c9ccedc)

# Original UNet Output
![image](https://github.com/SsalDduck/Adversarial-Attack-with-Semantic-Segmantation/assets/124281401/0b948d02-3746-4c35-9f26-d110163e380d)

# After Adversarial Attack
![image](https://github.com/SsalDduck/Adversarial-Attack-with-Semantic-Segmantation/assets/124281401/20b05b95-e0cd-4c56-acf2-0442f4056932)



---

# Tutorial

# Step 1. Train UNet with PascalVOC
  You don't have to download pascalVOC dataset by yourself.\
  Train_UNet file automatically download PascalVOC train&validation Dataset in torchvision.datasets.\
  All you need is adjuset HyperParameter and run source code.

  ---
  
# Step 2. Test UNet 
  PascalVOC's test dataset is not public so I used validation Dataset for test.\
  You can test your own UNet and make sure to check crossentropy Loss for compare Attack dataset.

  ---
  
# Step 3. Generate Adversarial Example with your UNet.
  Run Adimg_generator src, You can easily genaerate perturbation.\
  According to paper, Main idea of DAG is gradient with fake GT.\
  There are three types of denseadversarial attack.\
  DAG_A , DAG_B , DAG_C . Their difference is way to make fake GT.\
  Those 3 method's reference : https://github.com/sky4689524/Pytorch_AdversarialAttacks

  ---
  
# Step 4. Test Adversarial Dataset
  Run test_attack src will able to check model output and Attack image in tesnorboard.\
  Also, Now you can compare  crossentropy loss between original image and attack image.
  
