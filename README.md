# Sportsperson-Face-Detection-HaarCascade-Wavelet-Transform
In this project, I took 5 of the most reknown sports celebraty, Roger Faderar, Luis Hamilton, Maria Sharapova, football legend Leonel Messi and world's best cricket alrounder Shakib Al Hasan, who is my favorite cricketer and also from my own country. The first step in our pre-processing pipeline is to detect faces from an image. Once face is detected, we will detect eyes, if two eyes are detected then only we keep that image otherwise discard it. I used openCV's haar cascade to identify faces and two eyes.<Br><Br>
  In the 2nd step of preprocessing, I used wavelet transofmation of the image also as a feature for training the model. Wavelet function can detect edges of faces, nose and eyes clearly. I will use transformed image as well as the raw image to train the model.<Br><Br>
  After creating the function I ran over all of the directories to get all of the cropped images of the faces of these sportpersons with wavelet transformed images. If two eyes are not visible the function will discard those images. Later we manually varified if the images are of the right persons and deleted some unnecessary images.<Br><Br>
  I used SVM model initially and trainded the model. Then I used gridSearchCV for hyperparameter tuning to try out different models with different parameters to find the best fined tuned parameters for the models. I found that logistic regression with the parameter logisticreggression_C: 1 gives the best accuracy over 83 percent. Confusion  matrix  is  used  with  seaborn  visualization  to  get  an  understanding  of classification  errors  for  each  of  the  classes. Lastly, I saved the model weights in a pickle file and also the numerical values assigned to each players in a json file.<Br><Br>
  Technologies Used in this project:<Br>
  1. Python
  2. Numpy and OpenCV for data cleaning
  3. pywt for transforming wavelet images
  4. Matplotlib and Seaborn for data visualization
  5. Sklearn for model building and greedSearchCV
  6. Jupyter notebook and Google Colab for IDE
