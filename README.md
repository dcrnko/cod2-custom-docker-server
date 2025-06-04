#My custom Call of Duty 2 docker server

This project is an adjusted version of the excellent work by [bgauduch](https://github.com/original-author/original-repo(https://github.com/bgauduch/call-of-duty-2-docker-server)). This repository is for closed circle of friends to be used when necessary. 

## Original Project: [call-of-duty-2-docker-server]
* **Author:** [bgauduch]
* **Original Repository:** https://github.com/original-author/original-repo

## My Adjustments
I have modified this project to:
- Added rcon password(on request)
- Added Server password(on request)

## How to use:
1. Clone or download this repository on your host machine;
2. Copy required data from the main folder of your original game (install directory or retail DVD) to the server:
2.1 Copy all the iw_XX.iwd from 00 to 15 to the cod2server/main folder;
2.2 Copy all the localizations localized_english_iwXX.iwd to the cod2server/main (it might be another language).

OR

Request the FULL Docker image. 

Launch the server
1. From the project root:
docker-compose up -d

2.Restart the server (to pick up config change for instance):
# cod2_server refer to the name of the service in the compose file
docker-compose logs -f cod2_server
3.Attach a shell to the server to run commands.
docker container attach call-of-duty-2-docker-server_cod2_server_1
# exemple commands
status
map_rotate
# Use the escape sequence to detach: `CTRL+P`, `CTRL+Q`or type "quit".
4. Completely stop the server:
docker-compose down

## Thanks
A huge thank you to [bgauduch] for creating the foundational work!
