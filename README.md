# Ecommerce MERN Project

## Getting Started

Follow these instructions to set up the project on your local machine for development and testing.

### Prerequisites

Ensure you have the following installed:

- **Node.js**
- **NPM** or **Yarn**

### Environment Variables

Create a `.env` file inside the `server` directory and add the following variables. Replace these values with your own API keys:

```
BRAINTREE_MERCHANT_ID=your_id
BRAINTREE_PUBLIC_KEY=your_public_key
BRAINTREE_PRIVATE_KEY=your_private_key
```

### Installation

Install dependencies for both client and server.

Run the following commands from the project root:

```sh
cd client && npm install
```

```sh
cd server && npm install
```

### Running the Application

Open a terminal and navigate to the `server` directory:

```sh
npm run start:dev
```

Then, open another terminal in the `client` directory:

```sh
npm run start
```

Access the application at: [http://localhost:3000/](http://localhost:3000/)

---

## Deploying the Backend to Render

Follow these steps to deploy the backend on [Render](https://render.com/):

1. **Create a Render Account**: Sign up at [Render](https://render.com/).
2. **Connect to GitHub**: Link your GitHub repository and grant necessary permissions.
3. **Create a New Web Service**: Add your repository, ensuring the structure includes both frontend and backend folders.
4. **Use a Dedicated Branch**: Deploy changes from the `render-deploy-backend` branch.
5. **Update MongoDB Connection**:
   - Replace the local database connection with MongoDB Atlas.
   - Retrieve your MongoDB Atlas connection string, which looks like this:
     ```
     mongodb+srv://<username>:<password>@<cluster>.mongodb.net/ecommerce?retryWrites=true&w=majority
     ```
   - Navigate to the `render-deploy-backend` branch and update the `.env` file:
     ```
     DATABASE=mongodb+srv://<username>:<password>@<cluster>.mongodb.net/ecommerce?retryWrites=true&w=majority
     ```
   - Find your **MongoDB Atlas** URL by logging into [MongoDB Atlas](https://www.mongodb.com/cloud/atlas), going to **Database**, clicking **Connect**, and copying the connection string.
   - **Important**: Use your _cluster password_ (not your account password).

### Render Configuration

- Set up your web service as shown below.
- Ensure you change the branch name from `master` to `render-deploy-backend`.

![Render Setup](assetREADME.md/renderDeployBackendSetup.png)

Once configured, create the web service, and it will deploy automatically.

---

## Deploying the Frontend

You can deploy the frontend to:

- [Vercel](https://vercel.com/)
- [Netlify](https://www.netlify.com/)

### Final Notes

by Fourat Mejri

Thanks
