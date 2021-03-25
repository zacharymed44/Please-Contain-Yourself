# What image do you want to start building on?
FROM node:latest

#------------------------------------------------------#

# Make a folder in your image where your app's source code can live
RUN mkdir -p /src/app
#make directory called app in src folder, -p makes the src folder(parent folders)

#------------------------------------------------------#

# Tell your container where your app's source code will live
WORKDIR /src/app
#tells your container which directory is the working directory

#------------------------------------------------------#

# What source code do you what to copy, and where to put it?
COPY . /src/app
#COPY takes two arguments:
#   '.' this says where to copy the app's soruce code from
  # in this case, its the relative path that points to the directory the dockerfile is in
# /src/app - refers to the directory inside tof the image that we just made a few commands ago

#------------------------------------------------------#

# Does your app have any dependencies that should be installed?
RUN yarn install
  #installs all the dependences necessary to run our node application using the yarn package manager
  #dockerignore

#------------------------------------------------------#


# What port will the container talk to the outside world with once created?
EXPOSE 3000
  # expose the containers port 3000 which will need to be mapped to a port on the hose when spun into a container by using the -p option with the docker run command

#------------------------------------------------------#


# How do you start your app?
CMD ["npm", "start"]
  #this command just tells the image to say npm start from inside the container once it is created
  
