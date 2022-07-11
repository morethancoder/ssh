# how to ssh into linux machine

## step one

installing the openssh package in case its not installed

this step will depend on your linux distribution for me its arch

```
    sudo pacman -Syy
    sudo pacman -S openssh
```

## step two

editing configuration file with nano

if you dont have nano installed just run `sudo pacman -S nano`
then open the config file in the etc directory

```
sudo nano /etc/ssh/sshd_config
```

in the nano editor uncomment `port 22` remove 22 and write port you like
or leave at 22 its not recommended !

## step three

enabling the ssh service on startup and starting it

```
sudo systemctl enable sshd.service
sudo systemctl start sshd.service
```

## step four

get your ip address for the machine you are trying to ssh into
by running the command `ip addr`

## step five

from any other linux you can connect by simply typing the ssh command with
the user@<ip address> and the port of the machine you want to ssh into

```
ssh -v user@<ip address> -p <port>
```

## final step

like and follow or star this repository 💙
