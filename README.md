# jupyter-service
Start Jupyter notebook/lab service upon boot.
## Configuration of Jupyter Service
Method 1 or method 2 can be used for this Configuration process. Then, follow the Enable and Starting jupyterlab.service section to enable and start the service.

>>
Method 1: 
---------
>>
1. User will need to will need to pre-create the service file then transfer jupyterlab.service to /etc/systemd/system.
>>
Method 2:
---------
>>
1. Enter the following command : 
-     sudo vi /etc/systemd/system/jupyterlab.service
or
-     sudo nano /etc/systemd/system/jupyterlab.service 
>>
--**Note**: You can use either nano or vi commands. Use the editor you are comfortable with :) 
>> 
2. Copy and paste or enter the contents of jupyterlab.service to the editor. Then, save the contents of jupyterlab.service.
      Content of the Jupyterlab Service found here : https://github.com/KompPsy/jupyter-service/blob/main/jupyterlab.service
>>
Enable and Starting jupyterlab.service
---------------------------------------
1. Enter the following commands :
-     sudo systemctl enable jupyterlab.service
-     sudo systemctl start jupyterlab.service
-     sudo systemctl status jupyterlab.service
      Expected Result : jupyterlab.service - Jupyter Lab Server will show as Active: active (running).
>> 
--**Note:** If jupyterlab.service does not show active and running status proceed to next steps.
>>
Disable and Stopping jupyterlab.service
---------------------------------------
1. Run the the following commands :
>>
-     sudo systemctl disable jupyterlab.service
-     sudo systemctl stop jupyterlab.service
-     sudo systemctl daemon-reload
>>
2. Reboot system.
3. After reboot and login, proceed to Enable and Starting jupyterlab.service section step 1.
>>

>>If you have any questions, please reach out : PeterAldrichJr@gmail.com


