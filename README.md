**Introduction**
This project describes the development of a robust serverless web application , leveraging a variety of AWS services to enhance functionality and streamline deployment. The primary resources employed include:

**AWS SAM (Serverless Application Model):** Utilized for defining and deploying serverless applications, SAM simplifies the process of working with AWS CloudFormation templates. In this project, SAM orchestrates AWS Lambda functions, Amazon API Gateway, DynamoDB tables, S3 buckets, and other resources.

**AWS Lambda:** The backbone of the serverless architecture, Lambda functions are employed for various tasks, such as authentication (MyAuthFunction), task retrieval, creation, and deletion (GetTasksFunction, GetTaskByIdFunction, DeleteTaskFunction), image analysis using Rekognition (DetectLabelsFunction), and more.

**Amazon API Gateway:** This service facilitates the creation, deployment, and management of APIs. In this project, API Gateway is configured to handle authentication through a Lambda authorizer (MyLambdaTokenAuthorizer) and exposes endpoints for tasks retrieval, creation, and deletion.

**AWS Amplify Console:** Amplify Console is employed for continuous deployment and hosting of the web application's static resources, providing a seamless and efficient deployment workflow.

**Amazon S3:** S3 serves as the storage solution for file uploads in the application. An S3 bucket (UploadsBucket) is configured with CORS settings and versioning to ensure secure and reliable file handling.

**Amazon DynamoDB**: DynamoDB is utilized as a NoSQL database for storing task-related data in a table (TasksTable). DynamoDB offers a serverless and scalable solution for efficient data management.

**Amazon Rekognition:** This service is integrated to perform image analysis, specifically label detection, enhancing the application's capabilities. The DetectLabelsFunction Lambda function is triggered by S3 events to analyze images uploaded to the designated bucket.

**Application Architecture**
The application architecture uses AWS Lambda, Amazon API Gateway, Amazon DynamoDB, Amazon Simple Storage Service (S3), and AWS Amplify Console. Amplify Console provides continuous deployment and hosting of the static web resources including HTML, CSS, JavaScript, and image files which are loaded in the user's browser. JavaScript executed in the browser sends and receives data from a public backend API built using Lambda and API Gateway. DynamoDB provides a persistence layer where data can be stored by the API's Lambda function. S3 is used to store uploaded images. Finally, Amazon Rekognition is used to detect and label objects in those images.
![image](https://github.com/binayapuri/image_recognization_app/assets/97520897/5e18e8ac-ddcb-451d-853b-5a862d48bce8)

****Final Application**
**
**Upload an Image and Detect Labels**
 fill up the information
 ![image](https://github.com/binayapuri/image_recognization_app/assets/97520897/cca2db76-a49b-4640-9d87-78574bdcdba9)
Choose a file and upload 
![image](https://github.com/binayapuri/image_recognization_app/assets/97520897/0aa845d0-a0c8-4603-9302-8a773c990deb)


Result : 
lets see the detected labels in the image where i use photo of dog wearing flower. 

![image](https://github.com/binayapuri/image_recognization_app/assets/97520897/378d2ab0-ac43-4358-b686-f5ac5cffbebb)
