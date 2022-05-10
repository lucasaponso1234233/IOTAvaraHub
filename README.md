Install Dependecies:


- Microsoft.Azure.* (using dotnet via CLI)
  dotnet add package Microsoft.Azure.Devices.Client


Enviroment Setup:

- mkdir IOTAvaraHub
- cd IOTAvaraHub
- dotnet new console


Develop the code:
- use primary connection string (can be found under IOTAvaraHub/Devices/AvaraDevice1/)
- uses two initial constants (double minTemperature = 20;
     double minHumidity = 60;) and randomises the values every second.
     
- the values are then printed in the CLI which displays the time it was recorded, the temperature and the humidity. 
- 

Execute the binary:
- by using dotnet run


Check Server Responsiveness by using the Azure cloud shell (watch the data flow into the server):
- az iot hub monitor-events --hub-name AvaraIOTHub --device-id AvaraDevice1
