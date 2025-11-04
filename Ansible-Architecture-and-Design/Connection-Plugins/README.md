####  🧩 1. Core Connection Plugins 

| Plugin	| Description
|--- |--- |
| ssh	| Default for most hosts. Uses OpenSSH or paramiko to connect over SSH.
| paramiko	| Python-based SSH (used when ssh binary is unavailable).
| local | 	Runs tasks locally on the Ansible control node (no SSH).
| docker	| Connects to Docker containers via the Docker API.
| podman | 	Connects to containers managed by Podman.
| chroot	| Executes commands in a chroot jail.
| jail | 	Executes inside a FreeBSD jail.
| lxc / lxd | 	Connects to LXC or LXD containers.
| paramiko_ssh	 | Legacy SSH option (rarely used now).
| persistent | 	Used internally for persistent network device sessions.
| local | 	Used when managing the control node itself.


#### 🌐 2. Network Connection Plugins

 | Plugin	 | Used For	| Example ansible_network_os
 |--- |--- |--- | 
 | network_cli | 	CLI-based access via SSH (most network devices).  | 	nxos, ios, eos, asa, junos, etc.
 | httpapi  | 	API-based connection over HTTP/HTTPS.  | 	paloaltonetworks.panos, cisco.ise, f5networks.f5os, etc.
 | netconf	 | Uses NETCONF over SSH. | 	junos, iosxr, nxos (NETCONF-enabled).
 | restconf	 | Uses RESTCONF over HTTP(S). | 	iosxe, iosxr (with RESTCONF enabled).
 | grpc	 | Uses gRPC protocol  | (for some modern devices like Cisco XR).	
 | ansible.netcommon.network_cli	 | Fully-qualified collection path for network_cli.	
 | ansible.netcommon.httpapi	 | Fully-qualified collection path for httpapi.	
 | ansible.netcommon.netconf	 | Fully-qualified collection path for netconf.


#### ☁️ 3. Cloud / API / Special Purpose

 | Plugin  | 	Description
 |--- |--- | 
 | winrm	 | Connects to Windows hosts using Windows Remote Management.
 | psrp	 | PowerShell Remoting Protocol for Windows (alternative to WinRM).
 | kubectl	 | Runs commands in Kubernetes pods using kubectl exec.
 | oc  | 	Runs commands in OpenShift pods using oc exec.
 | smart	 | Automatically chooses between ssh and paramiko depending on availability.


####  🧠 Example Mapping
 | 	Device  | 	Type	Connection Plugin | 	Network OS
 |--- |--- |---|
 | Cisco  NX-OS	 | network_cli	 | nxos
 | Cisco IOS-XE	 | network_cli / httpapi	 | ios or iosxe
 | Cisco ASA	 | network_cli	 | asa
 | Palo Alto Firewall	 | httpapi	 | paloaltonetworks.panos
 | Juniper JunOS	 | netconf	 | junos
 | Arista EOS	 | network_cli / httpapi	 | eos
 | F5 BIG-IP	 | httpapi	 | f5networks.f5_bigip

 
