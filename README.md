# git-lfs-demo
This repository demonstrates Git LFS use with Artifactory.

Create a local repository in Artifactory of type Git LFS. For this example, we will be using a repository called gitlfs-local on https://104.197.232.86/artifactory. To log in, the username is gitlfs and password is demo.

Clone the repository using the command ```git clone https://github.com/jfrogtraining/git-lfs-demo.git```. Go into that repository.

Use the command ```open .``` to see everything that is currently inside the Github repository.

Add files that you would like to push to the Github repository and any large files that you would like to push to the Git LFS local repository in Artifactory.

In order to connect the Github repository to the Git LFS in Artifactory, we will need to change the ```.git/config``` file. A sample is provided in this repository.

Now, type the command ```git lfs track “*.<file extension>”```. The file extension should match the file extension of the files you would like to push to the Git LFS repository in Artifactory. For example, if we wanted to push all the zip and war files to the Git LFS repository, we would type in ```git lfs track “*.zip”```, then ```git lfs track “*.war”```.

Finally, use the command ```git lfs push origin master``` to push all the source code to the Github repository and the large files to the Git LFS repository in Artifactory.
