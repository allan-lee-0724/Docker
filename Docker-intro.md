# Docker
When deloying applications there are many factors you must account for:
- Can I even run my app in the environment?
- Is the correct runtime environment installed?
- Is the correct build tool installed?
- Do my security settings allow access to my application?

Docker is the answer to simplifying this process. Instead of having to worry about having all the right tools
available on whatever device you are deploying your app on, if you have docker installed, the answer is "yes".
Docker creates a virtual "container" for your application that can handle the building/running/exposure for your
application.

## Containerization
According to docker, a container is, "a standard unit of software that packages up code and all its dependencies
so the application runs quickly and reliably from one computing environment to another." This includes the 
necessary "code, runtime, system tools, system libraries and settings."

This containerization is achieved by turning "images" into containers. Images contain the instructions for how
your containerized application should be built/deployed. Once docker engine has read the image, Docker then
creates the container based off the configuration details you provided in the image, and then you are free to 
interact with your application like you had started it up yourself.

## Image & Dockerfile
Docker uses "Dockerfile"s to know how it is supposed to build an image. You can set the following details within a docker file (this is not an exhaustive list):
- Base image
    - What kind of environment should the application run in?
- Working directory
    - What directory within the container should be considered the root directory
- Application details
    - What source code and/or executable files should be included in the container
- Commands
    - What build/execution commands should be used when the container is started?