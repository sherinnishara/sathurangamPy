# ***SathurangamPy User Guidance***


Sathurangam is a python package designed to streamline OpenCV tasks by reducing complex operations to single-line solutions, enhancing code readability and efficiency.

This documentation explains how to use each function in the module step by step, including its required inputs and outputs with examples.



## **Disclaimer**

Below functions are require

 `cv2.imshow()` and others 


---

## 1. Display Image
- **Function:** `display_image(filename)`
- **Description:** Displays an image in a new window.
- **Parameters:**
  - `filename` (str): Path to the image file.
- **Steps to Use:**
  1. Set the file path for the image.
  2. Call the function with the image path.
- **Example:**
  ```python
  display_image('path/to/image.jpg')
- **Usage:**
  ```python
   import sathurangamPy as sp 
   import import cv2

   path = 'img.png'
   image = display_image(path)

   cv2.imshow(image)
   cv2.waitKey(0)
   cv2.destroyAllWindows()

---


## 2. Image to Grayscale
- **Function:** `grayscale_converter(path)`
- **Description:** Converts the input image to grayscale.
- **Parameters:**
  - `path` (str): Path to the image file.
- **Steps to Use:**
  1. Set the file path for the image.
  2. Call the function with the image path.
- **Example:**
  ```python
  display_image(img.png)

---



## 3. Resize Image
- **Function:** `resize_image(path, width, height)`
- **Description:** Resizes the input image to the specified size.
- **Parameters:**
  - `path` (str): File path of the image
     `width` (int): New width of the image.
      `height` (int): New height of the image.
- **Example:**
  ```python
  resized_image = resize_image(path, 400, 300)

---


## 4. Rotate Image
- **Function:** `rotate_image(filename, angle)`
- **Description:** Rotates the image by a given angle in degrees.
- **Parameters:**
  - `filename` (str): Path to the image file.
  - `angle` (float): Angle in degrees to rotate the image.
- **Usage Example:**
  ```python
  rotated_image = rotate_image(path, 45)

---


## 5. Blur Image
- **Function:** `blur_image(filename, kernel)`
- **Description:** Applies a Gaussian blur to the image.
- **Parameters:**
  - `filename` (str): Path to the image file.
  - `kernel` (int): Size of the kernel (must be odd).
- **Usage Example:**
  ```python
  blurred_image = blur_image(path, 5)
  ```

---


## 6. Crop Image
- **Function:** `crop_image(filename, x, y, width, height)`
- **Description:** Crops the image to a specific rectangular region.
- **Parameters:**
  - `filename` (str): Path to the image file.
  - `x` (int): X-coordinate of the top-left corner.
  - `y` (int): Y-coordinate of the top-left corner.
  - `width` (int): Width of the crop region.
  - `height` (int): Height of the crop region.
- **Usage Example:**
  ```python
  cropped_image = crop_image(path, 50, 50, 200, 200)
  ```

---


## 7. Canny Edge Detection
- **Function:** `canny_edge(filename, kernel, low_threshold, high_threshold)`
- **Description:** Detects edges in the image using the Canny edge detection algorithm.
- **Parameters:**
  - `filename` (str): Path to the image file.
  - `kernel` (int): Size of the kernel for blurring (must be odd).
  - `low_threshold` (int): Lower threshold for edge detection.
  - `high_threshold` (int): Upper threshold for edge detection.
- **Usage Example:**
  ```python
  edges = canny_edge(path, 3, 50, 150)
  ```

---


## 8. Dilate Image
- **Function:** `dilate_image(filename, kernel, low_threshold, high_threshold, iterations)`
- **Description:** Applies dilation to the edges detected using the Canny edge detector after Gaussian blurring.
- **Parameters:**
  - `filename` (str): Path to the image file.
  - `kernel` (int): Size of the kernel (must be odd).
  - `low_threshold` (int): Lower threshold for Canny edge detection.
  - `high_threshold` (int): Upper threshold for Canny edge detection.
  - `iterations` (int): Number of iterations for dilation.
- **Usage Example:**
  ```python
  dilated_image = dilate_image(path, 
  5, 100, 200, 3)

---


## 9. Erode Image
- **Function:** `erode_image(filename, kernel, low_threshold, high_threshold, dilate_iterations, erode_iterations)`
- **Description:** Applies erosion to a dilated image after detecting edges using the Canny edge detector.
- **Parameters:**
  - `filename` (str): Path to the image file.
  - `kernel` (int): Size of the kernel (must be odd).
  - `low_threshold` (int): Lower threshold for Canny edge detection.
  - `high_threshold` (int): Upper threshold for Canny edge detection.
  - `dilate_iterations` (int): Number of iterations for dilation.
  - `erode_iterations` (int): Number of iterations for erosion.
