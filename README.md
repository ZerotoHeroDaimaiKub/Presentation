# Image Crop/Edge-Detection Application
## Overview

Our program is an image processing application that allows users to perform various operations such as edge detection and image cropping. It provides a graphical user interface (GUI) built using JavaFX, making it intuitive and easy to use for various image manipulation tasks.

The project is modular, with dedicated components for handling different image processing features. It implements several edge detection algorithms, offers customizable cropping functionality and can do bulk files.

![main](https://i.imgur.com/jJZwwXU.png)
![edge](https://i.imgur.com/AxZZoL8.png)
![crop](https://i.imgur.com/7dmd0sY.png)

---

## Features

### 1. **Edge Detection**
   - Supports multiple edge detection algorithms:
     - **Sobel Edge Detector**
     - **Laplacian Edge Detector**
     - **Roberts Cross Edge Detector**
   - Users can apply these detectors to highlight the edges in images for various applications such as feature extraction and image analysis.

### 2. **Image Cropping**
   - Resizable cropping tools enable users to select and crop regions of interest within an image.

### 3. **File Type Support**
   - The application supports the following file types:
     - **Single Image Files**: `.jpg`, `.png`
     - **Multiple Image Files**: Batch processing of `.jpg`, `.png`
     - **Single Archive Files**: `.zip` archives containing image files

### 4. **Drag-and-Drop File Input**
   - Users can **drag-and-drop** single or multiple files, as well as `.zip` archives, directly into the application for processing.

### 5. **Batch Processing**
   - The application supports **batch processing** of multiple images at once, including extraction and processing of images from `.zip` archives.
   
   - It uses **multiprocessing** or **multithreading** to handle large batches of images, ensuring performance improvements by parallelizing tasks.

### 6. **User Interface**
   - Provides a **clear and intuitive user interface**, ensuring users can navigate and use the application efficiently.

### 7. **Error Handling**
   - Handles potential runtime errors gracefully by providing **informative messages** to the user. This ensures that users are aware of any issues that may occur during the image processing workflow.

## File Structure

```
SEProject20/
│
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── seproject/
│   │   │       ├── controller/       # Controllers for handling user interactions
│   │   │       ├── exceptions/       # Custom exception classes
│   │   │       ├── model/            # Image processing logic (edge detectors, crop models, etc.)
│   │   │       └── view/             # FXML files and styles for UI
│   │   └── resources/
│   │       └── view/                 # UI FXML files and stylesheets (e.g., crop.css, edge.css)
│   └── test/                         # Unit tests for controllers and models
├── target/                           # Compiled files
│
├── pom.xml                           # Maven project configuration
└── README.md                         # Project documentation (you're reading this)
```

---

## Usage

1. Launch the application and load an image using the file chooser.
2. Navigate through the tabs to select the operation:
   - Use the **Edge Detector** tab to apply one of the edge detection algorithms.
   - Use the **Crop Tool** tab to resize and crop portions of the image.

Edge Detection Tab Buttons:

    Select Edge Detection Algorithm:
    A dropdown menu that allows users to choose the edge detection algorithm they want to apply. Available options might include Sobel, Laplacian, or Roberts Cross edge detectors.

    Clear:
    Removes all applied edge detection effects from the current image, reverting it to its original state before the edge detection was applied.

    Reset:
    Restores the image to its original state, discarding all changes, including edge detection, cropping, and other modifications.

    Detect Edges:
    Applies the selected edge detection algorithm to the loaded image. Once pressed, the edges of the image will be highlighted based on the chosen algorithm.

    Detect All:
    Applies edge detection to all loaded images (in case of batch processing). It automatically processes each image with the selected algorithm.

    Save:
    Saves the current processed image (with edges detected) to the local directory.

    Save All:
    Saves all processed images in batch mode to a user-defined location. Each image will be saved with the applied edge detection algorithm.

Crop Tool Tab Buttons:

    Start Crop:
    Activates the cropping tool, allowing users to select the area of the image they want to crop. A resizable rectangle will appear on the image for adjusting the crop region.

    Confirm Crop:
    After selecting the crop area, pressing this button confirms and performs the crop operation on the selected image area.

    Batch Process:
    Allows for batch cropping of multiple images. This function processes all loaded images, cropping each according to the defined crop region.

    Reset Image:
    Resets the current image to its original state, discarding any applied crop or modifications.

    Save Image:
    Saves the currently cropped image to a user-defined location.

    Save All:
    Saves all cropped images from a batch process into a selected directory.

    Clear:
    Removes any crop selection from the current image, resetting it to the state before the crop was initiated.

    ESC Key:
    Cancel Operation

    Left Arrow / Right Arrow:
    These buttons are used to navigate between loaded images in case multiple images have been loaded for batch processing. Use these buttons to move through the images and apply individual cropping or processing.

3. Save the processed image to your local directory.

