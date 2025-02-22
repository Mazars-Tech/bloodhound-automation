# BloodHound automation
Automatically run and populate a new instance of BH CE.
Only works on Linux (tested on Ubuntu 22.04). 

## How to run
```
usage: bloodhound-automation.py [-h] -p PORT -z ZIP [-P PASSWORD]

Automatically deploy a bloodhound instance and populate it with the SharpHound data

options:
  -h, --help            show this help message and exit
  -p PORT, --port PORT  The custom port for the neo4j container
  -z ZIP, --zip ZIP     The zip file from SharpHound containing the json extracts
  -P PASSWORD, --password PASSWORD
                        Custom password for the web interface (12 chars min. & all types of characters)
```

You can edit the docker file in the template folder for more customization.

By default, it starts three containers. When the script is done, you can shutdown both the web and the postgresql containers if you only wish to keep the neo4j one.


## Requirements

You need docker and docker-compose installed.