- **Usage Example:**
  ```python
  eroded_image = erode_image(path, 
  5, 100, 200, 2, 2)

---


## 10. Threshold Image
- **Function:** `threshold_image(filename, threshold)`
- **Description:** Applies a binary threshold to an image after converting it to grayscale.
- **Parameters:**
  - `filename` (str): Path to the image file.
  - `threshold` (int): Threshold value (0-255) for binarization.
- **Usage Example:**
  ```python
  thresholded_image = 
  threshold_image(path, 128)

---


## 11. Count Contours
- **Function:** `contour_count(filename, kernel, low_threshold, high_threshold)`
- **Description:** Counts the number of contours found in the image after edge detection using Canny.
- **Parameters:**
  - `filename` (str): Path to the image file.
  - `kernel` (int): Size of the kernel (must be odd).
  - `low_threshold` (int): Lower threshold for Canny edge detection.
  - `high_threshold` (int): Upper threshold for Canny edge detection.
- **Usage Example:**
  ```python
    contour_count(path, 5, 100, 200)

---


## 12. Draw Contours
- **Function:** `draw_contour(filename, kernel, low_threshold, high_threshold, thickness, color=()*3)`
- **Description:** Draws all contours found in the image after edge detection using Canny. The contours are drawn on a blank canvas.
- **Parameters:**
  - `filename` (str): Path to the image file.
  - `kernel` (int): Size of the kernel for Gaussian blur (must be odd).
  - `low_threshold` (int): Lower threshold for Canny edge detection.
  - `high_threshold` (int): Upper threshold for Canny edge detection.
  - `thickness` (int): Thickness of the contour lines.
  - `color` (tuple): Color for the contours, default is `(0, 0, 255)` (red).
- **Usage Example:**
  ```python
  contour_image = 
  draw_contour(path, 5, 100, 200, 2, 
  (0, 255, 0))

---


## 13. Draw Specific Contour
- **Function:** `draw_specific_contour(filename, kernel, low_threshold, high_threshold, contourIdx, thickness, color=()*3)`
- **Description:** Draws a specific contour based on the index `contourIdx` from the contours detected in the image.
- **Parameters:**
  - `filename` (str): Path to the image file.
  - `kernel` (int): Size of the kernel for Gaussian blur (must be odd).
  - `low_threshold` (int): Lower threshold for Canny edge detection.
  - `high_threshold` (int): Upper threshold for Canny edge detection.
  - `contourIdx` (int): Index of the contour to be drawn.
  - `thickness` (int): Thickness of the contour line.
  - `color` (tuple, optional): Color for the contour, default is `(0, 0, 255)` (red).
- **Usage Example:**
  ```python
  specific_contour_image = 
  draw_specific_contour(path, 5, 100, 
  200, 0, 2, (255, 0, 0))

---


## 14. Draw Blank Image
- **Function:** `draw_blank_image(height, width)`
- **Description:** Creates a blank grayscale image with specified dimensions.
- **Parameters:**
  - `height` (int): Height of the image.
  - `width` (int): Width of the image.
- **Returns:** A blank grayscale image (array of zeros).
- **Usage Example:**
  ```python
  blank_image = 
  draw_blank_image(500, 500)

---


## 15. Draw Color Image
- **Function:** `draw_color_image(height, width, color=()*3)`
- **Description:** Creates a blank color image with specified dimensions and fills it with a specified color.
- **Parameters:**
  - `height` (int): Height of the image.
  - `width` (int): Width of the image.
  - `color` (tuple, optional): Color to fill the image with (default is `(0, 0, 0)` for black).
- **Returns:** A color image filled with the specified color.
- **Usage Example:**
  ```python
  color_image = draw_color_image(500, 500, (255, 0, 0))

---


## 16. Draw Rectangle 
- **Function:**
`draw_rectangle(filename, x, y, width, height, color, thickness)`
- **Description:** Draws a rectangle on the image.
- **Parameters:**
  - `filename` (str): Path to the image file.
  - `x` (int): X-coordinate of the top-left corner.
  - `y` (int): Y-coordinate of the top-left corner.
  - `width` (int): Width of the rectangle.
  - `height` (int): Height of the rectangle.
  - `color` (tuple): Color of the rectangle (B, G, R).
  - `thickness` (int): Thickness of the rectangle border.
- **Usage Example:**
  ```python
  draw_rectangle(path, 50, 50, 100, 50, (0, 255, 0), 2)

---


## 17. Draw Circle
- **Function:** `draw_circle(filename, thickness, radius, center_point=()*2, color=()*3)`
- **Description:** Draws a circle on an image at the specified location with a given radius and color.
- **Parameters:**
  - `filename` (str): Path to the image file.
  - `thickness` (int): Thickness of the circle's border. If set to `-1`, the circle will be filled.
  - `radius` (int): Radius of the circle.
  - `center_point` (tuple): Coordinates of the circle's center (default is `(0, 0)`).
  - `color` (tuple): Color of the circle in RGB format (default is `(0, 0, 0)`).
