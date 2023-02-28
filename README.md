# challenge_2023
#import libiraries
import numpy
import matplotlib.pyplot as plt
from PIL import Image
import PIL

#load the data from a compressed file in the specified path
b = numpy.load('/Users/mohamedashraf/Downloads/chestmnist.npz')

#print the name of the files in the compressed file
print(b.files)

#access the second image in the 'train_images' array and store it in a variable img
img = b['train_images'][1]

#display the image using a grayscale colormap
plt.imshow(img, cmap='gray')

#save the plot as image file with the specified name and format
plt.savefig("Mohamed_Abdelrazek_1.png")

#display the plot
plt.show()

#access the second image in the 'train_images' array and store it in a variable img
img = b['train_images'][1]

# cmap = grey sets the image to grayscale Interpolation calculates what the color or value of a pixel 
#“should” be, according to different mathematical schemes. Setting it to bicubic means that the image will 
#get blurred instead of getting pixelated
plt.imshow(img, cmap='gray',interpolation = 'BICUBIC')

#save the plot as image file with the specified name and format
plt.savefig("Mohamed_Abdelrazek_3A.png")

#display the plot
plt.show()
#intvert the color of the image by subtracting each pixel value form 255 (maximum intensity value)
img_inverted = 255 - img

#display the image using a grayscale colormap
plt.imshow(img_inverted, cmap='gray')

#save the plot as image file with the specified name and format
plt.savefig("Mohamed_Abdelrazek_2.png")

#display the plot
plt.show()

# Invert the black and white pixels
img_inverted = 255 - img

#display the image using a grayscale colormap and the image get blurred instead of getting pixelated
plt.imshow(img_inverted, cmap='gray', interpolation='BICUBIC')

#save the plot as image file with the specified name and format
plt.savefig("Mohamed_Abdelrazek_3B.png")

#display the plot
plt.show()
