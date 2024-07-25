# Disentngling IND and OOD in VAE latent space
This repository includes the python.pytorch implementation of the case study in out recent ICASSP2025 manuscript:
SPATIALLY DISENTANGLE IN-DOMAIN AND OUT-OF-DOMAIN IN LATENT SPACE

Step 1:
In data space (2D), we assume Gaussian distribution(s) as in-domain (IND), out-of-domain (OOD) for training:
![X](https://github.com/user-attachments/assets/f6a86d93-050a-460c-8b95-59239dea3595)

A VAE is trained to project IND into another 2-D latent space:
![Z](https://github.com/user-attachments/assets/215b24b6-97a5-4811-a9bf-85d2c13430e0)



Step 2:
By running our boundary sampler (PGBS), we can define and sample from the "boundary" of IND in latent space



Step 3:
We can then let OOD samples to fit into the boundary we have defined in latent space, which enables VAE + PGBS to perform accurate OOD detection for IND
![Z_regularised](https://github.com/user-attachments/assets/b461142f-bbc6-4aaa-9168-668ba66a8ecb)

