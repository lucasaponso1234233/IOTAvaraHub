To Clone the repo:
git clone https://github.com/lucasaponso/IOTAvaraHub.git


Install dotnet:

//downloading deb file from microsoft
wget https://packages.microsoft.com/config/ubuntu/20.04/packages-microsoft-prod.deb -O packages-microsoft-prod.deb

//installing deb file
sudo dpkg -i packages-microsoft-prod.deb

//removing package after install
rm packages-microsoft-prod.deb

//installing dotnet-sdk
sudo apt-get update && sudo apt-get install -y dotnet-sdk-6.0

//install aspnetcore runtime
sudo apt-get update && sudo apt-get install -y aspnetcore-runtime-6.0
    
//install dotnet runtime
sudo apt-get install -y dotnet-runtime-6.0

//adds the azure package to dotnet
dotnet add package Microsoft.Azure.Devices.Client



Compile & Execute Program:

dotnet run ##(client device)
az iot hub monitor-events --hub-name PolymerIOT --device-id PolymerDeviceX ##(server device)








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
