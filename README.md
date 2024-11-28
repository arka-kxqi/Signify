# **Signify**

## **Elevator Pitch**

"Streamline document signing with seamless, secure eSignature integration using DocuSign's API."

## **Inspiration**

The inspiration behind **Signify** came from the growing need for digital transformation in document management. Traditional paper-based signatures are time-consuming, costly, and prone to errors. By leveraging DocuSign's eSignature API, **Signify** aims to simplify and automate the process of obtaining electronic signatures, making it more efficient, secure, and eco-friendly.

## **What it does**

**Signify** integrates DocuSign’s eSignature API into a web application, allowing users to:
- **Create envelopes** (documents) that require signatures.
- **Send documents** to recipients for electronic signing.
- **Track the signing process** and receive real-time updates.
- **Utilize templates** for quick and easy document creation.
- **Authenticate using OAuth 2.0** for secure access to the DocuSign API.

## **How we built it**

We built **Signify** using a modern tech stack:
- **Backend**: Node.js and Express to handle API requests, OAuth authentication, and envelope creation.
- **Database**: MongoDB for storing user data and document statuses.
- **DocuSign API**: Integrated for creating envelopes, managing templates, and tracking document status.
- **JWT Token**: Used for secure, token-based authentication with DocuSign.
- **Frontend**: Simple HTML/CSS for the user interface, with JavaScript handling user interactions.
- **OAuth 2.0 Authentication**: Used to securely authenticate users with DocuSign.

## **Getting Started**

Follow these steps to set up and run the project locally.

