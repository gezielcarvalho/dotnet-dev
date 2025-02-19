# Use the official .NET 8 SDK image as the base
FROM mcr.microsoft.com/dotnet/sdk:8.0

# Set the working directory inside the container
WORKDIR /app

# Install debugging/networking tools
RUN apt-get update && apt-get install -y \
    net-tools \       
    iputils-ping \    
    vim \             
    procps \          
    iproute2 \        
    curl \           
    dnsutils \        
    && rm -rf /var/lib/apt/lists/*  

# Expose the port used by the .NET application
EXPOSE 5151

# Start a shell by default (useful for debugging)
CMD ["/bin/bash"]
