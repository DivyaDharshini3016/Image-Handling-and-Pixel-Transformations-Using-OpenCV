# Image-Handling-and-Pixel-Transformations-Using-OpenCV 

## AIM:
Write a Python program using OpenCV that performs the following tasks:

1) Read and Display an Image.  
2) Adjust the brightness of an image.  
3) Modify the image contrast.  
4) Generate a third image using bitwise operations.

## Software Required:
- Anaconda - Python 3.7
- Jupyter Notebook (for interactive development and execution)

## Algorithm:
### Step 1:
Load an image from your local directory and display it.

### Step 2:
Create a matrix of ones (with data type float64) to adjust brightness.

### Step 3:
Create brighter and darker images by adding and subtracting the matrix from the original image.  
Display the original, brighter, and darker images.

### Step 4:
Modify the image contrast by creating two higher contrast images using scaling factors of 1.1 and 1.2 (without overflow fix).  
Display the original, lower contrast, and higher contrast images.

### Step 5:
Split the image (boy.jpg) into B, G, R components and display the channels

## Program Developed By:
- **Name:** Divya Dharshini S 
- **Register Number:** 212224240039

  ### Ex. No. 01
```
import cv2
import matplotlib.pyplot as plt
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)

plt.imshow(img_rgb, cmap='viridis')  # You can change 'viridis' to another cmap or use None for RGB images
plt.title("Original Image")
plt.axis('off')  # Removes axis ticks and labels
plt.show()
image = cv2.imread('Qno. 1.jpg') 
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape
line_img = cv2.line(img_rgb, (0, 0), (768, 600), (255, 0, 0), 2) # cv2.line(image, start_point, end_point, color, thickness)
plt.imshow(line_img, cmap='viridis')  
plt.title("Image with Line")
plt.axis('off')  
plt.show()

image = cv2.imread('Qno. 1.jpg') 

img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape
circle_img = cv2.circle(img_rgb,(400,300),150,(255,0,0),10) # cv2.circle(image, center, radius, color, thickness)
plt.imshow(circle_img, cmap='viridis')  
plt.title("Image with Circle")
plt.axis('off')  
plt.show()

image = cv2.imread('Qno. 1.jpg') 

img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img.shape

rectangle_img = cv2.rectangle(img_rgb, (0, 0), (768, 600), (0, 0, 255), 10)  # cv2.rectangle(image, start_point, end_point, color, thickness)

plt.imshow(rectangle_img, cmap='viridis')  
plt.title("Image with Rectangle")
plt.axis('off')  
plt.show()

image = cv2.imread('Qno. 1.jpg') 

img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB) 

text_img = cv2.putText(img_rgb, "OpenCV Drawing", (10, 30), cv2.FONT_HERSHEY_SIMPLEX, 1, (255, 255, 255), 10)  ## cv2.putText(image, text, position, font, font_scale, color, thickness)

plt.imshow(text_img, cmap='viridis')  
plt.title("Image with Text")
plt.axis('off')  
plt.show()

image = cv2.imread('Qno. 1.jpg') 
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)

plt.imshow(image_rgb)
plt.title("Original RGB Image")
plt.axis("off")

image_hsv = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2HSV)

plt.imshow(image_hsv)
plt.title("HSV Image")
plt.axis("off")

image_gray = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2GRAY)

plt.imshow(image_gray, cmap='gray')
plt.title("Grayscale Image")
plt.axis("off")

image_ycrcb = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2YCrCb)

plt.imshow(image_ycrcb)
plt.title("YCrCb Image")
plt.axis("off")

image_hsv_to_rgb = cv2.cvtColor(image_hsv, cv2.COLOR_HSV2RGB)
plt.imshow(image_hsv_to_rgb)
plt.title("HSV to RGB Image")
plt.axis("off")

image[100:400, 50:350] = [255, 0 , 255]  # Rows: 200-499, Columns: 200-499

image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)

plt.imshow(image_rgb)
plt.title("Image with 300x300 White Block")
plt.axis("off")
plt.show()

image = cv2.imread('Qno. 1.jpg') 
image.shape

resized_image = cv2.resize(image, (768 // 2, 600 // 2))  # (new_width, new_height)

resized_image_rgb = cv2.cvtColor(resized_image, cv2.COLOR_BGR2RGB)
resized_image_rgb.shape

plt.imshow(resized_image_rgb)
plt.title("Resized Image (Half Size)")
plt.axis("off")
plt.show()

image = cv2.imread('Qno. 1.jpg') 
image.shape

roi = image[50:350, 50:350]  # Rows: 50-349, Columns: 50-349

roi_rgb = cv2.cvtColor(roi, cv2.COLOR_BGR2RGB)

plt.imshow(roi_rgb)
plt.title("Cropped Region of Interest (ROI)")
plt.axis("off")
plt.show()

image = cv2.imread('Qno. 1.jpg') 

flipped_horizontally = cv2.flip(image, 1)

flipped_horizontally_rgb = cv2.cvtColor(flipped_horizontally, cv2.COLOR_BGR2RGB)

plt.imshow(flipped_horizontally_rgb)
plt.title("Flipped Horizontally")
plt.axis("off")

flipped_vertically = cv2.flip(image, 0)

flipped_vertically_rgb = cv2.cvtColor(flipped_vertically, cv2.COLOR_BGR2RGB)

plt.imshow(flipped_vertically_rgb)
plt.title("Flipped Vertically")
plt.axis("off")
```

