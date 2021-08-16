# Ubuntu RDP black screen fix
```bash
sudo -s 
```
```bash
nano /etc/xrdp/startvm.sh
```
Before:

```bash
if test -r /etc/profile; then
          . /etc/profile
```
Insert: 

```bash
unset DBUS_SESSION_BUS_ADDRESS
unset XDG_RUNTIME_DIR
. $HOME/.profile
```

```bash
reboot
```
