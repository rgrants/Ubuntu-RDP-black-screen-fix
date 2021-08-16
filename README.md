# Ubuntu-RDP-black-screen-fix
sudo -s 
nano /etc/xrdp/startvm.sh
Before:
if test -r /etc/profile; then
          . /etc/profile
Insert: 
unset DBUS_SESSION_BUS_ADDRESS
unset XDG_RUNTIME_DIR
. $HOME/.profile

reboot
