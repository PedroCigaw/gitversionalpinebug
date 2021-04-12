# gitversionalpinebug

This project highlights a bug in GitVersion when building a docker image based on mcr.microsoft.com/dotnet/runtime-deps:5.0-alpine

Essentially as part of the docker file build a copy of the appropriate files and folders are copied to the container including the .git and GitVersion.yml files.

build the Dockerfile.alpine.base file and bash into a running instance.

Running dotnet-gitversion produces "Segmenation Fault"

I don't see this issue when building the debian based dotnet images.
