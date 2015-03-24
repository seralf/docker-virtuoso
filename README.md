# Virtuoso docker
Docker for hosting Virtuoso.

The Virtuoso is built from a specific commit SHA in https://github.com/openlink/virtuoso-opensource.

## Running your Virtuoso
    docker run --name my-virtuoso \
        -p 8890:8890 -p 1111:1111 \
        -e DBA_PASSWORD=myDbaPassword \
        -v /my/path/to/the/virtuoso/db:/var/lib/virtuoso/db
        -d tenforce/virtuoso

The Virtuoso database folder is mounted in `/var/lib/virtuoso/db`.
The Docker image exposes port 8890 and 1111.
The `dba` password can be set at container start up via the `DBA_PASSWORD` environment variable.