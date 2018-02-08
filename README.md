#ChRIS End To End Testing Environment
This script autmatically builds and deploys the ChRIS backend in docker-compose and pman and pfioh in Openshift. Currently,
this only works locally. I am working on an implementation of this that builds the end to end system in a vagrant vm as well.

This script takes the following flags:
    --deps              This will trigger the script to install and configure the necessary dependancies on your system

    --interactive       The ChRIS_backend container will be run in interactive mode at the end of this script.
                            Note: if you include this flag, when the script ends the terminal buffer you are using
                            will be attached to the docker shell of the ChRIS_backend container
    
    --vagrant           The end to end system will be deployed in a vagrant vm instead of on your local system.
                            WARNING: this has not yet been implemented

    --test              This will run tests agains the components of the system to make sure they are working correctly

    --help              Prints this message and exits the script with code 0

##Usage
You must run this bash script with sudo permissions. The easiest way to do this is as follows:
    sudo bash mkenv.sh