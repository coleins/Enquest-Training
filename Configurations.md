#COMMASTER INSTALLATION############################################

COMMASTER SETUP_1.14 - Run the commaster setup extracted- blue icon in
ALL COMMASTER DLLS- copy all-paste Bitplus Commaster
LATEST ZEEMKEEPER- copy all from files folder- paste sysWoW64(windows system64)
sdk64- copy all dlls- paste sysWoW64
Auto install-sdk-bat from sysWoW64 (run as admin)
SUPREMA- copy all dlls-paste to sysWoW64
COMMASTER UPDATE VERSION 1.76- copy all folder components- paste in Bitplus Commaster folder
LICENSE HANDLER UPDATE VERSION 1.6_1 - copy all files paste in Bitplus Commaster
APPS- run as admin Commaster.exe/ or in desktop shortcut
Go to licence handler in Bitplus Commaster and stop all services then copy all dlls and paste in Commaster Bitplus folder

EMAIL SETUP#######################################################

open MAIL SETUP- run mail sett.msi
select Everyone in the installation process
MAIL SERVICE UPDATE VERSION 1.5- copy all dlls paste in program86 in C:\Program Files (x86)\Bitplus\Email Service\
In C:\Program Files (x86)\Bitplus\Email Service\ - open scheduler setup run as administrator
open server info to check the server connection and database name, test connection
in the mail settings tick the default checkbox
SMTP Server Name- usually in the format "smtp.domain.com" or "mail.domain.com," though it can vary depending on your email provider.
SMTP Port No- most common SMTP port number is 25. However, other ports like 587 and 465 are also used, especially for secure connections. Port 25 is the traditional default for unencrypted SMTP, while 587 is favored for secure submissions with authentication, and 465 was historically used for SMTPS but is less common now.
SMTP Username- refers to the email address associated with your email account or the specific SMTP credentials provided by your email service provider
The Enable SSL checkbox should only be clicked to test

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

#PAYMASTER DESKTOP INSTALLATION##########################################

Ensure to have both Paymaster 12 setup and TAPA dll folders

Run the paymaster setup (blue icon ). the file path during instalation is Bitplus/paymaster
Copy the TAPA dll folder and paste in the bitplus folder (sibling to paymaster)
Open the Tapa folder and run as admin the BSPLRegKeyDecryptRegistration_64Bit and BitNetPostingRegistration_64Bit
Copy the TAPA dll files to the syswow64 folder in drive C
Pull shortcut from the server by going to the bitplus folder win + R //ip or pc name, if access is limited then look for the paymaster application and pull the shortcut to the desktop

#UPDATE PAYMASTER DESKTOP#################################################
Rename the current paymaster in the bitplus folder
Look for the PayMaster12 Version 12.0.736_1 (36.1) or later
Unzip and copy the paymaster.exe file to the server bitplus folder
