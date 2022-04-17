# jupyter-service
Start Jupyter notebook/lab service upon boot.
--> NOTE: User will need to will need to pre-create the service file then transfer jupyterlab.service to /etc/systemd/system or
--> use the following command : sudo vi /etc/systemd/system/jupyterlab.service or sudo nano /etc/systemd/system/jupyterlab.service then enter or paste
--> the file contents text in the vi/nano editor. Save the contents of jupyterlab.service.
--> Lastly, enter the following command:
--> 1. sudo systemctl enable jupyterlab.service
--> 2. sudo systemctl start jupyterlab.service
--> 3. sudo systemctl status jupyterlab.service
--> Expected Result : jupyterlab.service shows active and running status.
--> Note: If jupyterlab.service does not show active and running status proceed to next steps.
--> 4: Run the the following commands
-->     a. sudo systemctl disable jupyterlab.service
-->     b. sudo systemctl stop jupyterlab.service
-->     c. sudo systemctl daemon-reload
-->     d. Reboot system
-->     e. After reboot and login, proceed to step 1.


