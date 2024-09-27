
**Cryptographie**

 Générer une clef aléatoire
	 `key = Fernet.generate_key()`
 Obtention de l’objet Fernet
	 `fernet = Fernet ( key )`
 Chiffre le contenu d’un fichier
	`with open ( filepath, ‘’rb’’ ) as f :`
	 'encrypted = fernet.encrypt ( f.read() )'

> with open ( filepath, ‘’rb’’ ) as f :	encrypted = fernet.encrypt ( f.read() 



```py
with open ( filepath, ‘’rb’’ ) as f : encrypted = fernet.encrypt ( f.read() )
```





 Déchiffre le contenu d’un fichier
	 `with open ( filepath, ‘’rb’’ ) as f :`
	 `decrypted = fernet.decrypt ( f.read() )`

**Requests**
	Simple requête GET
	 `r = requests.get (’’https://esdacademy.eu’’)`
	
   Requête POST avec envoi de données
	 `r = requests.post`
	```
	(’’https://esdacademy.eu/login’’, data = {
	 username=’’esdmaster’’
	 password=’’2secret4u’’
	 } )
	 ```
	Obtention du code de retour HTTP, des en-têtes de réponse et de la page web
     `status = r.status_code`
     `headers = r.headers`
     `html = r.text`

**Winreg**

 Créer une clef de registre dans HKCU
  `winreg.CreateKey ( winreg.HKEY_CURRENT_USER, REG_PATH )`
 
 Ouvrir une clef de registre en écriture dans HKCU
  `reg_key = winreg.OpenKey ( winreg.HKEY_CURRENT_USER, REG_PATH, 0, winreg.KEY_WRITE )`
 
 Assigner une valeur à une clef de registre
  `winreg.SetValueEx ( registry_key, name, 0, winreg.REG_SZ, value )`
 
 Fermer une clé de registre
  `winreg.CloseKey ( reg_key )`

**Subprocess** 
	
 Démarre un sous process 
 `subprocess.call ('clac.exe')`
 
 Démarre un sous-process dans un shell
 `subprocess.call ( ['dir'], shell = True)`
 
 Renvoie la sortie d'un sous-process
 `subprocess.check_output (['netsh','wlan','show','profiles'])`
 
 Récupération de la sortie erreur 
 `p = subprocess.Popen( ['unknow-command'], stderr = subprocess.PIPE) output = p.stderr.read` 
 
**Scapy** 
 Création d'un packet TPC/IP 
 `packet = IP(dst="192.168.1.24",src="192.168.1.17")/ TCP(dport=443, flags="S")`
 
 Envoi du packet et attente de la réponse 
 `srl(packet)`
 
 Inspection d'un paquet 
 `ls(packet)`
 `packet.show()`
 
 Création d'une requête ARP
 `ARP (pdst = '192.168.1.24',psrc='192.168.1.17')`
 
 Sniffe le traffic TCP sur le port 80 et applique une callback sur chaque paquets capturés 
 `sniff(filter="tcp port 80",prn=callback)`

**Screenshot** 
 Capture d'écran instantanée 
 `screen = pyautogui.screenshot()`
 
 Enregistrement de la capture
 `screen.save (filename)`

**Socket** 
 Création d'un socket TPC 
	`s = socket.socket(socket.AF_INET,socket.SOCK_STREAM)`
	
  Création d'un socket udp
	`s = socket.socket(socket.AF_INET,socket.SOCK_DATAGRAM)`
	
 Se connecte à un socket
	`s.connect ((host,port))` 
	
 Réception de données 
	`s.recv (1024)` 
	
 Envoi de données 
	`s.send (data)` 

 Résolution de nom 
 `socket.gethostname (host_name)`
 
 Récupération du nom d'hôte 
 `socket.gethostbyaddr (host_ip)`

**Win32clipboard**

 Récupère le contenu du presse-papier
 `win32clipboard.OpenClidBoard()`
 `data = win32clipboard.GetClipboardData()`
 `win32clipboard.CloseClipboard()` 
 
 Remplace le contenu du presse-papier
 `win32clipboard.OpenClipboard()` 
 `win32clipboard.EmptyClipboard()`
 `win32clipboard.SetClipboardText(string)`
 `win32clipboard.CloseClipboard()`

