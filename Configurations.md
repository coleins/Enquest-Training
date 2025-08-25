# EMAIL SETUP

1. open MAIL SETUP- run mail sett.msi
2. select Everyone in the installation process
3. MAIL SERVICE UPDATE VERSION 1.5- copy all dlls paste in program86 in C:\Program Files (x86)\Bitplus\Email Service\
4. In C:\Program Files (x86)\Bitplus\Email Service\ - open scheduler setup run as administrator
5. open server info to check the server connection and database name, test connection
6. in the mail settings tick the default checkbox
7. SMTP Server Name- usually in the format "smtp.domain.com" or "mail.domain.com," though it can vary depending on your email provider.
8. SMTP Port No- most common SMTP port number is 25. However, other ports like 587 and 465 are also used, especially for secure connections. Port 25 is the traditional default for unencrypted SMTP, while 587 is favored for secure submissions with authentication, and 465 was historically used for SMTPS but is less common now.
9. SMTP Username- refers to the email address associated with your email account or the specific SMTP credentials provided by your email service provider
10. The Enable SSL checkbox should only be clicked to test
11. Password is generated from the app password in google settings after enabling 2FA

| **Email Provider**      | **SMTP Server Name**                | **Port (TLS/STARTTLS)** | **Port (SSL)**   |
| ----------------------- | ----------------------------------- | ----------------------- | ---------------- |
| Gmail                   | `smtp.gmail.com`                    | 587                     | 465              |
| Yahoo Mail              | `smtp.mail.yahoo.com`               | 587                     | 465              |
| Outlook / Hotmail       | `smtp.office365.com`                | 587                     | N/A              |
| Microsoft 365           | `smtp.office365.com`                | 587                     | N/A              |
| Zoho Mail               | `smtp.zoho.com`                     | 587                     | 465              |
| iCloud Mail             | `smtp.mail.me.com`                  | 587                     | 465              |
| AOL Mail                | `smtp.aol.com`                      | 587                     | 465              |
| ProtonMail (via Bridge) | `127.0.0.1` (through Proton Bridge) | Custom by Bridge        | Custom by Bridge |
| Yandex Mail             | `smtp.yandex.com`                   | 587                     | 465              |
| Mail.com                | `smtp.mail.com`                     | 587                     | 465              |
| GMX Mail                | `smtp.gmx.com`                      | 587                     | 465              |
| FastMail                | `smtp.fastmail.com`                 | 587                     | 465              |

# PAYMASTER DESKTOP INSTALLATION

1. Ensure to have both Paymaster 12 setup and TAPA dll folders

2. Run the paymaster setup (blue icon ). the file path during instalation is Bitplus/paymaster
3. Copy the TAPA dll folder and paste in the bitplus folder (sibling to paymaster)
4. Open the Tapa folder and run as admin the BSPLRegKeyDecryptRegistration_64Bit and BitNetPostingRegistration_64Bit
5. Copy the TAPA dll files to the syswow64 folder in drive C
6. Pull shortcut from the server by going to the bitplus folder win + R //ip or pc name, if access is limited then look for the paymaster application and pull the shortcut to the desktop

## UPDATE PAYMASTER DESKTOP

1. Rename the current paymaster in the bitplus folder
2. Look for the PayMaster12 Version 12.0.736_1 (36.1) or later
3. Unzip and copy the paymaster.exe file to the server bitplus folder

### reindex db in paymaster enquest

EXEC sp_MSforeachtable @command1="print '?' DBCC DBREINDEX ('?', ' ', 80)"
enter this query on the sql right click, new query paste

# COMMASTER INSTALLATION

Files: Commaster Setup, Commaster Update 1.79

## COMMASTER SETUP_1.14

Run the commaster setup extracted- blue icon

## ALL COMMASTER DLLS

copy all-paste Bitplus Commaster

## LATEST ZEEMKEEPER

copy all from files folder- paste sysWoW64(windows system64)

## sdk64

