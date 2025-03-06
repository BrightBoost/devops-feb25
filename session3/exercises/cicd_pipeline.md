## CI/CD Pipeline

You're tasked with:

1. Build a simple Node.js Express application. Or, if you're ambitious, a Node.js backend + React frontend “full-stack” app.
2. First, create a plan for source control, build steps, testing, and deployment.
3. Expected: By the end of the session, each group should have a functioning CI/CD pipeline that deploys your chosen app to a target environment (could be a local Docker container, Azure, a free Heroku account, GitHub Pages, or any other platform your group agrees upon).

This approach encourages research, collaboration, and problem-solving. You won’t just follow a tutorial, you’ll design and build the pipeline yourselves.

---

## Step 1: Choose an App and Tech Stack

Pick from a few recommended “presets” or choose your own:

### **Option A: Node.js + Express Only**
- Simpler option; focuses on server-side code only.
- Basic JavaScript/Node knowledge, maybe Express fundamentals.
You can use your own app **or**:
- Go to the demo project [here](https://github.com/BrightBoost/deploy-azure) and fork it to your GitHub account.

### **Option B: Node.js + Express (backend) + VanillaJS/React (frontend)**
- More challenging. You need to handle a separate frontend build (Webpack, Create React App, or Vite) and integrate that build into the pipeline.
- Familiarity with frontend frameworks, Node scripting, build tools.
You can use your own app **or** work with separate frontend and backend (these will require some ops, like in session 1. Recommended to get them to work locally first. Also, make sure to fork them!): 
   - The github link of the frontend is [here](https://github.com/BrightBoost/demo-frontend).
   - The github link of the backend is [here](https://github.com/BrightBoost/demo-backend).

Choose a stack that aligns with your skill set or interests. Some may prefer the simpler version, others might relish the full-stack challenge.

---

## Step 2: Research and Decide on CI/CD Tooling

### **Examples of CI/CD Tools**  
- **GitHub Actions**: Easy to integrate with GitHub repos.  
- **GitLab CI/CD**: Generous free tier.  
- **Jenkins**: Flexible and open-source, can run locally or in Docker.  
- **CircleCI / TravisCI**: Also popular hosted solutions with free tiers.
- **Azure pipelines**: You have access to accounts for this training.

Weigh high-level pros/cons of each platform, then decide which best fits the skill set of your group. The deciding factors might include:
 - Familiarity with the platform
 - Ease of setup
 - Available free credits or no-cost usage
 - Workflow language preference (YAML vs. Jenkinsfile, etc.)

---

## Step 3: Outline the Pipeline Requirements

**Minimal required stages** (you can add more if you want):
1. **Build**  
   - Install dependencies (npm install).  
   - Compile or bundle the frontend if applicable (npm run build).  
2. **Optional: Test**  
   - Run automated tests if any.  
3. **Package/Artifact**  
   - Create a Docker image (if using container-based deployments) or a zipped artifact.  
4. **Deploy**  
   - Push Docker image to a registry (Docker Hub, GitHub Container Registry, etc.) *or* deploy directly to a hosting platform (Heroku, AWS, Netlify for frontend, etc.).

You're encouraged to incorporate code linting, scanning for vulnerabilities, or coverage reporting if you have time. Please mind, real DevOps pipelines often have additional quality gates.

---

## Step 4: Plan the Deployment Strategy

Let each group propose your own deployment approach. Some ideas:

- **Docker-based**: Build a Docker image and run it locally or deploy to a free Docker hosting platform like Azure Container Instances (if credits allow) or a local Minikube cluster.  
- **Platform as a Service**: Heroku free tier (for Express), Netlify (for React frontends), Render, or Railway.  
- **Static Hosting**: If you only do a React frontend, GitHub Pages or Netlify can be quick wins.

Again, weigh the pros and cons: does the team want to learn containerization? Or is Heroku’s Git based autodeploy enough? No solution is “best” here; it’s about what fits the skills and the time constraints.

---

## Step 5: Create Documentation / Present the Plan

Before coding, you should document your intended approach:
1. **Tech stack chosen**: Node.js alone or Node + React, etc.
2. **CI/CD platform**: GitHub Actions, Jenkins, etc.
3. **Pipeline stages**: Build, test, containerize, deploy.
4. **Deployment environment**: Docker local, Heroku, Netlify, etc.
5. **Roles & responsibilities**: If multiple people in the group, who handles front-end vs. pipeline vs. deployment steps?

---

## Step 6: Let's Implement It

Finally, let's do it! Let's implement the pipeline in your chosen CI/CD platform. Rather than handing out step-by-step instructions:
1. Checkout references to the official docs or DevOps tutorials for that platform (e.g., GitHub Actions docs, Jenkins docs).
2. You're encouraged to troubleshoot pipeline errors yourselves (with you or peers providing hints if you get stuck).
3. At the end, each group should do a brief demo talking through the plan and showing the pipeline in action.

---

## Optional: Go Wild

1. **Automated Code Quality**: Integrate ESLint or SonarQube scanning as part of the pipeline.
2. **Infrastructure as Code**: Use something like Terraform to spin up a test environment on AWS or Azure (if free resources are available).
3. **Monitoring & Logging**: Show how to add logging or basic metrics to the app. This is often overlooked in quick DevOps tutorials but is extremely valuable in real-world scenarios.
4. **Rollbacks**: Figure out a rollback strategy if the new version fails (manual vs. automated revert, etc.).
5. Anything you have in your design can be added.

---
## Optional: Implement the Pipeline with Different Tools to Understand Differences
