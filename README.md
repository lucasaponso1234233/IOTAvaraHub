Can only be run on an ubuntu system atm.

To Clone the repo:
git clone https://github.com/lucasaponso/IOTAvaraHub.git


Execute dotnet install script:

./dotnet-install.sh




Compile Program:

dotnet run

View Data:

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
