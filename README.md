To Clone the repo:
git clone https://github.com/lucasaponso/IOTAvaraHub.git


Install dotnet:




wget https://packages.microsoft.com/config/ubuntu/20.04/packages-microsoft-prod.deb -O packages-microsoft-prod.deb


sudo dpkg -i packages-microsoft-prod.deb


rm packages-microsoft-prod.deb


sudo apt-get update && sudo apt-get install -y dotnet-sdk-6.0


sudo apt-get update && sudo apt-get install -y aspnetcore-runtime-6.0
    

sudo apt-get install -y dotnet-runtime-6.0







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
- az iot hub monitor-events --hub-name PolymerIOT --device-id PolymerDeviceX
