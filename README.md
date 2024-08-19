# PHP-Image-Optimizer-Resizer-Service
A robust image optimizer, cache, and delivery service. Users can upload and delete images, and request images with dynamic resizing and compression through configurable parameters built using php and mysql.

## Image Optimizer & Resizer Service
This project provides an image optimization, caching, and delivery solution. It includes two main components:

User-Facing Endpoint Application: Allows users to upload and delete images. It also serves images based on request parameters, handling resizing and compression efficiently.

Resizer Application: Processes image URLs and resizing parameters to generate and store resized images. If a requested image configuration does not exist, it performs the resize operation, stores the result in object storage, and updates the database.


## Key Features:

Upload & Delete: Manage your images through user-friendly endpoints.

Dynamic Image Delivery: Request images with specified parameters (quality, format, width, height) and receive the optimized version.

Efficient Resizing: The service checks if a resized version of an image exists; if not, it creates and stores it for future use.

This service ensures that images are efficiently cached and delivered, minimizing processing time and storage usage.
