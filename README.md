# AI Workbench Image Style Transfer

This project demonstrates image style transfer using NVIDIA AI Workbench. It allows users to upload a content image and a style image, and then applies the style of the latter to the former using a pre-trained neural network.

## Prerequisites

NVIDIA AI Workbench
NVIDIA GPU with CUDA support

## Getting Started

Clone this repository:
git clone https://github.com/HectorTa1989/AIWorkbench-ImageStyleTransfer.git

Navigate to the project directory:
cd AIWorkbench-ImageStyleTransfer

Build the Docker image:
docker build -t ai-workbench-style-transfer .

Run the container:
docker run --gpus all -p 8000:8000 ai-workbench-style-transfer

Open a web browser and navigate to http://localhost:8000 to access the web interface.

## Usage

Upload a content image and a style image using the web interface.
Click the "Transfer Style" button to process the images.
The resulting stylized image will be displayed on the page.

## Project Structure

• app/: Contains the main application code 
   
      •	main.py: FastAPI application entry point
   
      •	model.py: Style transfer model implementation
   
      •	image_processor.py: Image processing utilities
   
      •	api.py: API endpoints for handling requests

• static/: Contains the HTML file for the web interface 

• Dockerfile: Defines the container environment 

• requirements.txt: Lists Python dependencies

## Restrictions

This project uses a pre-trained VGG19 model for style transfer.
The container image is based on NVIDIA's PyTorch container (nvcr.io/nvidia/pytorch:23.08-py3).
GPU acceleration is required for optimal performance.

## License
This project is licensed under the MIT License - see the LICENSE file for details. You need my permission for commercialization purpose.
