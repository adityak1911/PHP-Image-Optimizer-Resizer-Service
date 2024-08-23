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


## Tech Stack used
1. PHP 8.2
2. Redis
3. Postgres
4. DigitalOcean Object Storage



## Getting Started
The request will be sent to url as below
```
https://image-optimizer.com/folder/index.php?image_url=https://digital-ocean-bucket.com/image-path.jpg?quality=low
```

- `image-optimizer.com` is the domain or IP address where the resizer service is hosted.
- `/folder` is the directory where the resizer code is located.



### Parameters

### 1. `quality` (required)

- **Description**: Determines the quality of the returned image.
- **Accepted Values**:
  - `low` - Returns the image at **144p** resolution.
  - `medium` - Returns the image at **480p** resolution.
  - `high` - Returns the image at **1080p** resolution.
- **Example**: `quality=medium`

### 2. `image_url` (required)

- **Description**: The URL of the image to be processed.
- **Accepted Values**: A valid URL pointing to an image file.
- **Example**: `image_url=https://example.com/image.jpg`

  
## Usage

To use this service, you need to provide the `quality` and `image_url` parameters. Below is an example of a typical request.

### Example Request

```http
GET /index.php?quality=high&image_url=https://example.com/sample-image.jpg
```


