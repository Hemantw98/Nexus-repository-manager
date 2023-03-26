<h2 align="center">
<b>Nexus-Repository-Manager</b></
</div>

## About ℹ️

This repo contains the Nexus artifact repository manager project to run Nexus on Droplet and Publish Artifact to Nexus

## Key Componets 🧑<200d>💻


- **DigitalOcean** : For creating Virtual Private Cloud Server.
- **Java** : For installing java application on server.
- **Maven** : Build tool of Java applications for buidling the java application. 
- **Java-maven** app : source code for our java maven application along with .jar aka artifact file for uploading on Nexus artifact repository Manager

## Tech Used 💻

- Nexus
- Digital-Ocean
- Linux
- Java
- Maven


## Part 1: Setting up server aka droplet in DigitalOcean ⚒️

To run the Nexus artifact repository manager on a DigitalOcean Droplet and publish artifacts to Nexus, you can follow these general steps:

#### 1. Create a new Droplet on DigitalOcean. Choose an appropriate size and operating system based on your needs.


#### 2. Connect to the Droplet using SSH. You can do this using the command line on your local computer or using a program like PuTTY.



#### 3. Install Java on the Droplet, if it is not already installed. You can do this by running the following command:


    sudo apt-get install default-jdk

#### 4. Download the Nexus repository manager distribution from the Sonatype website. You can download the OSS (open source software) version from https://www.sonatype.com/download-nexus-repo-oss.

    

#### 5. Extract the downloaded file to a location on the Droplet. For example, you could extract it to the /opt/nexus directory:

    sudo mkdir /opt/nexus
sudo tar -xvzf nexus-<version>.tar.gz -C /opt/nexus --strip-components=1

#### 6. Create a new Nexus user by running the following command:

    sudo adduser nexus

#### 7. Give the new Nexus user ownership of the Nexus installation directory:

    sudo chown -R nexus:nexus /opt/nexus

#### 8. Start the Nexus service by running the following command:

    sudo /opt/nexus/bin/nexus start

#### 9. Access the Nexus web interface by navigating to the following URL in a web browser:

    http://<droplet-ip>:8081
    
#### 10. Log in to Nexus using the default administrator credentials:

    Username: admin
    Password: admin123
    
#### 11. Once you're logged in, you can create a new repository by following the instructions in the Nexus documentation. You can then publish artifacts to the repository using Maven or another build tool. Be sure to configure your build tool to use the correct repository URL and authentication credentials.    

#### That's it! You should now have Nexus up and running on your Droplet, and you can start publishing and managing your artifacts.
