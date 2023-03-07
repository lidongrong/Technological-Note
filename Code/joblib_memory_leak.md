This MarkDown file discusses how to solve the memory leak problem in joblib.

While operating an extremely large dataset, joblib will map the large array onto a disk and distribute each worker a hash code for them to get access to that dataset. 
This mechanism is called memmap (memory mapping).

Therefore, when working with latent variable models, we usually manipulate the original dataset (such as imputing, estimate latent state, etc) and this will cause 
joblib to store a new array onto the disk. Even if you delete the original dataset in the memory, the memmap object in the disk will not be deleted. Therefore, doing this
repeatly will cause the disk be filled with memory mapping objects and lead to collapsing.

To solve this problem, one must manually manage the memory. To tackle this, see tutorial in section **Manual Management of memmapped input data** in
https://joblib.readthedocs.io/en/latest/parallel.html
