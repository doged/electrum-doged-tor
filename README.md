Electrum-DOGED for TOR - lightweight DogecoinDark client for connecting to the DOGED Tor Electrum Server
------------------------------------------------
![Electrum-DOGED](https://raw.githubusercontent.com/doged/electrum-doged-tor/master/electrumlogo.png)

Licence: GNU GPL v3

Authors: sunerok, bitspill & whit3water

Language: Python

Homepage: http://electrum-doged.space/


1.a) GETTING STARTED WITH UBUNTU/LINUX
------------------
sudo apt-get update

sudo apt-get install tor

now go to /etc/tor/ and edit the torrc file. (you can use sudo nano torrc)

you just need to remove the # before the line that starts with SocksPort 9050

then save torrc, and go back to command prompt and type sudo service tor restart.

now we install the electrum wallet!

sudo apt-get install git pyqt4-dev-tools python-pip python-dev python-slowaes python-pip

sudo pip install pyasn1 pyasn1-modules pbkdf2 tlslite qrcode

git clone https://github.com/doged/electrum-doged-tor && cd electrum-doged-tor

pyrcc4 icons.qrc -o gui/qt/icons_rc.py

sudo python setup.py install

To run Electrum from this directory, just do:
---------------------------------------------
  ./electrum-doged

To start Electrum from your web browser, see
--------------------------------------------
http://electrum-doged.space/DogecoinDark_URIs.html

To update your copy of the electrum client:
-------------------------------------------
cd electrum-doged

git pull

sudo python setup.py install

1.b) GETTING STARTED WITH WINDOWS
------------------

-download this repo as a zip and extract it to where you would like it to run from. 
https://github.com/doged/electrum-doged/archive/master.zip

-download python 2.7 for windows here: https://www.python.org/ftp/python/2.7.10/python-2.7.10.msi

-download Microsoft Visual C++ Compiler for Python 2.7 here: http://www.microsoft.com/en-us/download/confirmation.aspx?id=44266

-download python qt4: http://sourceforge.net/projects/pyqt/files/PyQt4/PyQt-4.11.3/PyQt4-4.11.3-gpl-Py2.7-Qt4.8.6-x64.exe

-then in ms visual studio command prompt, go into the directory electrum-doged:

pyrcc4 icons.qrc -o gui/qt/icons_rc.py

py -m pip install pip pyasn1 pyasn1-modules pbkdf2 tlslite qrcode ecdsa ltc_scrypt pyrcc

py setup.py install

py electrum-doged



2. HOW OFFICIAL PACKAGES ARE CREATED
------------------------------------

python mki18n.py

pyrcc4 icons.qrc -o gui/qt/icons_rc.py

python setup.py sdist --format=zip,gztar

On Mac OS X:

  # On port based installs
  
  sudo python setup-release.py py2app

  # On brew installs
  
  ARCHFLAGS="-arch i386 -arch x86_64" sudo python setup-release.py py2app --includes sip

  sudo hdiutil create -fs HFS+ -volname "Electrum-DOGED" -srcfolder dist/Electrum-DOGED.app dist/electrum-doged-VERSION-macosx.dmg


[![Visit our IRC Chat!](https://kiwiirc.com/buttons/irc.freenode.net/dogecoindark.png)](https://kiwiirc.com/client/irc.freenode.net/?nick=doged|?&theme=cli#dogecoindark)