copy all dlls- paste sysWoW64
Auto install-sdk-bat from sysWoW64 (run as admin)

## SUPREMA

copy all dlls-paste to sysWoW64

## COMMASTER UPDATE VERSION 1.76

copy all folder components- paste in Bitplus Commaster folder

## LICENSE HANDLER UPDATE VERSION 1.6_1

copy the files to commaster folder, run licence Service handle, stop all services then copy all files paste in Bitplus Commaster then restart the services after running licence handler as admin

## APPS

run as admin Commaster.exe/ or in desktop shortcut

## JANSEN LICENSE ERROR RESOLUTION

1. stop and uninstall the license service handler in bitplus commaster
2. rename the commaster xml file
3. copy and paste latest commaster, latest license service handler, latest Commaster.lic
4. Delete any file with the name tappscomm

# Port that needs to be opened on this network for us to access the punching data from remote machines

Installation and configuration is done. Input username: admin to login to Commaster

1. Enquest: port 2021
2. Paymaster: port 2026
3. EnquestHCM Mobile API: port 2031
4. MailService API: port 2025
5. Paymaster web API: port 2027
6. commaster port for adms communication: random not used

# COMMASTER DEVICE SETUP

## Company Info

1. Go to general and fill the info short name, code, and company name and save
2. Click on Database enter sql credentials for the server where commaster is hosted
3. Database name is COMMASTER, enter username e.g sa and sql password
4. select mixed mode and save

## General Settings

### Comapny settings

close form after save
clear attendancelogdata while downloading

### Employee settings

sql details
database name CO1
sa
password

## Device setup Face Pro

### ADMS service setting

enter server ip
enter port random 6060
create file

## Node Setup

1. select node type
2. model fingerprint- BioSH5000 facepro- face pro
3. node name (as advised by client)
4. communication (NETWORK)
5. node id 1 0r 2 0r 3 etc
6. 7. ip address (unused ip address within the network)
7. port no (4370)
8. used for (in/out)
9. active yes
10. serial number(from the device)

adms -face pro only

# MOUNTING DEVICE TO WALL

To mount the eSSL AiFace Mars (a biometric facial recognition attendance system) to the wall, follow these general steps. This guide is based on typical mounting methods used for eSSL biometric devices like the AiFace series.

🔧 What You’ll Need
Mounting bracket (usually included in the box)

Screws and wall plugs (typically provided)

Drill with appropriate bits

Screwdriver

Spirit level (optional but recommended)

Pencil/marker for marking

Wall anchors (if mounting on concrete or plaster)

🛠️ Step-by-Step Mounting Instructions

1. Unbox and Identify Components
   Ensure you have:

AiFace Mars device

Wall mounting bracket

Screws & plugs

Power adapter or POE cable (based on your setup)

2. Choose the Wall Location
   Mount the device at face height (~1.4 to 1.6 meters from the ground).

Ensure good lighting and avoid strong backlight or direct sunlight.

Ensure the surface is flat and solid (drywall, concrete, wood, etc.)

3. Mark the Mounting Holes
   Take the mounting bracket.

Hold it against the wall where you want to install the device.

Use a pencil to mark the positions of the screw holes.

Use a spirit level to ensure it’s aligned horizontally.

4. Drill Holes
   Drill holes at the marked points.

If mounting on concrete or plaster, insert wall plugs.

5. Attach the Bracket
   Fix the mounting bracket to the wall using the provided screws.

Ensure it's tightly secured.

6. Connect the Wiring
   Connect power (DC adapter or POE).

Connect network cable (LAN).

Connect any other optional wiring (access control, exit button, door lock, etc.)

⚠️ Tip: Ensure power is OFF while connecting wires.

7. Mount the Device
   Slide or clip the AiFace Mars onto the wall bracket as per the design.

Secure it using screws or latch provided on the bracket.

8. Power On and Configure
   Once mounted and wired, turn on the device.

Follow the screen instructions or connect via web to configure IP, time, users, etc.
