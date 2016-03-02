# Application
[PlexPy](https://github.com/drzoidberg33/plexpy)

# Description
A python based web application for monitoring, analytics and notifications for Plex Media Server

# Access application
`http://<host ip>:8181`

# Run the application
## Usage
Please replace all user variables in the above command defined by ```<>``` with the correct values.
```
docker run -d
  --name=<container name> \
  -p <port>:8181
  -v <path for config files>:/config
  -e PUID=<uid for user> \
  -e PGID=<gid for user> \
  tyler43636/unraid-plexpy
```

## Example
```
docker run -d
  --name=plexpy \
  -p 8181:8181
  -v /config:/config
  -e PUID=99
  -e GUID=100
  tyler43636/unraid-plexpy
```

# Notes
User ID (PUID) and Group ID (PGID) can be found by issuing the following command for the user you want to run the container as:
```
id <username>
```
