# ColorizeTOP
Touchdesigner Colorizing TOP. Opencv Dnn colorizing
"Black & White" | Color
--------------- | ----
![Cabane](https://github.com/shieman/ColorizeTOP/blob/master/Images/Cabane.jpg) | ![Cabane Couleur](https://github.com/shieman/ColorizeTOP/blob/master/Images/cabane_couleur.jpg)
![Paulilles](https://github.com/shieman/ColorizeTOP/blob/master/Images/Paulliles.jpg) | ![Paulilles Couleur](https://github.com/shieman/ColorizeTOP/blob/master/Images/Paulilles_couleur.jpg)

# How it works
This c++ Top is made with opencv 4.2 dnn using Cuda 10.2. It uses machine learning model to predict colors.

It's a Windows version, but you can compile with other Oses, since it's just c++ and opencv (and Cuda Cudnn for GPU acceleration)

Using movie files, i get an average 20fps with cuda dnn, 2 fps without.

# What you need
To make it working you need :
* opencv_world420.dll near Colorizing.dll
  You can get it on https://jamesbowley.co.uk/downloads/
  Take the opencv 4.2 version with cuda 10.2
  In subdirectory x64\vc16\bin, you'll find opencv420.dll
* Cuda 10.2 and cuDNN 7.6.5.32 installed if you want dnn gpu acceleration.
* the machine learning models near colorizing.dll :
    - colorization_deploy_v2.prototxt
    https://raw.githubusercontent.com/richzhang/colorization/master/colorization/models/colorization_deploy_v2.prototxt
    - colorization_release_v2.caffemodel
    http://eecs.berkeley.edu/~rich.zhang/projects/2016_colorization/files/demo_v2/colorization_release_v2.caffemodel
* Colorizing.dll of course
  I put a windows version in release directory (compiled with opencv 4.2 cuda 10.2)
* I put colorizing.toe Touchdesigner in release directory to test it, with Level settings and Recording image
  
# Thanks to
* James Bowley for his shared opencv binaries https://jamesbowley.co.uk/
* learnopencv.com and pyimagesearch.com for base helps
* All people sharing on Touchdesigner forum
