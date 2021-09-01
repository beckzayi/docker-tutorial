## Dockerize your React app and serve your build artifacts through Nginx


https://www.youtube.com/watch?v=gM2cWo1DWIk


1. Create React App
	```bash
	npx create-react-app my-react-project
	```

2. Create a Dockerfile, and .dockerignore

3. Build React Docker image based on Dockerfile (image is called “awesome-app”)
	```bash
	docker build -t awesome-app .
	```
	```bash
	docker build -t <IMAGE>:<IMAGE_VERSION> .
	```

4. Run the React App in a container
	```docker images``` to see if the image awesome-app has been built
	```bash
	docker run -p 8080:3000 -t awesome-app 
	```

5. Create a Dockerfile for production
	Run ```docker build -t awesome-app:nginx -f Dockerfile.production```

6. Run the App in nginx container
	```bash
	docker run -p 8081:3000 awesome-app:nginx
	```