- **Returns:** The image with the drawn circle.
- **Example:**
  ```python
  image_with_circle = 
  draw_circle(path, 2, 50, (100, 100), 
  (255, 0, 0)) 

---


## 18. Draw Line on image
- **Function:** `draw_line(filename, thickness, start_point=()*2, end_point=()*2, color=()*3)`
- **Description:** Draws a line on an image from a start point to an end point with the given thickness and color.
- **Parameters:**
  - `filename` (str): Path to the image file.
  - `thickness` (int): Thickness of the line.
  - `start_point` (tuple, optional): Coordinates of the start point (default is `(0, 0)`).
  - `end_point` (tuple, optional): Coordinates of the end point (default is `(0, 0)`).
  - `color` (tuple, optional): Color of the line in RGB format (default is `(0, 0, 0)`).
- **Returns:** The image with the drawn line.
- **Usage Example:**
  ```python
  image_with_line = draw_line(path, 2, (50, 50), (150, 150), (0, 255, 0)) 

---


## 19. Put Text on image
- **Function:** `draw_text(filename, text, fontScale, position=()*2, color=()*3)`
- **Description:** Adds text to an image at a specified position with a given font size and color.
- **Parameters:**
  - `filename` (str): Path to the image file.
  - `text` (str): The text to be displayed.
  - `fontScale` (float): The size of the font.
  - `position` (tuple, optional): Coordinates of the text position (default is `(0, 0)`).
  - `color` (tuple, optional): Color of the text in RGB format (default is `(0, 0, 0)`).
- **Returns:** The image with the added text.
- **Usage Example:**
  ```python
  image_with_text = draw_text(path, "Hello", 1, (100, 100), (255, 255, 255)) 

---


## 20. Draw Custom Text
- **Function:** `draw_custom_text(filename, text, fontstyle, fontScale, position=()*2, color=()*3)`
- **Description:** Adds text to an image at a specified position with a custom font style, font size, and color.
- **Parameters:**
  - `filename` (str): Path to the image file.
  - `text` (str): The text to be displayed.
  - `fontstyle` (int): The font style to be used (e.g., `cv2.FONT_HERSHECOMPLEX`).
  - `fontScale` (float): The scale of the font.
  - `position` (tuple, optional): Coordinates of the text position (default is `(0, 0)`).
  - `color` (tuple, optional): Color of the text in RGB format (default is `(0, 0, 0)`).
- **Usage Example:**
  ```python
  image_with_custom_text = draw_custom_text(path, "Custom Text", cv2.FONT_HERSHEY_SIMPLEX, 1, (100, 100), (255, 0, 0))  

---


## 21. Display Video(including live)
- **Function:** `read_video(filename)`
 - **Description:** read and displays a video frame by frame. The video will stop if the user presses 'q'.if filename = 0 it stream a live video capture from webcam
- **Parameters:**
  - `filename` (str or int): Path to the video file.(if 0 gives live capture from webcam) 
- **Usage Example:**
  ```python
  video = read_video("video.mp4")
  read_ video(0) #webcam open
  #if not works use print(video)

---


## 22.Human Face detection from image
- **Function:** -`detect_face(filename, haarfile, scaleFactor, minNeighbors)`
- **Description:** Detects faces in the given image using a Haar Cascade classifier and draws rectangles around the detected faces.
#### Arguments:
- `filename`: The path to the image file.
- `haarfile`: The path to the Haar cascade XML file used for face detection.
- `scaleFactor` (float): Parameter specifying how much the image size is reduced at each image scale.
- `minNeighbors` (int): Parameter specifying how many neighbors each candidate rectangle should have to retain it.
- **Usage Example:**
```python
  path = 'img.png'
  haar_f ='haar cascade.xml'
  face = detect_face(path, haar_f, 0.1, 
  3)
  print(face)
```

---


## 23.Save Images(Face detected) to a Dataset including live capture 
- **Function:** - `save_face(videocap, datasets, sub_data, haar_file, total)`
- **Description:** faces from a webcam feed, resizes them, and saves them in the specified directory.

#### Arguments:
- `videocap`: The video capture source (e.g., camera or video file).
- `datasets`: The root directory for saving the dataset.
- `sub_data`: The folder name where the captured faces will be stored.
- `haar_file`: The path to the Haar cascade XML file used for face detection.
- `total`: The total number of images to be captured.

- **Usage Example:**
```python
datasets = 'main_folder'
sub_data = 'sub_folder'
haar_f ='haar cascade.xml'

data = save_face(0, datasets, sub_data, haar_file, 50)
print(data)
```

---


## Setup and Requirements:
- **Libraries**: `cv2` (OpenCV), `numpy`.
- **Dataset/Files**: Image/video paths, Haar cascade XML files for face detection.


---


## Connect with Us:

[![GitHub](https://img.shields.io/badge/-GitHub-000000?style=flat&logo=github&logoColor=white&circle=true)](sherinnishara ) 

[![LinkedIn](https://img.shields.io/badge/-LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white&circle=true)](sherinnishara) 


>"made by ❤️ sherin"