## Output:
- **i)** Read and Display an Image.
- **ii)** Adjust Image Brightness.  
- **iii)** Modify Image Contrast.  
- **iv)** Generate Third Image Using Bitwise Operations.

<img width="435" height="537" alt="image" src="https://github.com/user-attachments/assets/8889172a-c072-4137-8e08-1ab0826f86f8" />

<img width="572" height="537" alt="image" src="https://github.com/user-attachments/assets/99343cd3-31a4-4438-9078-c73710056d4f" />

<img width="580" height="527" alt="image" src="https://github.com/user-attachments/assets/8216ecbf-0a25-4b71-bf4d-031592e4c99d" />

<img width="597" height="527" alt="image" src="https://github.com/user-attachments/assets/21e8057c-5488-43c0-866f-88391913199c" />

<img width="611" height="540" alt="image" src="https://github.com/user-attachments/assets/e5fbbabb-e889-4210-bd48-8c0d973dc3af" />

<img width="787" height="563" alt="image" src="https://github.com/user-attachments/assets/22e3ac52-eac5-4f0d-9f49-170cbe7e0a16" />

<img width="757" height="525" alt="image" src="https://github.com/user-attachments/assets/bfd35472-7153-4a3e-9703-a5e7b43d4a6c" />

<img width="792" height="560" alt="image" src="https://github.com/user-attachments/assets/550fa8ab-d4ff-456c-ba66-d9ee4d96e216" />

<img width="737" height="547" alt="image" src="https://github.com/user-attachments/assets/b0c64aac-f039-44b0-a6d4-be31a9a697d4" />

<img width="602" height="527" alt="image" src="https://github.com/user-attachments/assets/b7202d5b-e3b1-4f08-8e70-4615a30a6e35" />

<img width="781" height="532" alt="image" src="https://github.com/user-attachments/assets/c449b138-b69e-49ed-a7ab-825558f499df" />

<img width="705" height="525" alt="image" src="https://github.com/user-attachments/assets/b52d2112-f7b5-4875-b53d-3074eb49ea9e" />

<img width="755" height="525" alt="image" src="https://github.com/user-attachments/assets/caed1d74-065f-4f96-9ea2-992486a54f20" />

<img width="717" height="541" alt="image" src="https://github.com/user-attachments/assets/e463dd46-298a-4ee6-a55d-f9ad30ff7855" />


## Result:
Thus, the images were read, displayed, brightness and contrast adjustments were made, and bitwise operations were performed successfully using the Python program.


