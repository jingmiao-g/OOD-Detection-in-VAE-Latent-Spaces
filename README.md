# Disentngling IND and OOD in VAE latent space
This repository includes the python.pytorch implementation of the case study in out recent ICASSP2025 manuscript:
SPATIALLY DISENTANGLE IN-DOMAIN AND OUT-OF-DOMAIN IN LATENT SPACE

Step 1:
In data space (2D), we assume Gaussian distribution(s) as in-domain (IND), out-of-domain (OOD) for training:
![X](https://github.com/user-attachments/assets/40013604-2b64-44c2-83b7-f884c1bfb76b)

A VAE is trained to project IND into another 2-D latent space:
![Z](https://github.com/user-attachments/assets/062e6a6d-5f26-4797-a54d-9d82d8593c80)

Step 2:
By running our boundary sampler (PGBS), we can define and sample from the "boundary" of IND in latent space

Step 3:
We can then let OOD samples to fit into the boundary we have defined in latent space, which enables VAE + PGBS to perform accurate OOD detection for IND
![Z_regularised](https://github.com/user-attachments/assets/c18ee0b6-1f41-4c44-a022-ab093ece8904)
