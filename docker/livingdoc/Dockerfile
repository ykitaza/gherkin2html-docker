# Use a .NET SDK image as the base
# Choose a version that is compatible with SpecFlow+ LivingDoc CLI
FROM mcr.microsoft.com/dotnet/sdk:8.0

# Set the working directory inside the container
WORKDIR /app

# Install SpecFlow+ LivingDoc CLI as a global tool
# Use the --global flag to install it in the default tools directory
RUN dotnet tool install --global SpecFlow.Plus.LivingDoc.CLI

# Add the .NET global tools directory to the PATH environment variable
# This allows the 'livingdoc' command to be found and executed directly
ENV PATH="$PATH:/root/.dotnet/tools"

# You can define a default command if needed, but we'll use docker-compose
# ENTRYPOINT ["livingdoc"]
# CMD ["--help"]