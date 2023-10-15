# Watermark Remover

This project provides a set of tools to detect and remove watermarks from images. It makes use of various image processing techniques and methods to identify the watermark and then inpaints the region to remove the watermark.

## Features

- Detects watermarks based on image patterns and edges.
- Uses adaptive thresholding, local binary patterns, and other image processing techniques.
- Processes images in batches for efficiency.
- Inpaints the watermark region to produce a clean image.

## Requirements

The project makes use of several libraries including:

- OpenCV (`cv2`)
- NumPy
- `glob` for file operations
- `asyncio` for asynchronous operations
- `tqdm` for progress bars
- `concurrent.futures` for parallel execution
- `skimage` for additional image processing techniques

## Getting Started

1. Ensure you have all the required libraries installed.
2. Place the images you want to process in the `DATA/3.IMAGES` directory.
3. Run the main script to process the images and remove watermarks.

## Usage

```python
from MainExecutor import MainExecutor

# Process all images
MainExecutor.run()

# Process only the first N images
# MainExecutor.run(num_images_to_process=N)
```

## Directory Structure

- `DATA/3.IMAGES`: Place your images here for processing.
- `DATA/0.DONE`: Processed images without watermarks are saved here.
- `DATA/1.MARK`: Watermark masks for different image dimensions are saved here.
- `samples`: Intermediate masks generated during watermark detection are saved here for reference.

## Logging

The script logs its operations in `watermark_removal.log`.

## Contributing

If you have suggestions, bug reports, or enhancements, feel free to open an issue or send a pull request.

## License

This project is open-source. Please ensure you mention the original creator when using or adapting this project for your needs.
