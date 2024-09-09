# Separating IND and OOD in VAE latent space
This repository includes the python/pytorch implementation of the case study in out recent ICASSP2025 manuscript:

Improved Out-of-domain Detection in VAE Latent Spaces with Boundary-driven Regularisation

Authors: Miao JING, Vidhyasaharan Sethu, Beena Ahmed 
Institution: The University of New South Wales
Date: 2024 September


Same observations can be reproduced by running jupyterlab files Step1, Step2 and Step3 in order.

Step 1:
In data space (2D), we assume Gaussian distribution(s) as in-domain (IND), out-of-domain (OOD) for training:

![X](https://github.com/user-attachments/assets/241e21f6-475e-4b53-b410-247763aa23fa)


A VAE is trained to project IND into another 2-D latent space:

![Z](https://github.com/user-attachments/assets/91544a81-d68f-4acc-8f98-8da30af18050)




Step 2:
By running our boundary sampler (PGBS), we can define and sample from the "boundary" of IND in latent space



Step 3:
We can then regularise the VAE encoder to encode OOD samples into the boundary we have defined in latent space, which enables VAE + PGBS to perform accurate OOD detection

![Z_regularised](https://github.com/user-attachments/assets/c324a2c7-0cce-4fdf-b483-525a1f00c1cf)


