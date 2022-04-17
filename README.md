# Jupyter Service Configuration
Description: ConStart Jupyter notebook/lab service upon boot.

### Prerequisites :
------------------
> **A:** Ensure virtualenv or conda environment are installed and configured. <
>
> **B:** Depending on the method that is used, ensure SSH and other applications (putty, winscp, or etc.) are installed and running. 
>

## Section 1.0 - Creation and Configuration of Jupyter Service 
>Method 1 or method 2 can be used for this Configuration process. Then, follow the Enable and Starting jupyterlab.service section to enable and start the service.
>>
> Few things to before we get started, I named the file jupyterlab.service because I wanted to use juypter lab rather than jupyter notebook.
> If you want to use Jupyter notebook at startup, I would recommend replacing the name of the file from  jupyterlab.service to jupyternotebook.service to help identify > what type of jupyter session excuting the steps in either method 1 or method 2. These steps are still appicable to both jupyterlab and jupyterlab services.
>>
### Method 1 : 
---------
>>
> **1.)** User can download the Jupyter Service file in the jupyter-service in the repository. User will need to modify the following in the jupyter-service file:
>>
> Line 5:
>>
>      User= <Username>
>>
> Line 6:
>>
>      Group= <Username or Group Name>
>>
> Line 8:     
>>
>      WorkingDirectory= <File Path of Directory of WorkSpace>
>>
> Line 9:     
>>
>      ExecStart= <File location of Jupyter Notebook or Lab file> --ip= '<Specified IP Address or * > '  --port= <Specified Port>
>>
> --**NOTE:** Content of the Jupyterlab Service file found here : https://github.com/KompPsy/jupyter-service/blob/main/jupyterlab.service
>>
> **2.)** Copy the jupyter-service file to
>>
>      /etc/systemd/system/
>>
> **3.)** Proceed to step 1 in Section 2.0.1 - Enable and Starting Jupyter Service.
      
### Method 2 :
---------
>>
> **1.)** Enter the following command :
>>
>     sudo vi /etc/systemd/system/jupyterlab.service
>>
> or
>>
>     sudo nano /etc/systemd/system/jupyterlab.service 
>>
> --**NOTE**: User can use either vi or nano commands. Use the editor that is most comfortable :)
>> 
> **2.)** Copy and paste or enter the contents of jupyterlab.service to the editor. Then, save the contents of jupyterlab.service.
>>
> --**NOTE:** Content of the Jupyterlab Service file found here : https://github.com/KompPsy/jupyter-service/blob/main/jupyterlab.serviceContent
>>
> **3.)** Proceed to step 1 in Section 2.0.1 - Enable and Starting Jupyter Service.
      
## Section 2.0 - Jupyter Service Startup Configuration
---------------------------------------
This section configures the service of Jupyter to be excute upon startup in section 2.0.1 and to be removed in section 2.0.2. 
      
### Section 2.0.1 - Enable and Starting Jupyter Service 
---------------------------------------
      
> **1.)** Enter the following commands :
>>
>     sudo systemctl enable jupyterlab.service
>>
>     sudo systemctl start jupyterlab.service
>>
>     sudo systemctl status jupyterlab.service
>>
>> **__Expected Result Output:__** jupyterlab.service - Jupyter Lab Server will show as Active: active (running).
>> 
> --**NOTE:** If jupyterlab.service does not show active and running status proceed to next steps.
>>
### Section 2.0.2 - Disable and Stopping Jupyter Service 
---------------------------------------
> **1.)** Run the the following commands :
>>
> -     sudo systemctl disable jupyterlab.service
> -     sudo systemctl stop jupyterlab.service
> -     sudo systemctl daemon-reload
>>
> **2.)** Reboot system.
>>
> **3.)** After reboot and login, proceed to Enable and Starting jupyterlab.service section step 1.
>>

      
### Contact:
If you have any questions, feel free to reach out:
      PeterAldrichJr@gmail.com


