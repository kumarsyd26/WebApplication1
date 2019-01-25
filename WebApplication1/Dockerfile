FROM microsoft/aspnetcore-build

WORKDIR /app
 
COPY . /app
 
# Run the following commands in Linux Terminal to restore .NET Core packages
RUN ["dotnet", "restore"]
 
# Build the application
RUN ["dotnet", "build"]
 
WORKDIR /app
 
ENTRYPOINT ["dotnet", "WEbApplication1.dll"]