### **1. Create a DocuSign Developer Account**
If you don’t already have a DocuSign developer account, sign up for one at [DocuSign Developer](https://www.docusign.com/developer-center).

### **2. Set Up Your DocuSign App**

- Navigate to the **App and Keys** section of the [DocuSign Developer Portal](https://account-d.docusign.com).
- Create a new app and RSA key pair.
- Save the **private key** as `private.key` for use in the project.
- Whitelist `http://localhost:3000/` in the **Redirect URIs** under your app's settings.

### **3. Configure the Project**

- Clone this repository to your local machine.
- Create a `.env` file and add your DocuSign credentials. The required fields are:
  - `CLIENT_ID` (your app’s client ID from DocuSign)
  - `CLIENT_SECRET` (your app’s client secret)
  - `REDIRECT_URI` (should be `http://localhost:3000/`)
  - `PRIVATE_KEY` (path to your private key)

### **4. Install Dependencies**

Run the following command in the project directory to install the necessary dependencies:

```bash
npm install
```

### **5. Create a DocuSign Template**

Create a template in the DocuSign portal and use the `Internship Application.pdf` provided in this repository as your document template. This template will be used for creating envelopes in your app.

### **6. Run the Application**

Start the application using:

```bash
npm start
```

Visit `http://localhost:3000/` to interact with the app.

### **7. OAuth Consent Flow**

To authorize your app, navigate to the consent URL below, replacing `(YOUR CLIENT ID)` with your actual client ID:

```
https://account-d.docusign.com/oauth/auth?response_type=code&scope=signature%20impersonation&client_id=(YOUR CLIENT ID)&redirect_uri=http://localhost:3000/
```

### **8. Test the Integration**

Once authenticated, you can create and send envelopes for signing directly from the application.

## **Challenges we ran into**

- **OAuth 2.0 Authentication**: Setting up and handling the OAuth 2.0 flow with DocuSign was tricky, especially managing token expiration and refreshing tokens automatically.
- **Template Integration**: Working with DocuSign templates required understanding their API and how to properly configure templates for dynamic use within the app.
- **Real-time Document Tracking**: Implementing real-time document status updates required integrating webhooks, which was a bit challenging to set up correctly.

## **Accomplishments that we're proud of**

- Successfully integrating DocuSign's eSignature API to allow document creation and signing workflows.
- Building a user-friendly interface for document management.
- Implementing OAuth 2.0 authentication seamlessly for secure user access.
- Storing user and document data in MongoDB to track envelopes and signing statuses.

## **What we learned**

- **OAuth 2.0**: Learned in-depth about OAuth 2.0 authentication and how to securely authenticate users with third-party APIs like DocuSign.
- **API Integration**: Gained experience in integrating third-party services (like DocuSign) into a web application, handling API responses, and managing document flows.
- **Handling Webhooks**: Worked with DocuSign’s webhook feature to receive real-time updates about document signing statuses.

## **What's next for Signify**

- **Enhanced User Interface**: Improving the frontend experience by adding more advanced features, such as progress bars, document previews, and better error handling.
- **Multi-Template Support**: Implementing a feature to allow users to choose from multiple templates for different document types.
- **Mobile Version**: Building a mobile-responsive version or even a native mobile app for users to manage documents on the go.
- **Expanded Integrations**: Exploring integration with other document management and cloud storage services, such as Google Drive or Dropbox.

## **Inspiration**

The inspiration behind **Signify** came from the growing need for digital transformation in document management. Traditional paper-based signatures are time-consuming, costly, and prone to errors. By leveraging DocuSign's eSignature API, **Signify** aims to simplify and automate the process of obtaining electronic signatures, making it more efficient, secure, and eco-friendly.

## **What it does**

**Signify** integrates DocuSign’s eSignature API into a web application, allowing users to:
- **Create envelopes** (documents) that require signatures.
- **Send documents** to recipients for electronic signing.
- **Track the signing process** and receive real-time updates.
- **Utilize templates** for quick and easy document creation.
- **Authenticate using OAuth 2.0** for secure access to the DocuSign API.

## **How we built it**

We built **Signify** using a modern tech stack:
- **Backend**: Node.js and Express to handle API requests, OAuth authentication, and envelope creation.
- **Database**: MongoDB for storing user data and document statuses.
- **DocuSign API**: Integrated for creating envelopes, managing templates, and tracking document status.
- **JWT Token**: Used for secure, token-based authentication with DocuSign.
- **Frontend**: Simple HTML/CSS for the user interface, with JavaScript handling user interactions.
- **OAuth 2.0 Authentication**: Used to securely authenticate users with DocuSign.

## **Challenges we ran into**

- **OAuth 2.0 Authentication**: Setting up and handling the OAuth 2.0 flow with DocuSign was tricky, especially managing token expiration and refreshing tokens automatically.
- **Template Integration**: Working with DocuSign templates required understanding their API and how to properly configure templates for dynamic use within the app.
- **Real-time Document Tracking**: Implementing real-time document status updates required integrating webhooks, which was a bit challenging to set up correctly.

## **Accomplishments that we're proud of**

- Successfully integrating DocuSign's eSignature API to allow document creation and signing workflows.
- Building a user-friendly interface for document management.
- Implementing OAuth 2.0 authentication seamlessly for secure user access.
- Storing user and document data in MongoDB to track envelopes and signing statuses.

## **What we learned**

- **OAuth 2.0**: Learned in-depth about OAuth 2.0 authentication and how to securely authenticate users with third-party APIs like DocuSign.
- **API Integration**: Gained experience in integrating third-party services (like DocuSign) into a web application, handling API responses, and managing document flows.
- **Handling Webhooks**: Worked with DocuSign’s webhook feature to receive real-time updates about document signing statuses.

## **What's next for Signify**

- **Enhanced User Interface**: Improving the frontend experience by adding more advanced features, such as progress bars, document previews, and better error handling.
- **Multi-Template Support**: Implementing a feature to allow users to choose from multiple templates for different document types.
- **Mobile Version**: Building a mobile-responsive version or even a native mobile app for users to manage documents on the go.
- **Expanded Integrations**: Exploring integration with other document management and cloud storage services, such as Google Drive or Dropbox.



## Instructions

1. Navigate to `App and Keys` in the DocuSign developer portal and create a new app.
2. On the app creation page, create a new RSA Key and save the private key in a new file `private.key`
3. Whitelist `http://localhost:3000/` in Redirect URIs in the App creation page
4. Fill in the `.env` file with your app credentials
5. Install the dependencies by running `npm install` in the terminal
6. Create a new template in DocuSign. You can use the `Docusign Load Application.pdf` present in this directory.

When giving consent to your app you can use the URL below, fill in your client id before openin the URL

```
https://account-d.docusign.com/oauth/auth?response_type=code&scope=signature%20impersonation&client_id=(YOUR CLIENT ID)&redirect_uri=http://localhost:3000/
```

# Project Screenshot


## FRONT PAGE TO SEND DETAILS
#
 ![Screenshot 2023-04-29 100120](https://user-images.githubusercontent.com/99763066/235283525-0129a0d9-f9c7-45c0-9032-1b63ef848682.jpg)
 
 ## Getting Access Token 
 #
 ![Screenshot 2023-04-29 100345](https://user-images.githubusercontent.com/99763066/235283576-b2f95dea-8633-43f2-81c8-baaf77db1403.jpg)

## Creating templates 
#
![Screenshot 2023-04-29 100547](https://user-images.githubusercontent.com/99763066/235283632-5b9d1096-dd35-4aff-90b8-b41a30cdd637.jpg)

## Getting Mails
![Screenshot 2023-04-29 100657](https://user-images.githubusercontent.com/99763066/235283676-daa00506-4ac6-4808-97e9-1e59eaca6b09.jpg)

