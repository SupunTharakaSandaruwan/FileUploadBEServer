# File Upload BE Server

This repository contains the backend server for file upload functionality.

## Getting Started
### 1. Prerequisites
Make sure you have the following prerequisites installed on your machine:

- Java
- Maven
### 2. Clone the Repository

```
git clone https://github.com/SupunTharakaSandaruwan/FileUploadBEServer.git
```

### 3. Build the Project
Navigate to the project directory and build the project using Maven:
```
mvn clean install -Dmaven.test.skip=true
```
### 4. Copy the JAR
Copy the generated JAR file from the target/ directory to a separate location.

### 5. Create Properties File
Create a properties file named file-upload.properties under the same location where the .jar file is located and insied the above properties file, define the target location of file upload.

-- Define File Upload Path as follows
 1. Edit the file-upload.properties file and define the file upload path:

   ```
   upload.directory=<your_fileUpload_full_path>
   ```
* Replace <fullPath> with the full path where you want to store the uploaded files.

### 6. Run the Application
Run the application using the generated JAR file:
```
java -jar file-upload-example-1.0.0.jar 
```
Replace <your-jar-filename> with the actual name of the JAR file.
### 7. Access the API

```
curl --location 'http://localhost:8080/api/files/upload' \
--form 'file=@"<fullPath>/yourFileName"'
```
Example
```
curl --location 'http://localhost:8080/api/files/upload' \
--form 'file=@"/Users/testuser/Library/simple/sampleFile.json"'
```
##### Folder structure #####
  <Your folder>
    |-file-upload-example-1.0.0.jar
   |-file-upload.properties

* Contributors 
Supun Tharaka Sandaruwan
Feel free to contribute or report issues!
