import cv2
import numpy as np
import os

path2='/media/aniket/D044BBC744BBAF1A/Users/user/test-images2'
for item in os.listdir(path2):
    f2 = '//media//aniket//D044BBC744BBAF1A//Users//user//test-images2//' + item
    os.remove(f2)


path='/media/aniket/D044BBC744BBAF1A/Users/user/test-images1'
for filename in os.listdir(path):
    f = '//media//aniket//D044BBC744BBAF1A//Users//user//test-images1//' + filename

i = 1
img = cv2.imread(f)
#crop_img = img[100:100+250, 10:10+900]
grayscaled = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
#th = cv2.adaptiveThreshold(grayscaled, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C, cv2.THRESH_BINARY, 115, 1)
retval2,threshold2 = cv2.threshold(grayscaled,125,255,cv2.THRESH_BINARY)
threshold3 = 255 - threshold2
cv2.imshow('original',img)
cv2.imshow('Otsu threshold',threshold3)
path1 = '/media/aniket/D044BBC744BBAF1A/Users/user/test-images2'
cv2.imwrite(os.path.join(path1, str(i) + '.png'), threshold3)
#cv2.waitKey(0)
#cv2.destroyAllWindows()
