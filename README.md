# On-the-Fly Image Resize for AWS Lambda

Creates image thumbnails from your S3 bucket on-the-fly using AWS Lambda & API Gateway. It reads the source image from a S3 bucket as stream, pipes it to sharp, then writes the resized version as a stream back to S3 bucket. It uses Node.js streams under the hood to prevent loading large amount of data in the Lambda function's memory and Sharp, a high performance Node.js module for image processing (https://sharp.pixelplumbing.com/)
