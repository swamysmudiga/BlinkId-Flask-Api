To run the Face Recognition Service, which is a Flask API hosted on EC2, follow these steps:

## Prerequisites

Before starting, ensure you have:

1. Access to an AWS EC2 instance.
2. Python installed on the EC2 instance.
3. Access to the codebase of the Face Recognition Service (`blinkid-flask-api-main`).

## Step-by-Step Guide

### 1. Connect to your EC2 Instance

Connect to your EC2 instance using SSH:

```bash
ssh -i your-key.pem ec2-user@your-ec2-instance-public-ip
```

Replace `your-key.pem` with the path to your private key file, and `your-ec2-instance-public-ip` with the public IP address of your EC2 instance.

### 2. Clone the Repository

Clone the repository containing the Face Recognition Service code:

```bash
git clone https://github.com/your-username/blinkid-flask-api-main.git
```

### 3. Navigate to the Project Directory

Change to the directory where the Flask API code is located:

```bash
cd blinkid-flask-api-main
```

### 4. Install Dependencies

Install the required Python dependencies using pip:

```bash
pip install -r requirements.txt
```

### 5. Configure the Application

Update any configuration files as needed. This may include setting environment variables or modifying configuration files such as `config.py`.

### 6. Run the Flask Application

Start the Flask application:

```bash
python app.py
```

### 7. Verify the Service

Once the service is running, verify it by sending requests to its endpoints using tools like `curl` or Postman. Ensure that the service behaves as expected and performs facial recognition accurately.

### 8. Set Up NGINX and Gunicorn (Optional)

For production deployment, it's recommended to use a WSGI HTTP server like Gunicorn and a reverse proxy server like NGINX to serve the Flask application. Set up NGINX and Gunicorn according to your deployment requirements.

### 9. Monitor and Maintain

Monitor the performance of the service using tools like AWS CloudWatch or third-party monitoring solutions. Regularly maintain and update the service to ensure security and reliability.

## Conclusion

You have successfully set up and run the Face Recognition Service.
