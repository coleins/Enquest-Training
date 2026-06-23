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

12 If chain cert 1, root 1, and chain cert 3 are missing on my domain SSL certificate what should i do- If your domain is missing intermediate or root certificates, it means your SSL chain is incomplete, which can cause trust errors in certain browsers and devices.To fix this:Do not install the Root (Root 1): Root certificates are pre-installed in the user's device. Including them can actually cause errors.Download the missing Intermediate (Chain 3): Fetch the exact intermediate bundle required by your Certificate Authority (CA).Update your server: Concatenate your domain certificate and the intermediate certificate into a single file and upload it to your web server. Follow the steps below to pinpoint and resolve the issue:1. Verify Your SSL ChainBefore making changes, use an online checker like SSL Shopper or Qualys SSL Labs to test your domain. This confirms exactly which certificates are missing or incorrectly configured.2. Obtain the Missing Intermediate CertificateIf "Chain Cert 3" is an intermediate/chain certificate, you must download it from your CA.Go to your Certificate Authority's support or certificate download page (e.g., Sectigo, Let's Encrypt, DigiCert, or GlobalSign).Download the exact intermediate/ca-bundle certificate that corresponds to the specific root certificate signed by your CA. 3. Install and Reconfigure on Your ServerYour web server requires the complete chain to serve clients correctly. Here is how to update it depending on your platform:For NginxYou need to create a chained certificate that combines your site certificate and the intermediate certificate.Open your terminal and run a command to append the intermediate to your site certificate:cat your_domain.crt intermediate_cert.crt > chained_cert.crtUpdate your Nginx configuration file (/etc/nginx/nginx.conf or your specific site config) to use this new chained file:ssl_certificate /path/to/chained_cert.crt;Restart Nginx: For Windows IISOpen IIS Manager, click on your server name, and double-click Server Certificates.If the intermediate is missing, you may need to right-click and import it into the Intermediate Certification Authorities store.Re-bind the SSL certificate to your domain using the updated intermediate trust. Why the SMTP Test FailsTrust Verification Broken: When your mail client or an external server tries to connect to your SMTP server over TLS/SSL (usually ports 465 or 587), it requests your server's certificate.Handshake Failure: Because the intermediate certificate ("Chain Cert 3") is missing, the connecting client cannot link your domain's certificate back to a trusted root.Security Block: The SMTP client views your connection as untrusted or insecure, throwing an error like SSL routines:ssl3_get_server_certificate:certificate verify failed or Unknown CA, and immediately terminates the test.

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

## COMMASTER UPDATE VERSION 1.79

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

# DEVICE MOUNTING WHAT TO CONSIDER

Here’s a complete checklist of what to consider during a site visit before installation 👇

🏗️ 1. Location & Mounting Surface

✅ Check wall type – Is it concrete, brick, or drywall?

Use appropriate screws and wall plugs for each.

Avoid weak walls or surfaces that vibrate.

✅ Flatness – Ensure the wall is flat for proper alignment.

✅ Height – Ideal mounting height: 1.4 – 1.6 meters from the floor (average adult face height).

✅ Accessibility – Position it where users can easily face the device without stretching or bending.

☀️ 2. Lighting Conditions

✅ Avoid direct sunlight or bright backlight — this causes face detection failure.
✅ Ensure uniform ambient lighting — especially for indoor installations.
✅ If outdoors, ensure the area is shaded or has a canopy.

⚡ 3. Power Supply

✅ Check power source proximity – Device requires 12V DC (or POE if supported).
✅ Confirm stable power – voltage fluctuations can damage the unit.
✅ Consider UPS backup if the site experiences frequent power cuts.
✅ Plan cable routing for safety and neatness.

🌐 4. Network Connectivity

✅ Verify LAN port availability or Wi-Fi signal strength (if wireless).
✅ Use shielded Ethernet cables (Cat5e or Cat6).
✅ Ensure network connection to the attendance server or router is reliable.
✅ Confirm IP addressing plan (static IP preferred).

🔒 5. Access Control Requirements (if applicable)

If the device will control doors or gates:

Identify door strike lock or magnetic lock compatibility.

Check wiring path for exit button, door sensor, and alarm if needed.

Ensure a metal back box or conduit is available for protection.

🌧️ 6. Environmental Conditions

✅ Temperature and humidity within device limits (usually 0°C–45°C, < 80% humidity).
✅ If outdoor installation:

Use weatherproof casing or shade.

Protect from rain, dust, and direct heat.

📶 7. User Flow & Positioning

✅ Ensure users can stand directly in front of the camera (30–80 cm) without crowding.
✅ Avoid placing the device:

Near mirrors, glass walls, or reflective surfaces.

Where people walk too fast past it (e.g., busy corridors).

🔧 8. Cabling & Conduit Path

✅ Identify shortest, safest cable route (power + network + access control lines).
✅ Confirm conduit availability for protection and neatness.
✅ Keep power and network cables separate to reduce interference.

🧱 9. Mounting Hardware

✅ Confirm you have:

Mounting bracket

Template sticker

Screws and plugs

Screwdriver/drill bits

📋 10. Documentation & Configuration

✅ Note:

Device serial number

Network details (IP, gateway, etc.)

Integration requirements (server IP, ETIMETRACK, etc.)
✅ Confirm with client:

Who will manage user enrollment

How logs will sync (LAN/Cloud)

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

During relocation of db commaster if it is not bringing the option to connect to an existing db Comm_Master.xml and reopen commaster.exe
During relocation of TA if not displaying years to the current as per the old server, check the shortcut you are running

# HRMS OLD RELOCATION

1. Copy HRMS and HRMS APPS from the old server(check IIS to see folder path)
2. Host on iis using the same ports as from the old server
3. Rename the WebHRcompany xml file in the APPS DATA folder in HRMS (could not have the name xml at the end)
4. Enter database info(connect to existing database)

msvbvm50 run as admin on the machine with the error when viewing attendance register

# LOOPBACK NAT (mobile app)

Loopback NAT (also known as NAT hairpinning, NAT reflection, or hairpin NAT) is a network feature that allows devices inside a private network (LAN) to access a public IP address (usually their own) and have the traffic correctly routed back into the same internal network.

Let’s break that down clearly 👇

🧩 Typical NAT Scenario

Normally, NAT (Network Address Translation) translates private IPs (like 192.168.1.10) to a public IP (like 41.89.77.10) when sending traffic to the internet.

However, if a device inside the LAN tries to access a public service hosted on the same network (e.g. a website or mail server using the same public IP), NAT might not know how to route that packet — because it appears as if it’s trying to reach the public IP from inside.

💡 What Loopback NAT Does

Loopback NAT makes that possible by “reflecting” the traffic back into the LAN.

It works like this:

A user inside the LAN (e.g. 192.168.1.20) tries to reach 41.89.77.10:80 (the public IP of their own router).

The router sees the destination is its own external IP, and instead of sending it to the internet, it:

Translates the destination (41.89.77.10) to the internal IP of the server hosting the service (e.g. 192.168.1.100).

Forwards the packet internally.

The internal server (192.168.1.100) replies, and the router does the reverse NAT translation so the client sees the response as coming from 41.89.77.10.

⚙️ Example

Let’s say you have:

Router public IP: 41.89.77.10

Internal web server: 192.168.1.100

Port forward: 41.89.77.10:80 → 192.168.1.100:80

Without loopback NAT, if a LAN user (192.168.1.20) tries to access http://41.89.77.10, the connection fails because the router doesn’t know to send it back inside.

With loopback NAT enabled, the router “hairpins” the traffic:

192.168.1.20 → 41.89.77.10:80 → NAT → 192.168.1.100:80
192.168.1.100 → response → NAT → 192.168.1.20

The internal user successfully reaches the internal web server using the external address.

To test if a public IP is accessible after performing Loopback NAT, you need to check two things separately:

Is the public IP reachable from OUTSIDE the network?

Can devices INSIDE the LAN access the service using the public IP (loopback NAT working)?

Below is a clean, professional checklist you can use for testing.

✅ 1️⃣ Test From Outside the Network (Public Reachability Test)

This confirms that port forwarding and the public IP are properly accessible from the internet.

✔ Method 1: Use your phone on mobile data (NOT Wi-Fi)

Turn off Wi-Fi on your phone.

Open a browser and enter:

http://<public-ip>:<port>
e.g. http://41.89.xx.xx:9090

If the service opens, the public IP is accessible externally.

✔ Method 2: Use an online port-check tool

Sites like:

Open Port Checker

YouGetSignal Port Checker

Enter:

Public IP

Port (e.g., 9090)

If the tool reports "Open", external access is working.

✅ 2️⃣ Test From Inside the Network (Loopback NAT Test)

This verifies whether LAN devices can access the internal server using the public IP.

✔ Method 1: Browser Test (Most common)

On any PC connected to the same LAN, open:

http://<public-ip>:<port>
e.g. http://41.89.xx.xx:9090

If the page or app opens, loopback NAT is working.

✔ Method 2: Ping Test

If the router allows ICMP (some don’t):

ping <public-ip>

If replies come back, the router responds correctly (but this does NOT confirm port forwarding).

✔ Method 3: Use Telnet/Nc to test open ports

Example:

telnet <public-ip> <port>
e.g. telnet 41.89.xx.xx 9090

If the screen clears or gives a connected message:

Connected to 41.89.xx.xx

Loopback NAT + port is working.

🔍 3️⃣ Confirm That Loopback NAT Is Actually Being Used

On the internal device (PC):

Run:

curl -I http://<public-ip>:<port>

If you get HTTP headers, loopback NAT is successful.

Example output:

HTTP/1.1 200 OK
Server: nginx

🟢 If Everything Works: Expected Results
Test Expected Outcome
External mobile test App opens
Online port checker Port shows as open
LAN browser test App loads via public IP
Telnet from LAN → public IP Connects successfully

If all these pass → Loopback NAT is correctly configured.

🔴 If Loopback Fails but External Works

Then:

Your router does not support NAT hairpinning, OR

The LAN → LAN NAT (MASQUERADE) rule is missing.

You can send me:

Router type (e.g., Mikrotik, Fortigate, Cisco, TP-Link)

Port

Public IP

Internal server IP

…and I will generate the correct working NAT rules for you.
