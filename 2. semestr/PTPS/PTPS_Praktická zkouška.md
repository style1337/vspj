# 1) Instalace Windows serveru

Přesuneme ISO a nebo VHDX soubor do podle zadání 
	Nejspíš to bude na disk E:\ do své složky
	Po spuštění VM nezapomenout zmáčknout klávesu, aby se pustil boot z ISO  
	Jazyk nechat EN  
	Instalace Windows Server 2019 Datacenter Experience

Nastavení admin hesla Password1*

## Postup
### Specify Name nad Location
**Name**:
```
PS2-(váš login)-Win_server_2019  
````
**Lokace**: 
````
E:\PTPS\váš login\ 
````
![](PZ_img/001.png) 
### Specify Generation
````
Generation 2 
````
![[2. semestr/PTPS/PZ_img/Pasted image 20230511141420.png]]
### Assign Memory 
````
4096 MB
````
"Dynamic memory" není potřeba zapíná, když je vypnutá nic to nezmění
![[2. semestr/PTPS/PZ_img/Pasted image 20230511141629.png]]
### Configure Networking
````
Virtual switch nad I219V  
````
![[2. semestr/PTPS/PZ_img/Pasted image 20230511142017.png]]
### Connect Virtual Hard Disk  
Vybereme, **Use an existing virtual hard disk** a uvedeme disk který nám byl poskytnut od učitele většinou se ukládá na **disk E**
````
E:\PS2\váš login\Win_server_2019\Virtual Hard Disks\ 
````
![[2. semestr/PTPS/PZ_img/Pasted image 20230511142617.png]]
Když nebudeme mít disk *(což nepřepokládám)* tak můžeme vytvořit disk možností **Create a virtual hard disk** a uložíme na **disk E do své složky** a **dáme velikost 127 GB**. A v další sekci uvdeme cestu k ISO souboru co jsme dostali od učitele. 
````
E:\Hyper-V\Windows_server_2019.iso
````
![[2. semestr/PTPS/PZ_img/Pasted image 20230511142939.png]]

---
# 2) Instalace Windows (klient)
Úplně to samé jako instalace serveru tady jsou pro případ možný specifikace kdyby se lišili
```
ISO uložit do E:\Hyper-V  
Založit složku E:\PTPS\váš login

