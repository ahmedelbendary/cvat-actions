# Computer Vision Annotation Tool (CVAT)

Please see https://openvinotoolkit.github.io/cvat/about/ for documentation.

*WARNING* this code has a bug where people who register automatically can see all tasks (which is bad!) I have disabled the ability to register, but it is strongly recommended that we only deploy/access this via a VPN for this reason.


## Deploy Instructions and Details

`docker-compose -f docker-compose.yml -f docker-compose.dev.yml build`

`docker-compose up -d`

The application runs on localhost:8080

## Inital Setup

As I have disabled a way to register, I need to manually create a default super user.

Please run the following command to do this, set the username as 'Tom' and for the password, please choose something strong:

`docker exec -it cvat bash -ic 'python3 ~/manage.py createsuperuser'`

## System Requirements

The following documentation explains where data (images) and annotations (meta data) are stored:

https://openvinotoolkit.github.io/cvat/docs/for-users/faq/#where-are-uploaded-imagesvideos-stored

I estimate we need about 5GB of storage at the moment for images.




