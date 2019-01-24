#BUILD PHASE  
FROM microsoft/aspnetcore-build:2.0.5-2.1.4-jessie AS build-env  
WORKDIR /app  
COPY *.csproj .  
RUN dotnet restore  
COPY . .  
RUN dotnet publish -c Release -o out  
#RUN PHASE  
FROM microsoft/aspnetcore:2.0.5-jessie  
WORKDIR /app  
COPY --from=build-env /app/out .  
ENTRYPOINT ["dotnet", "WebApplication1.dll"]
