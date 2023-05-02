Download Link: https://assignmentchef.com/product/solved-comp9517-lab2-sift-scale-invariant-feature-transform
<br>
<strong>SIFT: Scale-Invariant Feature Transform </strong>

A well-known algorithm in computer vision to detect and describe local features in images is the scale-invariant feature transform (SIFT). Its applications include object recognition, mapping and navigation, image stitching, 3D modelling, object tracking, and others.

A SIFT feature of an image is a salient keypoint with an associated descriptor. SIFT computation is commonly divided into two steps: 1) detection and 2) description.

At the end of the detection step, for each keypoint the SIFT algorithm computes the:

<ul>

 <li>keypoint spatial coordinates (x, y),</li>

 <li>keypoint scale (in the scale space),</li>

 <li>keypoint dominant orientation.</li>

</ul>

The description step computes a distinctive 128-dimensional feature vector for each keypoint. SIFT is designed to be invariant to scale and rotation. Moreover, the algorithm offers decent robustness to noise, illumination gradients, and affine transformations.

<strong>SIFT in OpenCV </strong>

In OpenCV the SIFT algorithm is available only in the non-free module (OpenCV has both free and non-free modules). The algorithm has been patented by the creator but can be freely used for academic and research purposes. The non-free modules can be found in the <a href="https://github.com/opencv/opencv_contrib">opencv_contrib</a> package. You will first need to install this package, as shown below, and then you can use the SIFT module.

Initialize and activate the virtual environment (optional):

$ python3 -m venv env

$ source venv/bin/activate




Install the correct version of OpenCV and the contrib module:

$ pip install opencv-python==3.4.2.17

$ pip install opencv-contrib-python==3.4.2.17




<strong>Task 1 (0.5 mark): </strong>Compute the SIFT features of the given image.

<ol>

 <li>Extract SIFT features with default parameters and show the keypoints on the image.</li>

 <li>To achieve better visualization of the keypoints, reduce the number of keypoints. Hint: Vary the parameter <strong>contrastThreshold</strong> or <strong>nfeatures</strong> so that the number of keypoints becomes about 10% of all default keypoints.</li>

</ol>

Submit the images obtained in a) and b) and mention the approach you used in b).

<strong>Task 2 (1 mark):</strong> Change the scale of the image and recompute the SIFT features. a) Enlarge the given image by a scale percentage of 115.

<ol>

 <li>Extract the SIFT features and show the keypoints on the scaled image using the same parameter setting as for Task 1 (for the reduced number of keypoints).</li>

 <li>Inspect the keypoints visually: Are the keypoints of the scaled image roughly the same as those of the original image? What does this observation imply?</li>

 <li>Match the SIFT descriptors of the keypoints of the scaled image with those of the original image using the nearest-neighbour distance ratio method. Show the keypoints of the 5 best-matching descriptors on both the original and the scaled image.</li>

</ol>

Hint: Brute-force matching is available in OpenCV for feature matching.

Submit the images obtained in b) and d) and your answers to the questions in c).

<strong>Task 3 (1 mark):</strong> Rotate the image and recompute the SIFT features. a) Rotate the given image clockwise by 60 degrees.

<ol>

 <li>Extract the SIFT features and show the keypoints on the rotated image using the same parameter setting as for Task 1 (for the reduced number of keypoints).</li>

 <li>Inspect the keypoints visually: Are the keypoints of the rotated image roughly the same as those of the original image? What does this observation imply?</li>

 <li>Match the SIFT descriptors of the keypoints of the rotated image with those of the original image using the nearest-neighbour distance ratio method. Show the keypoints of the 5 best-matching descriptors on both the original and the rotated image.</li>

</ol>

Submit the images obtained in b) and d) and your answers to the questions in c).

<strong> </strong>