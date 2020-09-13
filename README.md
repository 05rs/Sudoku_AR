# Sudoku_AR

Sudoku Solver AR is an augmented reality Sudoku solver. It captures video using a camera, finds Sudoku puzzles in the photo, and then displays answers to those puzzles in such a way that they look like they are part of the original scene.
![Video](video)

## Technology Used

 - Tensoflow
 - OpenCv
 - Python

## Workflow
![workflow diagram](https://www.pyimagesearch.com/wp-content/uploads/2020/08/opencv_sudoku_puzzle_steps.png)


# STEPS 
 1. Input the Sudoku image.
![input_image](/media/2.jpg)

 2. Apply thresholding to image.
![thresh_image](media/3.png)

 3. Select the biggest contour with four corners and perform perspective transform.
![warped_image](media/4.png) 

 4. Divide the wrapped image into 81 cells, extract each cell in the warped image and chop it borders as it may contain some white pixels.  
![digit_image](media/5.png)
 
 5. Predict the number on cell using Neural Network, trained on CIFAR dataset, generate sudoku board and solve with py-sudoku library.


## Usage

`python3 main.py` 

## Features

-   Automatically Detects Sudoku Block
-  Fast Prediction

## To-DO

- Detect Sudoku Block in live video stream and solve
- Detect multiple sudoku board in a frame
- Add rotation robustness

