GENTOO headless + SKYPE + XVFB + VNC + SIPTOSIS + BITLBEE + ZNC 

This is my Gentoo init script for Skype for my headless computer...
It run SipToSis for call forwarding to a sip protocol and bitlbee
for chat message (and Znc to be always online)...

I publish this script to keep a backup copy, and in the hope that it 
will be a starting point for someone ... I think it needs some changes 
to be adapted to your environment...

Software needed for this script:
- net-im/skype (with -qt-static USE if you want use Dbus then Bitlbee)
- x11-base/xorg-server (with xvfb USE)
- x11-misc/x11vnc
- x11-wm/wm2 (or other windows manager)
- sys-apps/dbus (I think it's already installed as a dependency)
- net-im/bitlbee (whit skype USE)
- net-irc/znc
- SipToSis http://www.mhspot.com/sts/siptosis.html (is not in portage, 
	installed locally. Clearly requires the JVM to run...)
- bindhack http://daniel-lange.com/software/bindhack.c ( OPTIONAL - I 
	use it to force Skype to use a specific IP address...)

Other notes:
- I place skyped in home dir (I have little modified it), this is 
	normally located in /usr/bin/skyped
- DBUS_TMP is a temporary file, necessary due to of the odious 
	functioning of dbus-launch 
- Stopping skyped will kill all python2.7 for user... (for my 
	enviroinment is needed the the python interpeter)


I know, the script can be made much more elegant... but it works, 
I have no feel like to change it... 

I hope it will be useful...
				
					Doom5 

