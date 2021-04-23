## Docker commands

### Common commands
* Check images: ``` docker images ```
* check all containers (active/inactive): ``` docker ps -a ```
* Check container logs: ``` docker logs <container_id>  ```
* Stop container: ``` docker container stop  <container_id>```
* Remove image: ``` docker rm <image_id> ```
* Remove container: ```docker container rm <container_id> ```
  
### Create docker image and run container  
* Create new file with name **Dockerfile** and add all the commands to compose image
* Create docker image: ``` docker build <path> -t <Docker_Image_Name>:<tag vesrion> ```
* Start container from image: ``` docker run -p <machine_port>:<container_port> --name <Docker_Conainter_Name> -d <Docker_Image_Name> ```

### Commands to push and pull image to docker hub
* ```docker login --username <username> --password <password>```
* ```docker tag <image-name> <username>/<your repo on docker hub> ```
* ```docker push <username>/<your repo on docker hub> ```
  
### Pull docker image from remote repository
By default docker pull pulles images frmo docker hum, to change repo we can specify repo path to pull from   
  ``` docker pull <username>/<your repo on docker hub> ```

  To pull and run docker image form remote repo use command:
  ``` docker run -p <machine port>:<container port> pull <username>/<your repository on docker hub> ```
  
  ### Docker compose commands
  To create and start container use following commands
  * docker-compose up (default file in current dir docker-compose.yml)
  * docker-compose -f <compose file name> up
  * docker-compose up -d (detached mode)
  * docker-compose stop (if started using -d switch)
  * docker-compose down (bring everything down and remove all containers)

