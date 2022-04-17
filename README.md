# jupyter-service
Start Jupyter notebook/lab service upon boot.
>- Method 1: 
>>- Step 1: 
>>- User will need to will need to pre-create the service file then transfer jupyterlab.service to /etc/systemd/system.


>- Method 2:
>>- Enter the following command : 
>>- You can use either nano or vi commands. Use the editor you are comfortable with :) 
>>-     sudo vi /etc/systemd/system/jupyterlab.service
>> or
>>-     sudo nano /etc/systemd/system/jupyterlab.service 
>>- Copy and paste or enter the contents of jupyterlab.service to the editor. Then, save the contents of jupyterlab.service.


Enable and Starting jupyterlab.service
>>Lastly, enter the following command:
>>-     sudo systemctl enable jupyterlab.service
>>-     sudo systemctl start jupyterlab.service
>>-     sudo systemctl status jupyterlab.service
>>- Expected Result : jupyterlab.service shows active and running status.
>>- Note: If jupyterlab.service does not show active and running status proceed to next steps.
Disable and Stoping jupyterlab.service
>>- Run the the following commands
>>-     sudo systemctl disable jupyterlab.service
>>-     sudo systemctl stop jupyterlab.service
>>-     sudo systemctl daemon-reload
>>- Reboot system
>>- After reboot and login, proceed to Enable and Starting jupyterlab.service section


