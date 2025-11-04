####  🧩 1. Core Connection Plugins 

| Plugin	| Description
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
