# Lab 3 – Microservices Deployment on Azure (PaaS)

## 🎥 Demo Video
YouTube Demo:  
https://www.youtube.com/watch?v=zKv2EF0r9sM


## 🌐 Deployed Services (Azure)
- Order Service URL: https://order-service-app-muhannad.azurewebsites.net/health  
- Product Service URL: https://product-service-app-muhannad.azurewebsites.net/products   

---

## ✍️ Reflection Questions

### 1. What challenges did you encounter when configuring environment variables in the GitHub Actions workflow?

One of the main challenges was understanding where environment variables should be defined and how they are injected into the build and deployment process. Small mistakes in variable names or missing secrets caused the application to fail silently, making debugging difficult. It also took time to understand the difference between local `.env` variables and GitHub Actions secrets.

---

### 2. How does deploying microservices on Azure Web App Service differ from running them locally?

Running services locally is simpler because everything is controlled on one machine with direct access to ports, environment variables, and logs. Deploying to Azure Web App Service introduces additional configuration such as startup commands, environment variables in the Azure portal, networking rules, and cloud logging. Debugging cloud deployments also requires checking Azure logs instead of just console output.

---

### 3. Why is it important to use environment variables for configurations in a cloud environment?

Environment variables allow sensitive information such as connection strings, credentials, and service URLs to be managed securely without hardcoding them into source code. This makes applications more secure, portable, and easier to configure across different environments such as development, testing, and production. It also allows configuration changes without modifying or redeploying code.

---

## 📝 Notes / Lessons Learned 

- Azure Web Apps require using `process.env.PORT` for Node.js apps.
- Environment variables must be configured in both Azure App Service and GitHub Actions.
- Cloud deployments require more attention to logs and startup configuration.
- PaaS is easier to manage than VMs once properly configured.
