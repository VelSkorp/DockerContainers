FROM jenkins/jenkins:lts

# Switch to root to install .NET Core SDK
USER root

# Install depency for dotnet core 6.
RUN apt-get update \
    && apt-get install -y --no-install-recommends \
    wget sudo curl libunwind8 gettext apt-transport-https \
    && curl https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > microsoft.gpg \
    && mv microsoft.gpg /etc/apt/trusted.gpg.d/microsoft.gpg \
    && sh -c 'echo "deb [arch=amd64] https://packages.microsoft.com/repos/microsoft-debian-stretch-prod stretch main" > /etc/apt/sources.list.d/dotnetdev.list' \
    && apt-get update
 
# Install the .Net Core framework, set the path, and show the version of core installed.
RUN apt-get install -y dotnet-sdk-6.0 \
    && export PATH=$PATH:$HOME/dotnet

# Switch back to jenkins user
USER jenkins