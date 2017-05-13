wget http://download.qt.io/official_releases/qt/5.7/5.7.0/qt-opensource-linux-x64-5.7.0.run

chmod +x qt-opensource-linux-x64-5.7.0.run ./qt-opensource-linux-x64-5.7.0.run

sudo apt-get install build-essential

sudo apt-get install libfontconfig1

Launch Qt Creator. Go to Tools > Options. Click Build & Run and select tab Kit. Configure a compiler if it is not automatically detected

Set file association with pro files
When installing from the on-line source the file association is not done automatically. It also not show up when you try to associate it with file explorer. Create a file named “Qt-Creator.desktop” and fill the file with the following.

[Desktop Entry] Version=1.0 Encoding=UTF-8 Type=Application Name=QtCreator Comment=QtCreator NoDsiplay=true Exec=(Install folder of QT)/Tools/QtCreator/bin/qtcreator %f Icon=(Install folder of QT)/5.4/Src/qtdoc/doc/images/landing/icon_QtCreator_78x78px.png Name[en_US]=Qt-Creator

Place this file in home .local/share/applications .

Edit a file named “defaults.list” in the same directory . Add the following line.

text/qtcreator=Qt-Creator.desktop;

open file mimeapps.list and check if the following line is present.

application/vnd.nokia.qt.qmakeprofile=qtcreator.desktop

if not add it under [added Associations].

Run the following command.

sudo update-mime-database /usr/share/mime

now Qt has been added to the list of file associations.

https://github.com/grumpbyguy/NicNacCoinwallet.git NicNac

git submodule https://github.com/grumpbyguy/NicNacCoinwallet.git NicNacCoinwallet

mkdir build && cd build && cmake .. && make
