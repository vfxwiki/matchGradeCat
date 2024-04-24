First attempt at a checkpont

- All the data used was from freely avaliable sources i.e. Camera Manufacture Test files, and Plates from tutorial sites on the internet. -only a single frame is uploaded here as it's too big for github but if you want to see it all, I can put it up on a file-sharing platform ifr you want.
- lessons / todo's for next time
  - quality rather than quantatiy of data is key, and I needed to curate the data far more carefully, as a scatter approch leads to worse prediction
  - the hardest thing for me was to find the balance between training data instance count / epocs / model size. Generally I used high data instances / low epocs / medium size
  - getting the data cached was often slow - also there is a bug/feature that if an inference file is enabled to the same folder one is trainning caching takes x100 longer
  - this took on a RTX3090 2h to train and about an 15min to cache (on windows) with a 32*32pix x10000 dataset
  - i have yet to create a model on a larger dataset due to
    - finding that resumeing training created a strong bias to the new train, and deceased prediction
    - running out of time and nuke licence
.
