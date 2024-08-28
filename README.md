# MRILatentEnergyModel

**Autoencoder Folder:**
`MRIAutoencoderDiscriminator` is code that trains an autoencoder alongside a discriminator, and `MRIAutoencoderDiscriminator2` is the same thing except the discriminator's weights get reset in certain intervals. `MRIAutoencoderDiscriminator2` produced the best results which were then used for the energy model.

**Energy folder:**
This folder contains a mix of files that Manu made, and a few that I modified to work for my purposes. The relevant notebooks are `fastmri_train2.ipynb` for training the model on my latents, and `fastmri_sample_small2.ipynb` for sampling.
The training notebook will save checkpoints in the `logs` directory, specifically `logs > fastmri_EBM_{args.time} > models`.
In the sampling code, be sure to select your desired `save_folder` and `settings_fname`, and select the correct `args.net_indx` value (for example, if the checkpoint you want to sample with is `mdsm_ebm150000.pt`, then set `args.net_indx = 150000`)
