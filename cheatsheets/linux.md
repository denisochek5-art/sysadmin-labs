whoami
id
groups
getent passwd denis
getent group sudo

sudo adduser user1
sudo usermod -aG sudo user1
sudo deluser user1
sudo passwd user1
sudo passwd -l user1   # lock
sudo passwd -u user1   # unlock
ls -la
stat file
chmod 644 file
chmod 755 dir
chmod -R 750 dir
chown user:group file
chown -R user:group dir
umask
systemctl status ssh
sudo systemctl start ssh
sudo systemctl stop ssh
sudo systemctl restart ssh
sudo systemctl enable ssh
sudo systemctl disable ssh
systemctl is-enabled ssh
systemctl list-units --type=service --state=running
journalctl -xe
journalctl -u ssh --no-pager
journalctl -u ssh -n 100
journalctl --since "today"
journalctl --since "2026-01-18 10:00" --until "2026-01-18 12:00"
