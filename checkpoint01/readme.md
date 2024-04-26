First attempt at a checkpont

- All the data used was from freely avaliable sources i.e. Camera Manufacture Test files, and Plates from tutorial sites on the internet. -only a single frame is uploaded here as it's too big for github but if you request, I can put it up on a file-sharing platform.
- Train:
  - this took on a RTX3090 2h to train and about an 15min to cache (on windows) with a 32*32pix x10000 dataset / 1000 epocs / 181818 steps
  - ground truth grade random variation:
    - 1 stop (slope)
    - 0.05 offset
    - 0.05 Power
- lessons / todo's for next time
  - quality rather than quantatiy of data is key
    - I needed to curate the data (images) far more carefully, as the scatter approch here leads to worse prediction in my tests. Less is more!
    - I needed to weigh the grade ground truths more consistent RGB exposure, and temperature pattens
  - the hardest thing for me was to find the balance between training data instance count / epocs / model size. Generally I used high data instances / low epocs / medium size. 
  - getting the data cached was often slow - also there is a bug/feature that if an inference file is enabled to the same folder one is trainning caching takes x100 longer
  - i have yet to create a model on a larger dataset due to
    - finding that resumeing training created a strong bias to the new train, and deceased prediction, as well as the prediction often decreacing whenever i increaced the time it took to train (i assume overfitting)
    - running out of time/work to do lengthy tests

Thanks to the foundy for granting me 1 month trial nuke licence try this out
