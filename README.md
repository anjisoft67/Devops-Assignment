# example-app-nodejs-backend-react-frontend
Building an example-app-nodejs-backend-react-frontend microservices application.


By Creating Instances in AWS cloud.
Jenkins master (t2.large)
Installed jenkins and configured the all necessary plugins
K8s master (t2.medium)
Install kubeadm
K8s node (t2.medium)
Install kubeadm both master and node.
configured in jenkins,
Prometheus and Graphana (t2.medium)
Step-1: Jenkins master installed jenkins in it.



Jenkins: install plugins nodejs, Eclipse Temurin Installer


Installed docker on host machine.

     
step-2) Run the sonar container after that login to sonar by taking credentials
install plugin SonarQube Scanner
docker run -d --name sonar -p 9000:9000 sonarqube:lts-community (created container in jenkins master)

step-3) Configured the webhook to sonar to the jenkins and
Created project examplenodejs in sonar and webhook configuration to jenkins
step-4) Created kubenetes cluster by installing kubeadm both master and node..setup cluster up.
step-5) created jenkinsfile
step-6) created Dockefile
step-7) Created Kubernetes Deployment.yaml and service.yaml files
step-8) created terraform scripts for creating jenkins by IAC.
and installed Prometheus and Graphana and configured in Jenkins.


## Requirements

- Node.js >= v12

## Application structure

- `client/` directory - React front end code.
- `server/` directory - Node.js back end code.
- `static/` directory - Compiled front end assets. Created by webpack when you run the
command `npm run build`. The Node.js back end serves serves these assets using the
[`express.static`](https://expressjs.com/en/starter/static-files.html#serving-static-files-in-express) middleware.

## Usage

```bash
# Install dependencies for front end and back end
npm install

# Build front end assets with webpack
npm run build

# Run Node.js back end server
npm start
```

Load up http://localhost:3000 in your browser to view the example website.

## Libraries and frameworks used

- [Express](https://expressjs.com/) - "Fast, unopinionated, minimalist web framework for Node.js".

- [React](https://reactjs.org/) - "A JavaScript library for building user interfaces".

- [Webpack](https://www.npmjs.com/package/webpack) - A popular tool for building
front end assets e.g. CSS and JavaScript.

- [Sucrase](https://www.npmjs.com/package/sucrase) - A simpler and faster
alternative to [Babel](https://babeljs.io/) which brings support
for JSX, TypeScript, ES modules, and more to your client side and server side
JavaScript.
