Install Dependecies:


- Microsoft.Azure.* (using dotnet via CLI)
  dotnet add package Microsoft.Azure.Devices.Client


Enviroment Setup:

- mkdir IOTAvaraHub
- cd IOTAvaraHub
- dotnet new console


Develop the code:
- use primary connection string (can be found under IOTAvaraHub/Devices/AvaraDevice1/)

Execute the binary:
- by using dotnet run


Check Server Responsiveness by using the Azure cloud shell:
- az iot hub monitor-events --hub-name AvaraIOTHub --device-id AvaraDevice1
