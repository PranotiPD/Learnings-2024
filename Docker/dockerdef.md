# Docker

##  What is Docker

-> It is virtualization software which makes **developing** and **deploying applications** very easy


-> It packages application with all the necessary dependencies, configuration, system tools and runtime.


-> In simple terms, you can say that it is a **standardized unit**, that has everything the application needs to run.  

## * Development process before containers?

-> Each developer needs to install and configure all services diectly on their OS on their 
local machine  
-> In this scenario, depending on OS, installation process will be different for different OS, in case of complex applications this process is very tedious and chances of error happening in this process are very high  

## * Development process with containers?

-> With Docker you have that service packaged in one **isolated environment**  
-> With container you don't have to install any of the service on your OS  
-> So, you just have to start a Docker container using 1 Docker command and the command would same irrespective of OS  
-> for example if you have 10 services (eg. PostgreSQL, redis) that your application depends on so you just have to run 10 commands for each container and that will be it  
-> It standardizes process of running any service on any local dev environment  
-> **Easy to run different versions** of same app without any conflicts  

## Deployment process before containers?

-> Development team needed to handover Artifacts(installation instructions, configurations and server setup) and instructions to operations team  
-> Problem with this approach is that you have to install everything on OS, which is as we know is error prone (eg. dependency version conflicts, wrong textual instructions)
-> These kind of problems get solved with containers  

## Deployment process with containers?

-> Now developers create application package that doesn't only include code itself but also  
all the dependencies and configurations.  
-> No configurations needed on server (except Docker runtime), less room for errors  
-> Now operations team needs to only install Docker runtime on the server and run Docker command to fetch and run Docker artifacts  

