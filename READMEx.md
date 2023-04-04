# File Metadata Viewer API Microservice

This is a simple Node.js API microservice that allows users to upload a file and retrieve its metadata, including the file name, MIME type, and size.

The API is built using the following technologies:

- Express.js for handling HTTP requests and routing
- Multer middleware for handling file uploads
- CORS middleware for enabling cross-origin resource sharing
- dotenv module for loading environment variables

## API Endpoints
The API has one endpoint:

`POST /api/fileanalyse`

This endpoint accepts a file upload and returns the file metadata as a JSON response. The file should be uploaded using the upfile field name in a multipart/form-data request.

#### Request Body

| Field | Type | Required | Description |
| ---- | ----- | -------- | ----------- |
| upfile | File | Yes | The file to be uploaded |

#### Response Body
If the file is uploaded successfully, the API will return a JSON response with the following fields:

|Field|	Type|	Description|
|-----|-----|--------------|
|name|	String|	The original name of the uploaded file.|
|type|	String|	The MIME type of the uploaded file.|
|size|	Number|	The size of the uploaded file in bytes.|

If no file is uploaded or an error occurs during the upload, the API will return a JSON response with a 404 status code and a message indicating that a file must be uploaded.
