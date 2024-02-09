# Requirements and Installation

> Note: Basic knowledge of command line is required.

Software:

- [Docker](https://www.docker.com/)

Host System:

- 15GB storage

- 8GB RAM

- Modern CPU

Installation Instructions:

### 1. Download and install Docker

Alternatively, you can download [Docker Desktop]](https://www.docker.com/get-started) if you prefer a desktop GUI.

### 2. Download Sybij

For the Mac / Linux version run the following command:

```bash
docker pull mitjclinic/sybil
```

For the Windows Version run the following command:

```bash
docker pull mitjclinic/sybil:windows
```

### 3. Verify that the image has been successfully loaded:

To do this, run the following command:

```bash
docker image ls
```

# Local Command Line Demo

The "sybil" container creates a server for an API. The API implements
the endpoint "/dicom/files" to receive DICOM files through a HTTP POST
request. The API will then return predictions with the server's
response.

Running the Server/Model:

1.  Download and extract the [demo data](https://www.dropbox.com/sh/addq480zyguxbbg/AACJRVsKDL0gpq-G9o3rfCBQa?dl=0). [This folder](https://drive.google.com/file/d/1aiwXn0cHIPzVS1eYwJDERijnYg94sIhH/view?usp=sharing) folder contains one LDCT from the publicly available LUNA16 dataset used as demo data, and a text file called sybil_run.txt that will allow you to process that particular example.

2.  Choose a \[PORT\] to expose, i.e., 5000. Run the docker image:

```bash
docker run -p \[PORT\]:5000 mitjclinic/sybil:windows
```

You should see logging messages indicated that a server has been started.

- In the sybil_run.txt file, fill http://localhost:\[PORT\]/dicom/files with your chosen
  port. Next, with the extracted folder "sybil_demo_data/" in the same
  working directory, you can run the demo using the sybil_run.txt
  file:

```bash
sh sybil_run.txt
```

The curl command may need to be installed with your package manager

depending on your OS.

Given that LDCTs usually are usually composed of dozens of DICOM
images, we provide this text file that allows you to loop over all the
images in a directory (example: sybil_demo_data or any other directory
containing the images for a single patient) and send them to the API
as one single request.

Be sure to replace \[PORT\] in the sybil_run.txt file with your chosen
port number.

**Important Note**: Each request to this endpoint should be the
equivalent of a single exam.4. After a few minutes, you will receive a JSON response like so:

On the hospital side, some program/script would need to be written to send files to the API and handle the JSON return object. This program ideally will be what interfaces with a database to grab the DICOM images and store the JSON predictions.
