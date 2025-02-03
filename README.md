# Margam-Park-Archives-Install-From-Here
Download the files required to install the Margam Park Archives application.

Installation instructions:
1. Log in to the computer with a **standard user account** (not an admin user). The application should be accessible to the public on a standard user account to ensure they cannot directly access the database files in the file explorer. Note you will need to enter the administrator password several times throughout these steps.
2. Install the Visual Studio Redistributable (required for MySQL installation):
    1. Go to the Microsoft website and download the **x64 version**. [Visit  Microsoft Download Webpage](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170&form=MG0AV3#latest-microsoft-visual-c-redistributable-version)
    2. Open the downloaded file and follow the installation steps. If it is already installed, the installer will tell you.
3. Install MySQL Community Server 8.4.4:
    1. Download the **MSI installer** for **MySQL Community Server 8.4.4 (LTS)** [Visit MySQL Download Webpage](https://dev.mysql.com/downloads/mysql/).
    2. Open the installer and follow the setup process using all default options. When prompted, choose the **Typical** setup option.
    3. When the MySQL installation is complete, open the **MySQL Configurator** by ticking the box at the end of the installer dialog or opening it from the start menu.
    4. Click Next to continue to the Data Directory screen. Choose a location on the computer (not an external hard drive) where the database will be stored. The default location will be fine.
    5. On the Type and Networking screen, choose **Server Computer**. Make sure that the TCP/IP option is ticked. Check the “Show Advanced and Logging Options” box. Now click Next.
    6. On the Accounts and Roles screen, **enter a root password and write it down** somewhere. You will need to use this password later. Click Next.
    7. On the Windows Service screen, leave all options as the defaults then click Next.
    8. On the Server File Permissions screen, leave the default option selected (yes, grant full access to the user running the Windows Service...), then click Next.
    9. On the Logging Options screen, tick Query Log and Binary Log. 
    10. On Advanced Options, click Next and on Sample Databases, click Next.
    11. Finally, click Execute and wait for the configurator to finish.
4. Add MySQL to the system path variable:
    1. Open File Explorer from the Start menu.
    2. Navigate to ```This PC > C: > Program Files > MySQL > MySQL Server 8.4 > bin```.
    3. Click on an empty part of the address bar and copy the folder path.
    4. Go to the search box next to the start menu and type "Environment Variables", then open **Edit the system environment variables**.
    5. Click the **Environment Variables...** button at the bottom.
    6. Under **System variables**, find the variable called **"Path"**, click it then click the **Edit** button below.
    7. Click **New** then paste the folder path you copied, then press Enter.
    8. Press OK, then OK, then OK again to apply the changes and close all the dialog boxes.
5. Run database setup scripts:
    1. Download the **database_setup_31_01_25.zip** folder from this respository using the following link. [Download database_setup_31_01_25.zip](https://richard2706.github.io/Margam-Park-Archives-Install-From-Here/database_setup_31_01_25.zip)
    2. Right click the downloaded zip folder, click Extract All, then click Extract.
    3. Open the extracted folder and open the file **run_database_setup_31_01_25.bat**.
    4. Enter the root password for the database. You created this in step 3.6.
    5. If there are no error messages in the command line window, then the database should now be set up correctly and you can close the command line window.
6. Install the certificate for the application. You must download and trust the certificate in order to use the application.
    1. If you have already installed this certificate (for example, if you installed the [Test Application](https://github.com/richard2706/WinUI-3-MSIX-Test-App-Install-From-Here)), you can skip this section.
    1. Download the certificate from this repository using the following link. [Download certificate](https://richard2706.github.io/Margam-Park-Archives-Install-From-Here/MargamParkArchives_1.0.0.0_x64_Test/MargamParkArchives_1.0.0.0_x64.cer)
    2. Right click on the downloaded file then select **Install Certificate**.
    3. Click Open if prompted.
    4. In the Certificate Import Wizard, select *Local Machine* as the Store Location, then click Next.
    5. If prompted, in the User Account Control dialog, click Yes.
    6. Select *Place all certificates in the following store*, then click Browse.
    7. Select *Trusted Root Certification Authorities*, then click OK.
    8. Click Next, then click Finish, then click OK.
7. Install Margam Archives Windows application
    1. Download the app installer from this repository using the following link. [Download app installer](https://richard2706.github.io/Margam-Park-Archives-Install-From-Here/MargamParkArchives_x64.appinstaller)
    2. Open the downloaded installer file, then click Install.
    3. The app is now installed and should update automatically. Open the app from the Start menu.
