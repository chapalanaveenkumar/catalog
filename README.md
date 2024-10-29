Shamir's Secret Sharing Algorithm API
This project implements a simplified version of Shamir's Secret Sharing algorithm. The API exposes a POST endpoint to calculate the secret code based on input shares.
Prerequisites
Ensure that the following are installed on your system:
Node.js (version 14 or higher)
npm (comes with Node.js)
Installation
Clone the repository:
bash
Copy code
git clone <repository-url>
Navigate to the project directory:
bash
Copy code
cd <project-directory>
Install the required dependencies:
bash
Copy code
npm install
Running the Server
Start the server by running:
bash
Copy code
npm start
This will start the API server, which by default runs on http://localhost:3000.

Testing the API
You can test the API using Postman or any HTTP client.

Endpoint:

URL: http://localhost:3000/calculateSecretCode
Method: POST
Request Body: Send a JSON object in the body with the necessary shares:

json
Copy code
{
    "keys": {
        "n": 4,
        "k": 3
    },
    "1": {
        "base": "10",
        "value": "4"
    },
    "2": {
        "base": "2",
        "value": "111"
    },
    "3": {
        "base": "10",
        "value": "12"
    },
    "6": {
        "base": "4",
        "value": "213"
    }
}
Response: The response will contain the calculated secret code based on the input shares.
