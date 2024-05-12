A demonstration of Docker to implement a simple 3-tier architecture

The frontend can access the mid-tier.
The mid-tier can access the database.
Requests to both frontend and API are routed through an NGINX reverse proxy.
Running the Application

To run this application, type docker-compose up at the command prompt. Docker will set up the environment as follows:

MongoDB: Utilizes the mongo image to create a MongoDB container for the database tier.
API: Uses Node.js with Express for the mid-tier, built from a node:alpine image, which handles business logic and database operations.
Frontend: The frontend is powered by ReactJS, also built from a node:alpine image, providing the user interface.
NGINX: Configured as a reverse proxy, NGINX routes incoming requests to either the frontend or the API based on the URL path. It improves security and efficiency of handling requests.
Architecture Overview

This setup illustrates a typical 3-tier architecture within a Docker environment, enhanced with an NGINX reverse proxy for better control over traffic flow and security.