Nainstalovat Windows Edu:  
name: PS2-(vaš login)-Win_Edu  
location: E:\PTPS\váš login  
Generation 1  
Memory: 4096  
Use Dynamic memory  
Connected: Virtual switch nad I219V  
Create virtual hard disk  
location: E:\PTPS\váš login\Win_Edu\Virtual Hard Disks\  
Size 127 GB (virtuální - pozor na realné místo na disku e:)  
Install an OS from bootable image:  
E:\Hyper-V\Windows_Edu.iso
```
---
# 3) Nastavení síťových karet
## Server
### Virtual switch síťová karta:
Statická IPv4 adresa:             **192.168.60.100+X/24**        **(X** je číslo tvého PC)
Gateway:                                **192.168.60.254**
DNS1:                                     **192.168.50.165**
![[2. semestr/PTPS/PZ_img/Pasted image 20230511180658.png]]

### Internal síťová karta:
Statická IPv4 adresa:             10.0.0.1/8
![[2. semestr/PTPS/PZ_img/Pasted image 20230511181001.png]]

## Stanice (klient) Windows 10
### Internal síťová karta:
Statická IPv4 adresa:             10.0.0.2/8
![[2. semestr/PTPS/PZ_img/Pasted image 20230511190113.png]]
### MASKA
/8        >          255.0.0.0 -internal
/24      >          25.255.255.0 – virtual switch

---
# 4) Instalace AD včetně DNS – přidání uživatele ‘‘uživatel‘‘ do AD
## Instalace Active Directory (AD)
- **Server manager -> Manage (vlaječka) -> Add roles features -> doinstalovat AD a DNS**
![[2. semestr/PTPS/PZ_img/Pasted image 20230511143919.png]]
![[2. semestr/PTPS/PZ_img/Pasted image 20230511190643.png]]
![[2. semestr/PTPS/PZ_img/Pasted image 20230511190736.png]]
## Nastavení AD
![[2. semestr/PTPS/PZ_img/Pasted image 20230511191027.png]]
**Add a new forest**
A jako **Root domain name** nastavíme 
````
ad.vspj.eit
````
![[2. semestr/PTPS/PZ_img/Pasted image 20230511191140.png]]
## Přidaní uživatele
Active Directory Users and Computers > ad.vspj.eit >Users
![[2. semestr/PTPS/PZ_img/Pasted image 20230512081323.png]]
Příklad vytváření uživatele:
![[2. semestr/PTPS/PZ_img/Pasted image 20230512081406.png]]

]]![[2. semestr/PTPS/PZ_img/Pasted image 20230511145008.png]]![[2. semestr/PTPS/PZ_img/Pasted image 20230511145021.png]]
![[2. semestr/PTPS/PZ_img/Pasted image 20230511145028.png]]
![[2. semestr/PTPS/PZ_img/Pasted image 20230511145049.png]]![[2. semestr/PTPS/PZ_img/Pasted image 20230511145132.png]]
![[2. semestr/PTPS/PZ_img/Pasted image 20230511145140.png]]
![[2. semestr/PTPS/PZ_img/Pasted image 20230511145145.png]]
![[2. semestr/PTPS/PZ_img/Pasted image 20230511145228.png]]
![[2. semestr/PTPS/PZ_img/Pasted image 20230511145238.png]]
## DNS
![[2. semestr/PTPS/PZ_img/Pasted image 20230511173544.png]]
![[2. semestr/PTPS/PZ_img/Pasted image 20230511173553.png]]
![[2. semestr/PTPS/PZ_img/Pasted image 20230511173558.png]]
![[2. semestr/PTPS/PZ_img/Pasted image 20230511173603.png]]
![[2. semestr/PTPS/PZ_img/Pasted image 20230511173608.png]]
Asi 10.0.0

Podle Internal
??

![[2. semestr/PTPS/PZ_img/Pasted image 20230511173647.png]]
![[2. semestr/PTPS/PZ_img/Pasted image 20230511173651.png]]
![[2. semestr/PTPS/PZ_img/Pasted image 20230511173655.png]]
![[2. semestr/PTPS/PZ_img/Pasted image 20230511173658.png]]
![[2. semestr/PTPS/PZ_img/Pasted image 20230511173702.png]]
A zkontrolovat v cmd nslookup

**Napsat nslookup**

**Pak napsat adresu**
![[2. semestr/PTPS/PZ_img/Pasted image 20230511173714.png]]

# 5) Nasdílení složky (home)
````
C:\home\%username%
````
Nasdílení složky  jako domovské složky pro účet ‘‘uživatel‘‘, a nastavení práv RW jen pro tohoto uživatele *(na serveru)*
![[2. semestr/PTPS/PZ_img/Pasted image 20230511145647.png]]
![[2. semestr/PTPS/PZ_img/Pasted image 20230511145656.png]]
![[2. semestr/PTPS/PZ_img/Pasted image 20230511145707.png]]
![[2. semestr/PTPS/PZ_img/Pasted image 20230511145716.png]]
![[2. semestr/PTPS/PZ_img/Pasted image 20230511145723.png]]
- Pak smazat účty
- A nastavit pro uživatelská práva
- Zabezpečení > Upravit > Přidat > Uživatel
![[2. semestr/PTPS/PZ_img/Pasted image 20230511145815.png]]
![[2. semestr/PTPS/PZ_img/Pasted image 20230511145823.png]]
# 6) Nasdílení složky (nějaké společné)
Nasdílení složky a nastavení práv 
````
C:\spolecne 
````
jako společné složky pro domain users pro čtení i zápis
![[2. semestr/PTPS/PZ_img/Pasted image 20230511150030.png]]
![[2. semestr/PTPS/PZ_img/Pasted image 20230511150038.png]]
![[2. semestr/PTPS/PZ_img/Pasted image 20230511150044.png]]
![[2. semestr/PTPS/PZ_img/Pasted image 20230511150048.png]]
![[2. semestr/PTPS/PZ_img/Pasted image 20230511150053.png]]
![[2. semestr/PTPS/PZ_img/Pasted image 20230511150100.png]]
# 7) Mapovaní dříve nakonfiguravaných disků
- Konfigurace mapování home disku H: a společného disku S: pro doménové stanice
## MAPOVÁNÍ HOME disku H: 
Pak zkopírovat **NETWORK PATH/Síťová cesta**:
![[2. semestr/PTPS/PZ_img/Pasted image 20230511150250.png]]
A pak dále v **Active Directory Users and Computers**
Nastavení uživatele
**Profil**
![[2. semestr/PTPS/PZ_img/Pasted image 20230511150338.png]]
**Home folder**
Connect:
````
H:        \\domena\home$\%username%
````
## MAPOVÁNÍ SPOLECNE na disku S:
- Otevřít Group Policy Management
- Vpravým klikni na Group Policy Objects a dát New  *Název: Map drive S*

- Pak pravým na to kliknout a     edit
- Jít do User Configuration > Preferences > Windows Settings > Drive Maps.
- Vpravým kliknout a vybrat  New > Mapped Drive.
- Under the General tab (see Figure 1 below), do the following:

	Action: **Update**.
	Location: \\domena\spolecne.
	Reconnect: **ANO**
	Label as: **spolecne.**
	Drive Letter: **S:**
	Connect as: **NIC NEDAVAT**
	Show this drive:
	Show all drives:

![[2. semestr/PTPS/PZ_img/Pasted image 20230511150644.png]]
PAK v **GROUP POLICY MANAGEMENT**
Pravým na vytvořený GPO Link a Existing GPO a Vybrat Map drive S
**Pak v cmd příkaz gpupdate /force**
# 8) Přihlášení stanice do domény, test přihlášení a mapování síťových disků
# 9) Konfigurace DHCP serveru
````
Konfigurace DHCP serveru pro internal LAN 10.0.0.0/8, server 10.0.0.1, DHCP rozsah 10.0.0.100 až 10.0.0.200, připojení stanice a ověření konektivity na server
````
## Postup
![[2. semestr/PTPS/PZ_img/Pasted image 20230512090103.png]]
![[2. semestr/PTPS/PZ_img/Pasted image 20230512090230.png]]
![[2. semestr/PTPS/PZ_img/Pasted image 20230512090300.png]]
![[2. semestr/PTPS/PZ_img/Pasted image 20230512090344.png]]
![[2. semestr/PTPS/PZ_img/Pasted image 20230512090453.png]]
![[2. semestr/PTPS/PZ_img/Pasted image 20230512090806.png]]
![[2. semestr/PTPS/PZ_img/Pasted image 20230512090906.png]]
### Klient (Windows 10)
![[2. semestr/PTPS/PZ_img/Pasted image 20230512091439.png]]
A pak stačí zkontrolovat v CMD
![[2. semestr/PTPS/PZ_img/Pasted image 20230512091548.png]]
# 10) Instalace ISS
Instalace IIS s podporou ASP, konfigurace ASP skriptu s název index.asp jako výchozího dokumentu webu
````
http://server.kts.vspj.cz/testasp.txt
````

````aspx
<html>
  <head>
    <title>ASP - testovací­ stránka</title>
  </head>
  <body>
    <h1>Ukázka ASP</h1>
    <% for i = 1 to 7 %>
    Radka c. <% = i %>. Obyčejný text.<br>
    <% next %>
    <BR>
    <table>
    <tr>
    <td><b>Server Variable</b></td>
    <td><b>Value</b></td>
    </tr>
    <% For Each name In Request.ServerVariables %>
    <tr>
    <td><% = name %></td>
    <td><% = Request.ServerVariables(name) %></td>
    </tr>
    <% Next %>
    </table>
  </body>
</html>
````
![[2. semestr/PTPS/PZ_img/Pasted image 20230512093920.png]]
![[2. semestr/PTPS/PZ_img/Pasted image 20230512094136.png]]
![[2. semestr/PTPS/PZ_img/Pasted image 20230512095247.png]]
![[2. semestr/PTPS/PZ_img/Pasted image 20230512095343.png]]
![[2. semestr/PTPS/PZ_img/Pasted image 20230512095538.png]]
Zde vytvoříme soubor "index.asp" a vložíme tam ten kod co nám byl poskytnut a pak na na adrese "127.0.0.1" můžeme ověřit jestli nám naše stránka funguje
![[2. semestr/PTPS/PZ_img/Pasted image 20230512095626.png]]
# 11) Konfigurace virtuální webů produkt100.cz
Konfigurace virtuálních webů produkt100.cz (+ www.produkt100.cz) a produkt200.cz (+ www.produkt200.cz) včetně konfigurace A záznamů v DNS

## Nastavená produkt produkt100.cz
![[2. semestr/PTPS/PZ_img/Pasted image 20230512105201.png]]
A pak jsem jen šel do DNS udělal jsou novou zonu "produkt100.cz" nastavil jsem všude jen jméno a jinak jsem všude nechal defualtní hodnoty a pak jsem **přidal záznam A**
![[2. semestr/PTPS/PZ_img/Pasted image 20230512110326.png]]
A pro IP address jsem dal IP adresu serveru což v tomto případě je 10.0.0.1
![[2. semestr/PTPS/PZ_img/Pasted image 20230512110057.png]]
A pak jsem jen zadal do prohlížeče abych otestoval jestli funguje *(ještě potřeba tam vytvořit nějaký dokument v té složce třema index.html a do toho napsat nějaký text)*
![[2. semestr/PTPS/PZ_img/Pasted image 20230512110425.png]]
A tohle celé zopakovat jen pro Produkt200.cz
# 12) Windows serveru jako terminálového serveru pro Domain Users
Konfigurace Windows serveru jako terminálového serveru pro domain users včetně lic. serveru, ukázka přihlášení pro u
živatele uzivatel
## Postup
Nainstalujte službu "Remote Desktop Services" na Windows Serveru
![[2. semestr/PTPS/PZ_img/Pasted image 20230512113341.png]]
![[2. semestr/PTPS/PZ_img/Pasted image 20230512113511.png]]
A pak přidáme třeba našeho vytvořeného uživatele do skupiny Remote Desktop Users
![[2. semestr/PTPS/PZ_img/Pasted image 20230512114114.png]]
## Ověření spojení
Jdeme na klienta (Windows 10). Vyhledáme aplikace Remote Desktop Connection
![[2. semestr/PTPS/PZ_img/Pasted image 20230512114502.png]]
![[2. semestr/PTPS/PZ_img/Pasted image 20230512114523.png]]
Zadáme IP server a uživatele pod kterým se chceme přihlásit *(Já vybral uživatele Administrator)*
![[2. semestr/PTPS/PZ_img/Pasted image 20230512114739.png]]
Dáme heslo uživatele
![[2. semestr/PTPS/PZ_img/Pasted image 20230512114823.png]]
Dáme Yes a mělo by nás to připojit


# 13) Konfigurace Windows serveru jako router 
https://mrigotech.com/windowsserver/win2019/how-to-setup-vpn-using-pptp-on-windows-server-2019/






