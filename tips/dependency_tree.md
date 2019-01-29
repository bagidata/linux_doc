```
user@hostname:~$ sudo apt install apt-rdepends
[sudo] password for user: 
Reading package lists... Done
Building dependency tree       
Reading state information... Done
The following packages were automatically installed and are no longer required:
  libboost-program-options1.58.0 libfreetype6:i386 libfuse2:i386 libjs-modernizr
  libjs-underscore libllvm4.0 libllvm5.0 libpng12-0:i386 libqt4-help libqt4-scripttools
  libqt4-test libqtassistantclient4 python-qt4 python-sip xxdiff
Use 'sudo apt autoremove' to remove them.
The following NEW packages will be installed:
  apt-rdepends
0 upgraded, 1 newly installed, 0 to remove and 0 not upgraded.
Need to get 13,7 kB of archives.
After this operation, 65,5 kB of additional disk space will be used.
Get:1 http://id.archive.ubuntu.com/ubuntu xenial/universe amd64 apt-rdepends all 1.3.0-5 [13,7 kB]
Fetched 13,7 kB in 2s (4.583 B/s)     
Selecting previously unselected package apt-rdepends.
(Reading database ... 282990 files and directories currently installed.)
Preparing to unpack .../apt-rdepends_1.3.0-5_all.deb ...
Unpacking apt-rdepends (1.3.0-5) ...
Processing triggers for man-db (2.7.5-1) ...
Setting up apt-rdepends (1.3.0-5) ...

user@hostname:~$ apt-rdepends -b libreoffice
Reading package lists... Done
Building dependency tree       
Reading state information... Done
You must put some 'source' URIs in your sources.list
libreoffice
user@hostname:~$ apt-rdepends -p libreoffice
Reading package lists... Done
Building dependency tree       
Reading state information... Done
libreoffice
  Depends: fonts-dejavu [Installed]
  Depends: fonts-sil-gentium-basic [NotInstalled]
  Depends: libreoffice-avmedia-backend-gstreamer [Installed]
  Depends: libreoffice-base [NotInstalled]
  Depends: libreoffice-calc [Installed]
  Depends: libreoffice-core (= 1:5.1.2-0ubuntu1) [Installed]
  Depends: libreoffice-draw [Installed]
  Depends: libreoffice-impress [Installed]
  Depends: libreoffice-java-common (>= 1:5.1.2~) [NotInstalled]
  Depends: libreoffice-math [Installed]
  Depends: libreoffice-report-builder-bin [NotInstalled]
  Depends: libreoffice-writer [Installed]
  Depends: python3-uno (>= 4.4.0~beta2) [Installed]
fonts-dejavu
  Depends: fonts-dejavu-core [Installed]
  Depends: fonts-dejavu-extra [Installed]
fonts-dejavu-core
fonts-dejavu-extra
  Depends: fonts-dejavu-core [Installed]
fonts-sil-gentium-basic
libreoffice-avmedia-backend-gstreamer
  Depends: libc6 (>= 2.4) [Installed]
  Depends: libgcc1 (>= 1:3.0) [Installed]
  Depends: libglib2.0-0 (>= 2.16.0) [Installed]
  Depends: libgstreamer-plugins-base1.0-0 (>= 1.0.0) [Installed]
  Depends: libgstreamer1.0-0 (>= 1.0.0) [Installed]
  Depends: libgtk-3-0 (>= 3.0.0) [Installed]
  Depends: libreoffice-core (= 1:5.1.2-0ubuntu1) [Installed]
  Depends: libstdc++6 (>= 4.1.1) [Installed]
  Depends: uno-libs3 (>= 4.4.0~alpha) [Installed]
  Depends: ure [Installed]
libc6
  Depends: libgcc1 [Installed]
libgcc1
  Depends: gcc-6-base (= 6.0.1-0ubuntu1) [Installed]
  Depends: libc6 (>= 2.14) [Installed]
gcc-6-base
libglib2.0-0
  Depends: libc6 (>= 2.17) [Installed]
  Depends: libffi6 (>= 3.0.4) [Installed]
  Depends: libpcre3 [Installed]
  Depends: libselinux1 (>= 1.32) [Installed]
  Depends: zlib1g (>= 1:1.2.2) [Installed]
libffi6
  Depends: libc6 (>= 2.14) [Installed]
libpcre3
  Depends: libc6 (>= 2.14) [Installed]
  PreDepends: multiarch-support [Installed]
multiarch-support
  Depends: libc6 (>= 2.3.6-2) [Installed]
libselinux1
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libpcre3 [Installed]
zlib1g
  Depends: libc6 (>= 2.14) [Installed]
libgstreamer-plugins-base1.0-0
  Depends: iso-codes [Installed]
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libglib2.0-0 (>= 2.40) [Installed]
  Depends: libgstreamer1.0-0 (>= 1.6.0) [Installed]
  Depends: liborc-0.4-0 (>= 1:0.4.25) [Installed]
  Depends: zlib1g (>= 1:1.1.4) [Installed]
iso-codes
libgstreamer1.0-0
  Depends: libc6 (>= 2.15) [Installed]
  Depends: libcap2 (>= 1:2.10) [Installed]
  Depends: libcap2-bin [Installed]
  Depends: libglib2.0-0 (>= 2.41.1) [Installed]
libcap2
  Depends: libc6 (>= 2.14) [Installed]
libcap2-bin
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libcap2 (>= 1:2.10) [Installed]
liborc-0.4-0
  Depends: libc6 (>= 2.14) [Installed]
libgtk-3-0
  Depends: libatk-bridge2.0-0 (>= 2.5.3) [Installed]
  Depends: libatk1.0-0 (>= 2.15.1) [Installed]
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libcairo-gobject2 (>= 1.10.0) [Installed]
  Depends: libcairo2 (>= 1.14.0) [Installed]
  Depends: libcolord2 (>= 0.1.10) [Installed]
  Depends: libcups2 (>= 1.6.2) [Installed]
  Depends: libepoxy0 (>= 1.0) [Installed]
  Depends: libfontconfig1 (>= 2.11.1) [Installed]
  Depends: libgdk-pixbuf2.0-0 (>= 2.30.1) [Installed]
  Depends: libglib2.0-0 (>= 2.45.8) [Installed]
  Depends: libgtk-3-common (>= 3.18.9-1ubuntu3) [Installed]
  Depends: libjson-glib-1.0-0 (>= 0.12.0) [Installed]
  Depends: libmirclient9 (>= 0.20.2+16.04.20160307) [Installed]
  Depends: libpango-1.0-0 (>= 1.37.5) [Installed]
  Depends: libpangocairo-1.0-0 (>= 1.37.3) [Installed]
  Depends: libpangoft2-1.0-0 (>= 1.37.3) [Installed]
  Depends: librest-0.7-0 (>= 0.7) [Installed]
  Depends: libwayland-client0 (>= 1.5.91) [Installed]
  Depends: libwayland-cursor0 (>= 1.5.91) [Installed]
  Depends: libwayland-egl1 [NotInstalled]
  Depends: libwayland-egl1-mesa (>= 10.0.2) [Installed]
  Depends: libx11-6 (>= 2:1.4.99.1) [Installed]
  Depends: libxcomposite1 (>= 1:0.3-1) [Installed]
  Depends: libxcursor1 (>> 1.1.2) [Installed]
  Depends: libxdamage1 (>= 1:1.1) [Installed]
  Depends: libxext6 [Installed]
  Depends: libxfixes3 [Installed]
  Depends: libxi6 (>= 2:1.2.99.4) [Installed]
  Depends: libxinerama1 [Installed]
  Depends: libxkbcommon0 (>= 0.5.0) [Installed]
  Depends: libxrandr2 (>= 2:1.5.0) [Installed]
  Depends: shared-mime-info [Installed]
libatk-bridge2.0-0
  Depends: libatk1.0-0 (>= 2.15.4) [Installed]
  Depends: libatspi2.0-0 (>= 2.9.90) [Installed]
  Depends: libc6 (>= 2.4) [Installed]
  Depends: libdbus-1-3 (>= 1.9.14) [Installed]
  Depends: libglib2.0-0 (>= 2.41.1) [Installed]
libatk1.0-0
  Depends: libatk1.0-data (= 2.18.0-1) [Installed]
  Depends: libc6 (>= 2.4) [Installed]
  Depends: libglib2.0-0 (>= 2.41.1) [Installed]
libatk1.0-data
libatspi2.0-0
  Depends: libc6 (>= 2.7) [Installed]
  Depends: libdbus-1-3 (>= 1.9.14) [Installed]
  Depends: libglib2.0-0 (>= 2.37.3) [Installed]
  Depends: libx11-6 [Installed]
libdbus-1-3
  Depends: libc6 (>= 2.17) [Installed]
  Depends: libsystemd0 [Installed]
libsystemd0
  PreDepends: libc6 (>= 2.17) [Installed]
  PreDepends: libgcrypt20 (>= 1.6.1) [Installed]
  PreDepends: liblzma5 (>= 5.1.1alpha+20120614) [Installed]
  PreDepends: libselinux1 (>= 1.32) [Installed]
libgcrypt20
  Depends: libc6 (>= 2.15) [Installed]
  Depends: libgpg-error0 (>= 1.14) [Installed]
libgpg-error0
  Depends: libc6 (>= 2.15) [Installed]
liblzma5
  Depends: libc6 (>= 2.14) [Installed]
  PreDepends: multiarch-support [Installed]
libx11-6
  Depends: libc6 (>= 2.15) [Installed]
  Depends: libx11-data [Installed]
  Depends: libxcb1 (>= 1.2) [Installed]
libx11-data
libxcb1
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libxau6 [Installed]
  Depends: libxdmcp6 [Installed]
libxau6
  Depends: libc6 (>= 2.4) [Installed]
  PreDepends: multiarch-support [Installed]
libxdmcp6
  Depends: libc6 (>= 2.4) [Installed]
libcairo-gobject2
  Depends: libc6 (>= 2.2.5) [Installed]
  Depends: libcairo2 (>= 1.10.0) [Installed]
  Depends: libglib2.0-0 (>= 2.14.0) [Installed]
libcairo2
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libfontconfig1 (>= 2.9.0) [Installed]
  Depends: libfreetype6 (>= 2.3.5) [Installed]
  Depends: libpixman-1-0 (>= 0.30.0) [Installed]
  Depends: libpng12-0 (>= 1.2.13-4) [Installed]
  Depends: libx11-6 [Installed]
  Depends: libxcb-render0 [Installed]
  Depends: libxcb-shm0 [Installed]
  Depends: libxcb1 (>= 1.6) [Installed]
  Depends: libxext6 [Installed]
  Depends: libxrender1 [Installed]
  Depends: zlib1g (>= 1:1.1.4) [Installed]
libfontconfig1
  Depends: fontconfig-config (= 2.11.94-0ubuntu1) [Installed]
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libexpat1 (>= 2.0.1) [Installed]
  Depends: libfreetype6 (>= 2.2.1) [Installed]
fontconfig-config
  Depends: fonts-dejavu-core [Installed]
  Depends: fonts-freefont-ttf [Installed]
  Depends: gsfonts-x11 [NotInstalled]
  Depends: ttf-bitstream-vera [NotInstalled]
  Depends: ucf (>= 0.29) [Installed]
fonts-freefont-ttf
gsfonts-x11
  Depends: gsfonts (>= 6.0-2) [Installed]
  Depends: xfonts-utils (>= 1:7.5+2) [Installed]
gsfonts
xfonts-utils
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libfontenc1 [Installed]
  Depends: libfreetype6 (>= 2.2.1) [Installed]
  Depends: libxfont1 (>= 1:1.4.2) [Installed]
  Depends: x11-common [Installed]
  Depends: xfonts-encodings [Installed]
  Depends: zlib1g (>= 1:1.1.4) [Installed]
libfontenc1
  Depends: libc6 (>= 2.14) [Installed]
  Depends: zlib1g (>= 1:1.1.4) [Installed]
libfreetype6
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libpng12-0 (>= 1.2.13-4) [Installed]
  Depends: zlib1g (>= 1:1.1.4) [Installed]
libpng12-0
  Depends: libc6 (>= 2.14) [Installed]
  Depends: zlib1g (>= 1:1.1.4) [Installed]
libxfont1
  Depends: libbz2-1.0 [Installed]
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libfontenc1 [Installed]
  Depends: libfreetype6 (>= 2.2.1) [Installed]
  Depends: zlib1g (>= 1:1.1.4) [Installed]
  PreDepends: multiarch-support [Installed]
libbz2-1.0
  Depends: libc6 (>= 2.4) [Installed]
x11-common
  Depends: lsb-base (>= 1.3-9ubuntu2) [Installed]
lsb-base
xfonts-encodings
  Depends: x11-common [Installed]
ttf-bitstream-vera
ucf
  Depends: coreutils (>= 5.91) [Installed]
  Depends: debconf (>= 1.5.19) [Installed]
coreutils
  PreDepends: libacl1 (>= 2.2.51-8) [Installed]
  PreDepends: libattr1 (>= 1:2.4.46-8) [Installed]
  PreDepends: libc6 (>= 2.17) [Installed]
  PreDepends: libselinux1 (>= 2.1.13) [Installed]
libacl1
  Depends: libattr1 (>= 1:2.4.46-8) [Installed]
  Depends: libc6 (>= 2.14) [Installed]
libattr1
  Depends: libc6 (>= 2.4) [Installed]
  PreDepends: multiarch-support [Installed]
debconf
  PreDepends: perl-base (>= 5.6.1-4) [Installed]
perl-base
  PreDepends: dpkg (>= 1.17.17) [Installed]
  PreDepends: libc6 (>= 2.14) [Installed]
dpkg
  PreDepends: libbz2-1.0 [Installed]
  PreDepends: libc6 (>= 2.14) [Installed]
  PreDepends: liblzma5 (>= 5.1.1alpha+20120614) [Installed]
  PreDepends: libselinux1 (>= 2.3) [Installed]
  PreDepends: tar (>= 1.23) [Installed]
  PreDepends: zlib1g (>= 1:1.1.4) [Installed]
tar
  PreDepends: libacl1 (>= 2.2.51-8) [Installed]
  PreDepends: libc6 (>= 2.17) [Installed]
  PreDepends: libselinux1 (>= 1.32) [Installed]
libexpat1
  Depends: libc6 (>= 2.14) [Installed]
libpixman-1-0
  Depends: libc6 (>= 2.14) [Installed]
libxcb-render0
  Depends: libc6 (>= 2.4) [Installed]
  Depends: libxcb1 (>= 1.8) [Installed]
libxcb-shm0
  Depends: libc6 (>= 2.4) [Installed]
  Depends: libxcb1 (>= 1.9.2) [Installed]
libxext6
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libx11-6 (>= 2:1.6.0) [Installed]
  PreDepends: multiarch-support [Installed]
libxrender1
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libx11-6 (>= 2:1.6.0) [Installed]
libcolord2
  Depends: libc6 (>= 2.4) [Installed]
  Depends: libglib2.0-0 (>= 2.37.3) [Installed]
  Depends: liblcms2-2 (>= 2.6) [Installed]
  Depends: libudev1 (>= 196) [Installed]
liblcms2-2
  Depends: libc6 (>= 2.14) [Installed]
  PreDepends: multiarch-support [Installed]
libudev1
  Depends: libc6 (>= 2.16) [Installed]
libcups2
  Depends: libavahi-client3 (>= 0.6.16) [Installed]
  Depends: libavahi-common3 (>= 0.6.16) [Installed]
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libgnutls30 (>= 3.4.2) [Installed]
  Depends: libgssapi-krb5-2 (>= 1.10+dfsg~) [Installed]
  Depends: zlib1g (>= 1:1.2.0) [Installed]
libavahi-client3
  Depends: libavahi-common3 (>= 0.6.22) [Installed]
  Depends: libc6 (>= 2.4) [Installed]
  Depends: libdbus-1-3 (>= 1.9.14) [Installed]
libavahi-common3
  Depends: libavahi-common-data [Installed]
  Depends: libc6 (>= 2.14) [Installed]
libavahi-common-data
libgnutls30
  Depends: libc6 (>= 2.17) [Installed]
  Depends: libgmp10 (>= 2:6) [Installed]
  Depends: libhogweed4 [Installed]
  Depends: libidn11 (>= 1.13) [Installed]
  Depends: libnettle6 [Installed]
  Depends: libp11-kit0 (>= 0.23.1) [Installed]
  Depends: libtasn1-6 (>= 4.5) [Installed]
  Depends: zlib1g (>= 1:1.1.4) [Installed]
libgmp10
  Depends: libc6 (>= 2.14) [Installed]
libhogweed4
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libgmp10 (>= 2:6.0.0) [Installed]
  Depends: libnettle6 (= 3.2-1) [Installed]
libnettle6
  Depends: libc6 (>= 2.14) [Installed]
libidn11
  Depends: libc6 (>= 2.14) [Installed]
libp11-kit0
  Depends: libc6 (>= 2.16) [Installed]
  Depends: libffi6 (>= 3.0.4) [Installed]
libtasn1-6
  Depends: libc6 (>= 2.14) [Installed]
libgssapi-krb5-2
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libcomerr2 (>= 1.34) [Installed]
  Depends: libk5crypto3 (>= 1.8+dfsg) [Installed]
  Depends: libkrb5-3 (= 1.13.2+dfsg-5) [Installed]
  Depends: libkrb5support0 (>= 1.13~alpha1+dfsg) [Installed]
libcomerr2
  Depends: libc6 (>= 2.17) [Installed]
libk5crypto3
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libkrb5support0 (>= 1.13~alpha1+dfsg) [Installed]
libkrb5support0
  Depends: libc6 (>= 2.14) [Installed]
libkrb5-3
  Depends: libc6 (>= 2.16) [Installed]
  Depends: libcomerr2 (>= 1.34) [Installed]
  Depends: libk5crypto3 (>= 1.9+dfsg~beta1) [Installed]
  Depends: libkeyutils1 (>= 1.5.9) [Installed]
  Depends: libkrb5support0 (= 1.13.2+dfsg-5) [Installed]
libkeyutils1
  Depends: libc6 (>= 2.14) [Installed]
libepoxy0
  Depends: libc6 (>= 2.7) [Installed]
libgdk-pixbuf2.0-0
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libgdk-pixbuf2.0-common (= 2.32.2-1ubuntu1) [Installed]
  Depends: libglib2.0-0 (>= 2.37.6) [Installed]
  Depends: libjpeg8 (>= 8c) [Installed]
  Depends: libpng12-0 (>= 1.2.13-4) [Installed]
  Depends: libtiff5 (>= 4.0.3) [Installed]
  Depends: libx11-6 [Installed]
libgdk-pixbuf2.0-common
libjpeg8
  Depends: libjpeg-turbo8 (>= 1.1.90+svn722-1ubuntu6) [Installed]
libjpeg-turbo8
  Depends: libc6 (>= 2.14) [Installed]
  PreDepends: multiarch-support [Installed]
libtiff5
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libjbig0 (>= 2.0) [Installed]
  Depends: libjpeg8 (>= 8c) [Installed]
  Depends: liblzma5 (>= 5.1.1alpha+20120614) [Installed]
  Depends: zlib1g (>= 1:1.1.4) [Installed]
libjbig0
  Depends: libc6 (>= 2.4) [Installed]
  PreDepends: multiarch-support [Installed]
libgtk-3-common
  Depends: adwaita-icon-theme (>= 3.18) [Installed]
  Depends: dconf-gsettings-backend [Installed]
  Depends: gsettings-backend [NotInstalled]
adwaita-icon-theme
  Depends: adwaita-icon-theme-full [NotInstalled]
  Depends: hicolor-icon-theme [Installed]
  Depends: libgtk-3-bin [Installed]
  Depends: librsvg2-common [Installed]
  Depends: ubuntu-mono [Installed]
adwaita-icon-theme-full
  Depends: adwaita-icon-theme (= 3.18.0-2ubuntu3) [Installed]
hicolor-icon-theme
libgtk-3-bin
  Depends: libc6 (>= 2.4) [Installed]
  Depends: libcairo2 (>= 1.14.0) [Installed]
  Depends: libglib2.0-0 (>= 2.45.8) [Installed]
  Depends: libgtk-3-0 (>= 3.18.9-1ubuntu3) [Installed]
  Depends: libgtk-3-common (>= 3.18.9-1ubuntu3) [Installed]
librsvg2-common
  Depends: libc6 (>= 2.2.5) [Installed]
  Depends: libgdk-pixbuf2.0-0 (>= 2.22.0) [Installed]
  Depends: libglib2.0-0 (>= 2.24.0) [Installed]
  Depends: librsvg2-2 (= 2.40.13-3) [Installed]
librsvg2-2
  Depends: libc6 (>= 2.4) [Installed]
  Depends: libcairo2 (>= 1.10.0) [Installed]
  Depends: libcroco3 (>= 0.6.2) [Installed]
  Depends: libgdk-pixbuf2.0-0 (>= 2.22.0) [Installed]
  Depends: libglib2.0-0 (>= 2.37.3) [Installed]
  Depends: libpango-1.0-0 (>= 1.36.0) [Installed]
  Depends: libpangocairo-1.0-0 (>= 1.36.0) [Installed]
  Depends: libxml2 (>= 2.8.0) [Installed]
libcroco3
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libglib2.0-0 (>= 2.16.0) [Installed]
  Depends: libxml2 (>= 2.7.4) [Installed]
libxml2
  Depends: libc6 (>= 2.15) [Installed]
  Depends: libicu55 (>= 55.1-1~) [Installed]
  Depends: liblzma5 (>= 5.1.1alpha+20120614) [Installed]
  Depends: zlib1g (>= 1:1.2.3.3) [Installed]
libicu55
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libgcc1 (>= 1:3.0) [Installed]
  Depends: libstdc++6 (>= 5.2) [Installed]
libstdc++6
  Depends: gcc-5-base (= 5.3.1-14ubuntu2) [Installed]
  Depends: libc6 (>= 2.18) [Installed]
  Depends: libgcc1 (>= 1:4.2) [Installed]
gcc-5-base
libpango-1.0-0
  Depends: fontconfig (>= 2.1.91) [Installed]
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libglib2.0-0 (>= 2.37.3) [Installed]
  Depends: libthai0 (>= 0.1.12) [Installed]
fontconfig
  Depends: fontconfig-config [Installed]
  Depends: libc6 (>= 2.4) [Installed]
  Depends: libfontconfig1 (>= 2.11.94) [Installed]
  Depends: libfreetype6 (>= 2.2.1) [Installed]
  PreDepends: dpkg (>= 1.16.1) [Installed]
libthai0
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libdatrie1 (>= 0.2.0) [Installed]
  Depends: libthai-data (>= 0.1.10) [Installed]
libdatrie1
  Depends: libc6 (>= 2.14) [Installed]
libthai-data
libpangocairo-1.0-0
  Depends: libc6 (>= 2.4) [Installed]
  Depends: libcairo2 (>= 1.12.10) [Installed]
  Depends: libfontconfig1 (>= 2.9.0) [Installed]
  Depends: libfreetype6 (>= 2.2.1) [Installed]
  Depends: libglib2.0-0 (>= 2.37.3) [Installed]
  Depends: libpango-1.0-0 (>= 1.37.5) [Installed]
  Depends: libpangoft2-1.0-0 (>= 1.28.1) [Installed]
libpangoft2-1.0-0
  Depends: libc6 (>= 2.4) [Installed]
  Depends: libfontconfig1 (>= 2.9.0) [Installed]
  Depends: libfreetype6 (>= 2.2.1) [Installed]
  Depends: libglib2.0-0 (>= 2.37.3) [Installed]
  Depends: libharfbuzz0b (>= 0.9.30) [Installed]
  Depends: libpango-1.0-0 (>= 1.37.2) [Installed]
libharfbuzz0b
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libfreetype6 (>= 2.4.2) [Installed]
  Depends: libglib2.0-0 (>= 2.31.8) [Installed]
  Depends: libgraphite2-3 (>= 1.2.2) [Installed]
libgraphite2-3
  Depends: libc6 (>= 2.14) [Installed]
ubuntu-mono
  Depends: adwaita-icon-theme [Installed]
  Depends: hicolor-icon-theme [Installed]
  Depends: humanity-icon-theme [Installed]
humanity-icon-theme
  Depends: adwaita-icon-theme [Installed]
  Depends: hicolor-icon-theme [Installed]
dconf-gsettings-backend
  Depends: dconf-service (<< 0.24.0-2.1~) [Installed]
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libdconf1 (= 0.24.0-2) [Installed]
  Depends: libglib2.0-0 (>= 2.39.1) [Installed]
dconf-service
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libdconf1 (= 0.24.0-2) [Installed]
  Depends: libglib2.0-0 (>= 2.39.1) [Installed]
libdconf1
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libglib2.0-0 (>= 2.39.1) [Installed]
gsettings-backend
libjson-glib-1.0-0
  Depends: libc6 (>= 2.4) [Installed]
  Depends: libglib2.0-0 (>= 2.41.1) [Installed]
  Depends: libjson-glib-1.0-common (>= 1.1.2-0ubuntu1) [Installed]
libjson-glib-1.0-common
libmirclient9
  Depends: libboost-system1.58.0 [Installed]
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libgcc1 (>= 1:3.3.1) [Installed]
  Depends: libmircommon5 (>= 0.21.0+16.04.20160330) [Installed]
  Depends: libmirprotobuf3 (>= 0.21.0+16.04.20160330) [Installed]
  Depends: libprotobuf-lite9v5 [Installed]
  Depends: libstdc++6 (>= 5.2) [Installed]
  Depends: libxkbcommon0 (>= 0.5.0) [Installed]
libboost-system1.58.0
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libstdc++6 (>= 5.2) [Installed]
libmircommon5
  Depends: libboost-filesystem1.58.0 [Installed]
  Depends: libboost-system1.58.0 [Installed]
  Depends: libc6 (>= 2.17) [Installed]
  Depends: libgcc1 (>= 1:3.4) [Installed]
  Depends: libstdc++6 (>= 5.2) [Installed]
libboost-filesystem1.58.0
  Depends: libboost-system1.58.0 [Installed]
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libgcc1 (>= 1:3.0) [Installed]
  Depends: libstdc++6 (>= 5.2) [Installed]
libmirprotobuf3
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libgcc1 (>= 1:3.3.1) [Installed]
  Depends: libprotobuf-lite9v5 [Installed]
  Depends: libstdc++6 (>= 5.2) [Installed]
libprotobuf-lite9v5
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libgcc1 (>= 1:4.1.1) [Installed]
  Depends: libstdc++6 (>= 5.2) [Installed]
libxkbcommon0
  Depends: libc6 (>= 2.17) [Installed]
  Depends: xkb-data [Installed]
xkb-data
librest-0.7-0
  Depends: libc6 (>= 2.4) [Installed]
  Depends: libglib2.0-0 (>= 2.37.3) [Installed]
  Depends: libsoup-gnome2.4-1 (>= 2.27.4) [Installed]
  Depends: libsoup2.4-1 (>= 2.30) [Installed]
  Depends: libxml2 (>= 2.7.4) [Installed]
  PreDepends: multiarch-support [Installed]
libsoup-gnome2.4-1
  Depends: libc6 (>= 2.4) [Installed]
  Depends: libglib2.0-0 (>= 2.39.90) [Installed]
  Depends: libsoup2.4-1 (>= 2.41.90) [Installed]
libsoup2.4-1
  Depends: glib-networking (>= 2.32.0) [Installed]
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libglib2.0-0 (>= 2.39.90) [Installed]
  Depends: libsqlite3-0 (>= 3.5.9) [Installed]
  Depends: libxml2 (>= 2.7.4) [Installed]
glib-networking
  Depends: glib-networking-common (= 2.48.0-1) [Installed]
  Depends: glib-networking-services (<< 2.48.0-1.1~) [Installed]
  Depends: gsettings-desktop-schemas [Installed]
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libglib2.0-0 (>= 2.46.0) [Installed]
  Depends: libgnutls30 (>= 3.4.2) [Installed]
  Depends: libp11-kit0 (>= 0.11) [Installed]
  Depends: libproxy1v5 (>= 0.4.11) [Installed]
glib-networking-common
glib-networking-services
  Depends: glib-networking-common (= 2.48.0-1) [Installed]
  Depends: libc6 (>= 2.4) [Installed]
  Depends: libglib2.0-0 (>= 2.46.0) [Installed]
  Depends: libproxy1v5 (>= 0.4.11) [Installed]
libproxy1v5
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libgcc1 (>= 1:3.0) [Installed]
  Depends: libstdc++6 (>= 5.2) [Installed]
gsettings-desktop-schemas
  Depends: dconf-gsettings-backend [Installed]
  Depends: gsettings-backend [NotInstalled]
libsqlite3-0
  Depends: libc6 (>= 2.14) [Installed]
libwayland-client0
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libffi6 (>= 3.0.4) [Installed]
libwayland-cursor0
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libwayland-client0 (>= 1.3.92) [Installed]
libwayland-egl1
libwayland-egl1-mesa
  Depends: libc6 (>= 2.2.5) [Installed]
  Depends: libegl1-mesa (= 11.2.0-1ubuntu2) [Installed]
libegl1-mesa
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libdrm2 (>= 2.4.60) [Installed]
  Depends: libexpat1 (>= 2.0.1) [Installed]
  Depends: libgbm1 (>= 8.1~0) [Installed]
  Depends: libgl1-mesa-dri (= 11.2.0-1ubuntu2) [Installed]
  Depends: libudev1 [Installed]
  Depends: libwayland-client0 (>= 1.3.92) [Installed]
  Depends: libwayland-server0 (>= 1.2.0) [Installed]
  Depends: libx11-xcb1 [Installed]
  Depends: libxcb-dri2-0 (>= 1.8) [Installed]
  Depends: libxcb-dri3-0 [Installed]
  Depends: libxcb-present0 [Installed]
  Depends: libxcb-sync1 [Installed]
  Depends: libxcb-xfixes0 [Installed]
  Depends: libxcb1 (>= 1.9.2) [Installed]
  Depends: libxshmfence1 [Installed]
libdrm2
  Depends: libc6 (>= 2.17) [Installed]
libgbm1
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libdrm2 (>= 2.4.3) [Installed]
  Depends: libexpat1 (>= 2.0.1) [Installed]
  Depends: libudev1 [Installed]
  Depends: libwayland-client0 (>= 1.2.0) [Installed]
  Depends: libwayland-server0 (>= 1.2.0) [Installed]
libwayland-server0
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libffi6 (>= 3.0.4) [Installed]
libgl1-mesa-dri
  Depends: libc6 (>= 2.17) [Installed]
  Depends: libdrm-amdgpu1 (>= 2.4.63) [Installed]
  Depends: libdrm-intel1 (>= 2.4.48) [Installed]
  Depends: libdrm-nouveau2 (>= 2.4.66) [Installed]
  Depends: libdrm-radeon1 (>= 2.4.31) [Installed]
  Depends: libdrm2 (>= 2.4.38) [Installed]
  Depends: libelf1 (>= 0.142) [Installed]
  Depends: libexpat1 (>= 2.0.1) [Installed]
  Depends: libgcc1 (>= 1:3.4) [Installed]
  Depends: libllvm3.8 [Installed]
  Depends: libstdc++6 (>= 5.2) [Installed]
libdrm-amdgpu1
  Depends: libc6 (>= 2.17) [Installed]
  Depends: libdrm2 (>= 2.4.60) [Installed]
libdrm-intel1
  Depends: libc6 (>= 2.17) [Installed]
  Depends: libdrm2 (>= 2.4.38) [Installed]
  Depends: libpciaccess0 [Installed]
libpciaccess0
  Depends: libc6 (>= 2.7) [Installed]
  Depends: zlib1g (>= 1:1.1.4) [Installed]
libdrm-nouveau2
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libdrm2 (>= 2.4.38) [Installed]
libdrm-radeon1
  Depends: libc6 (>= 2.4) [Installed]
  Depends: libdrm2 (>= 2.4.38) [Installed]
libelf1
  Depends: libc6 (>= 2.14) [Installed]
  Depends: zlib1g (>= 1:1.1.4) [Installed]
libllvm3.8
  Depends: libc6 (>= 2.15) [Installed]
  Depends: libedit2 (>= 2.11-20080614) [Installed]
  Depends: libffi6 (>= 3.0.4) [Installed]
  Depends: libgcc1 (>= 1:3.4) [Installed]
  Depends: libstdc++6 (>= 5.2) [Installed]
  Depends: libtinfo5 (>= 6) [Installed]
  Depends: zlib1g (>= 1:1.2.0) [Installed]
libedit2
  Depends: libbsd0 (>= 0.0) [Installed]
  Depends: libc6 (>= 2.17) [Installed]
  Depends: libtinfo5 (>= 6) [Installed]
libbsd0
  Depends: libc6 (>= 2.17) [Installed]
libtinfo5
  Depends: libc6 (>= 2.16) [Installed]
libx11-xcb1
  Depends: libc6 (>= 2.2.5) [Installed]
libxcb-dri2-0
  Depends: libc6 (>= 2.4) [Installed]
  Depends: libxcb1 [Installed]
libxcb-dri3-0
  Depends: libc6 (>= 2.4) [Installed]
  Depends: libxcb1 (>= 1.9.2) [Installed]
libxcb-present0
  Depends: libc6 (>= 2.4) [Installed]
  Depends: libxcb1 [Installed]
libxcb-sync1
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libxcb1 [Installed]
libxcb-xfixes0
  Depends: libc6 (>= 2.4) [Installed]
  Depends: libxcb1 [Installed]
libxshmfence1
  Depends: libc6 (>= 2.4) [Installed]
  PreDepends: multiarch-support [Installed]
libxcomposite1
  Depends: libc6 (>= 2.2.5) [Installed]
  Depends: libx11-6 (>= 2:1.4.99.1) [Installed]
  PreDepends: multiarch-support [Installed]
libxcursor1
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libx11-6 (>= 2:1.4.99.1) [Installed]
  Depends: libxfixes3 [Installed]
  Depends: libxrender1 [Installed]
  PreDepends: multiarch-support [Installed]
libxfixes3
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libx11-6 (>= 2:1.6.0) [Installed]
  PreDepends: multiarch-support [Installed]
libxdamage1
  Depends: libc6 (>= 2.2.5) [Installed]
  Depends: libx11-6 (>= 2:1.4.99.1) [Installed]
  PreDepends: multiarch-support [Installed]
libxi6
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libx11-6 (>= 2:1.6.0) [Installed]
  Depends: libxext6 [Installed]
libxinerama1
  Depends: libc6 (>= 2.2.5) [Installed]
  Depends: libx11-6 (>= 2:1.4.99.1) [Installed]
  Depends: libxext6 [Installed]
  PreDepends: multiarch-support [Installed]
libxrandr2
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libx11-6 (>= 2:1.6.0) [Installed]
  Depends: libxext6 [Installed]
  Depends: libxrender1 [Installed]
shared-mime-info
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libglib2.0-0 (>= 2.35.9) [Installed]
  Depends: libxml2 (>= 2.7.4) [Installed]
libreoffice-core
  Depends: fontconfig [Installed]
  Depends: fonts-opensymbol [Installed]
  Depends: libc6 (>= 2.16) [Installed]
  Depends: libcairo2 (>= 1.10.0) [Installed]
  Depends: libclucene-contribs1v5 (>= 2.3.3.4) [Installed]
  Depends: libclucene-core1v5 (>= 2.3.3.4) [Installed]
  Depends: libcmis-0.5-5v5 [Installed]
  Depends: libcups2 (>= 1.4.0) [Installed]
  Depends: libcurl3-gnutls (>= 7.16.2) [Installed]
  Depends: libdbus-glib-1-2 (>= 0.78) [Installed]
  Depends: libeot0 [Installed]
  Depends: libexpat1 (>= 2.0.1) [Installed]
  Depends: libexttextcat-2.0-0 (>= 2.2-8) [Installed]
  Depends: libfontconfig1 (>= 2.11.94) [Installed]
  Depends: libfreetype6 (>= 2.3.5) [Installed]
  Depends: libgcc1 (>= 1:3.0) [Installed]
  Depends: libgl1 [NotInstalled]
  Depends: libgl1-mesa-glx [Installed]
  Depends: libglew1.13 (>= 1.12.0) [Installed]
  Depends: libglib2.0-0 (>= 2.15.0) [Installed]
  Depends: libgraphite2-3 (>= 1.2.2) [Installed]
  Depends: libharfbuzz-icu0 (>= 0.9.18) [Installed]
  Depends: libharfbuzz0b (>= 0.9.18) [Installed]
  Depends: libhunspell-1.3-0 (>= 1.3.3) [Installed]
  Depends: libhyphen0 (>= 2.7.1) [Installed]
  Depends: libice6 (>= 1:1.0.0) [Installed]
  Depends: libicu55 (>= 55.1-1~) [Installed]
  Depends: libjpeg8 (>= 8c) [Installed]
  Depends: liblangtag1 (>= 0.4.0) [Installed]
  Depends: liblcms2-2 (>= 2.2+git20110628) [Installed]
  Depends: libldap-2.4-2 (>= 2.4.7) [Installed]
  Depends: libmythes-1.2-0 [Installed]
  Depends: libneon27-gnutls [Installed]
  Depends: libnspr4 (>= 2:4.9-2~) [Installed]
  Depends: libnspr4-0d (>= 1.8.0.10) [NotInstalled]
  Depends: libnss3 (>= 2:3.13.4-2~) [Installed]
  Depends: libnss3-1d (>= 3.12.0~1.9b1) [NotInstalled]
  Depends: libpng12-0 (>= 1.2.13-4) [Installed]
  Depends: librdf0 (>= 1.0.17) [Installed]
  Depends: libreoffice-common (>> 1:5.1.2) [Installed]
  Depends: librevenge-0.0-0 [Installed]
  Depends: libsm6 [Installed]
  Depends: libstdc++6 (>= 5.2) [Installed]
  Depends: libx11-6 [Installed]
  Depends: libxext6 [Installed]
  Depends: libxinerama1 [Installed]
  Depends: libxml2 (>= 2.7.4) [Installed]
  Depends: libxrandr2 [Installed]
  Depends: libxrender1 [Installed]
  Depends: libxslt1.1 (>= 1.1.25) [Installed]
  Depends: lp-solve (>= 5.5.0.13-5+b1) [Installed]
  Depends: uno-libs3 (>= 5.1.0~alpha) [Installed]
  Depends: ure (>= 4.2~) [Installed]
  Depends: zlib1g (>= 1:1.1.4) [Installed]
fonts-opensymbol
libclucene-contribs1v5
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libclucene-core1v5 (>= 2.3.3.4) [Installed]
  Depends: libgcc1 (>= 1:4.1.1) [Installed]
  Depends: libstdc++6 (>= 5.2) [Installed]
  Depends: zlib1g (>= 1:1.1.4) [Installed]
libclucene-core1v5
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libgcc1 (>= 1:4.1.1) [Installed]
  Depends: libstdc++6 (>= 5.2) [Installed]
  Depends: zlib1g (>= 1:1.1.4) [Installed]
libcmis-0.5-5v5
  Depends: libboost-date-time1.58.0 [Installed]
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libcurl3-gnutls (>= 7.16.2) [Installed]
  Depends: libgcc1 (>= 1:3.0) [Installed]
  Depends: libstdc++6 (>= 5.2) [Installed]
  Depends: libxml2 (>= 2.7.4) [Installed]
libboost-date-time1.58.0
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libgcc1 (>= 1:3.0) [Installed]
  Depends: libstdc++6 (>= 5.2) [Installed]
libcurl3-gnutls
  Depends: libc6 (>= 2.17) [Installed]
  Depends: libgnutls30 (>= 3.4.2) [Installed]
  Depends: libgssapi-krb5-2 (>= 1.10+dfsg~) [Installed]
  Depends: libidn11 (>= 1.13) [Installed]
  Depends: libldap-2.4-2 (>= 2.4.7) [Installed]
  Depends: libnettle6 [Installed]
  Depends: librtmp1 (>= 2.4+20131018.git79459a2-3~) [Installed]
  Depends: zlib1g (>= 1:1.1.4) [Installed]
libldap-2.4-2
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libgnutls30 (>= 3.4.2) [Installed]
  Depends: libgssapi3-heimdal (>= 1.4.0+git20110226) [Installed]
  Depends: libsasl2-2 [Installed]
libgssapi3-heimdal
  Depends: libasn1-8-heimdal (>= 1.4.0+git20110226) [Installed]
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libcomerr2 (>= 1.01) [Installed]
  Depends: libhcrypto4-heimdal (>= 1.4.0+git20110226) [Installed]
  Depends: libheimntlm0-heimdal (>= 1.4.0+git20110226) [Installed]
  Depends: libkrb5-26-heimdal (>= 1.6~git20131117) [Installed]
  Depends: libroken18-heimdal (>= 1.4.0+git20110226) [Installed]
libasn1-8-heimdal
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libcomerr2 (>= 1.01) [Installed]
  Depends: libroken18-heimdal (>= 1.4.0+git20110226) [Installed]
libroken18-heimdal
  Depends: libc6 (>= 2.16) [Installed]
libhcrypto4-heimdal
  Depends: libasn1-8-heimdal (>= 1.4.0+git20110226) [Installed]
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libroken18-heimdal (>= 1.4.0+git20110226) [Installed]
libheimntlm0-heimdal
  Depends: libc6 (>= 2.4) [Installed]
  Depends: libhcrypto4-heimdal (>= 1.4.0+git20110226) [Installed]
  Depends: libkrb5-26-heimdal (>= 1.4.0+git20110226) [Installed]
  Depends: libroken18-heimdal (>= 1.4.0+git20110226) [Installed]
  Depends: libwind0-heimdal (>= 1.4.0+git20110226) [Installed]
libkrb5-26-heimdal
  Depends: libasn1-8-heimdal (>= 1.6~git20131117) [Installed]
  Depends: libc6 (>= 2.15) [Installed]
  Depends: libcomerr2 (>= 1.41.11) [Installed]
  Depends: libhcrypto4-heimdal (>= 1.4.0+git20110226) [Installed]
  Depends: libheimbase1-heimdal (>= 1.6~git20131117) [Installed]
  Depends: libhx509-5-heimdal (>= 1.4.0+git20110226) [Installed]
  Depends: libroken18-heimdal (>= 1.7~git20150920) [Installed]
  Depends: libsqlite3-0 (>= 3.5.9) [Installed]
  Depends: libwind0-heimdal (>= 1.6~git20120311) [Installed]
libheimbase1-heimdal
  Depends: libc6 (>= 2.14) [Installed]
libhx509-5-heimdal
  Depends: libasn1-8-heimdal (>= 1.4.0+git20110226) [Installed]
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libcomerr2 (>= 1.34) [Installed]
  Depends: libhcrypto4-heimdal (>= 1.4.0+git20110226) [Installed]
  Depends: libheimbase1-heimdal (>= 1.6~git20131117) [Installed]
  Depends: libroken18-heimdal (>= 1.7~git20150920) [Installed]
  Depends: libwind0-heimdal (>= 1.4.0+git20110226) [Installed]
libwind0-heimdal
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libcomerr2 (>= 1.01) [Installed]
  Depends: libroken18-heimdal (>= 1.4.0+git20110226) [Installed]
libsasl2-2
  Depends: libc6 (>= 2.15) [Installed]
  Depends: libsasl2-modules-db (>= 2.1.26.dfsg1-14build1) [Installed]
libsasl2-modules-db
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libdb5.3 [Installed]
libdb5.3
  Depends: libc6 (>= 2.17) [Installed]
librtmp1
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libgmp10 [Installed]
  Depends: libgnutls30 (>= 3.4.2) [Installed]
  Depends: libhogweed4 [Installed]
  Depends: libnettle6 [Installed]
  Depends: zlib1g (>= 1:1.1.4) [Installed]
libdbus-glib-1-2
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libdbus-1-3 (>= 1.9.14) [Installed]
  Depends: libglib2.0-0 (>= 2.31.8) [Installed]
libeot0
  Depends: libc6 (>= 2.14) [Installed]
libexttextcat-2.0-0
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libexttextcat-data (= 3.4.4-1ubuntu3) [Installed]
libexttextcat-data
libgl1
libgl1-mesa-glx
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libdrm2 (>= 2.3.1) [Installed]
  Depends: libexpat1 (>= 2.0.1) [Installed]
  Depends: libgl1-mesa-dri (>= 7.2) [Installed]
  Depends: libglapi-mesa (= 11.2.0-1ubuntu2) [Installed]
  Depends: libudev1 [Installed]
  Depends: libx11-6 (>= 2:1.4.99.1) [Installed]
  Depends: libx11-xcb1 [Installed]
  Depends: libxcb-dri2-0 (>= 1.8) [Installed]
  Depends: libxcb-dri3-0 [Installed]
  Depends: libxcb-glx0 (>= 1.8) [Installed]
  Depends: libxcb-present0 [Installed]
  Depends: libxcb-sync1 [Installed]
  Depends: libxcb1 (>= 1.9.2) [Installed]
  Depends: libxdamage1 (>= 1:1.1) [Installed]
  Depends: libxext6 [Installed]
  Depends: libxfixes3 [Installed]
  Depends: libxshmfence1 [Installed]
  Depends: libxxf86vm1 [Installed]
libglapi-mesa
  Depends: libc6 (>= 2.14) [Installed]
libxcb-glx0
  Depends: libc6 (>= 2.4) [Installed]
  Depends: libxcb1 [Installed]
libxxf86vm1
  Depends: libc6 (>= 2.4) [Installed]
  Depends: libx11-6 (>= 2:1.6.0) [Installed]
  Depends: libxext6 [Installed]
  PreDepends: multiarch-support [Installed]
libglew1.13
  Depends: libc6 (>= 2.4) [Installed]
  Depends: libgl1 [NotInstalled]
  Depends: libgl1-mesa-glx [Installed]
libharfbuzz-icu0
  Depends: libc6 (>= 2.4) [Installed]
  Depends: libharfbuzz0b (>= 0.6.0) [Installed]
  Depends: libicu55 (>= 55.1-1~) [Installed]
libhunspell-1.3-0
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libgcc1 (>= 1:3.0) [Installed]
  Depends: libstdc++6 (>= 5.2) [Installed]
libhyphen0
  Depends: libc6 (>= 2.14) [Installed]
libice6
  Depends: libc6 (>= 2.14) [Installed]
  Depends: x11-common [Installed]
  PreDepends: multiarch-support [Installed]
liblangtag1
  Depends: libc6 (>= 2.17) [Installed]
  Depends: liblangtag-common (= 0.5.7-2ubuntu1) [Installed]
  Depends: libxml2 (>= 2.7.4) [Installed]
liblangtag-common
libmythes-1.2-0
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libgcc1 (>= 1:4.1.1) [Installed]
  Depends: libstdc++6 (>= 4.1.1) [Installed]
libneon27-gnutls
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libgnutls30 (>= 3.4.2) [Installed]
  Depends: libgssapi-krb5-2 (>= 1.10+dfsg~) [Installed]
  Depends: libxml2 (>= 2.7.4) [Installed]
  Depends: zlib1g (>= 1:1.1.4) [Installed]
libnspr4
  Depends: libc6 (>= 2.15) [Installed]
libnspr4-0d
  Depends: libnspr4 (= 2:4.11-1ubuntu1) [Installed]
libnss3
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libnspr4 (>= 2:4.9-2~) [Installed]
  Depends: libnspr4-0d (>= 4.8.6) [NotInstalled]
  Depends: libnss3-nssdb [Installed]
  Depends: libsqlite3-0 (>= 3.5.9) [Installed]
  Depends: zlib1g (>= 1:1.1.4) [Installed]
libnss3-nssdb
  Depends: libnss3 (= 2:3.21-1ubuntu4) [Installed]
libnss3-1d
  Depends: libnss3 (= 2:3.21-1ubuntu4) [Installed]
librdf0
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libdb5.3 [Installed]
  Depends: libltdl7 (>= 2.4.6) [Installed]
  Depends: libraptor2-0 (>= 2.0.14) [Installed]
  Depends: librasqal3 (>= 0.9.31) [Installed]
libltdl7
  Depends: libc6 (>= 2.14) [Installed]
libraptor2-0
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libcurl3-gnutls (>= 7.16.2) [Installed]
  Depends: libxml2 (>= 2.7.4) [Installed]
  Depends: libxslt1.1 (>= 1.1.25) [Installed]
  Depends: libyajl2 (>= 2.0.4) [Installed]
  PreDepends: multiarch-support [Installed]
libxslt1.1
  Depends: libc6 (>= 2.17) [Installed]
  Depends: libgcrypt20 (>= 1.6.0) [Installed]
  Depends: libxml2 (>= 2.9.0) [Installed]
libyajl2
  Depends: libc6 (>= 2.14) [Installed]
  PreDepends: multiarch-support [Installed]
librasqal3
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libgmp10 [Installed]
  Depends: libmhash2 [Installed]
  Depends: libpcre3 [Installed]
  Depends: libraptor2-0 (>= 2.0.12) [Installed]
  Depends: libuuid1 (>= 2.16) [Installed]
  PreDepends: multiarch-support [Installed]
libmhash2
  Depends: libc6 (>= 2.4) [Installed]
  PreDepends: multiarch-support [Installed]
libuuid1
  Depends: libc6 (>= 2.4) [Installed]
  Depends: passwd [Installed]
passwd
  Depends: debianutils (>= 2.15.2) [Installed]
  Depends: libaudit1 (>= 1:2.2.1) [Installed]
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libpam-modules [Installed]
  Depends: libpam0g (>= 0.99.7.1) [Installed]
  Depends: libselinux1 (>= 1.32) [Installed]
  Depends: libsemanage1 (>= 2.0.3) [Installed]
  Depends: lsb-base (>= 4.1+Debian11ubuntu7) [Installed]
debianutils
  Depends: sensible-utils [Installed]
  PreDepends: libc6 (>= 2.15) [Installed]
sensible-utils
libaudit1
  Depends: libaudit-common (>= 1:2.4.5-1ubuntu2) [Installed]
  Depends: libc6 (>= 2.14) [Installed]
libaudit-common
libpam-modules
  PreDepends: debconf (>= 0.5) [Installed]
  PreDepends: debconf-2.0 [NotInstalled]
  PreDepends: libaudit1 (>= 1:2.2.1) [Installed]
  PreDepends: libc6 (>= 2.15) [Installed]
  PreDepends: libdb5.3 [Installed]
  PreDepends: libpam-modules-bin (= 1.1.8-3.2ubuntu2) [Installed]
  PreDepends: libpam0g (>= 1.1.3-2) [Installed]
  PreDepends: libselinux1 (>= 2.1.9) [Installed]
debconf-2.0
libpam-modules-bin
  Depends: libaudit1 (>= 1:2.2.1) [Installed]
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libpam0g (>= 0.99.7.1) [Installed]
  Depends: libselinux1 (>= 1.32) [Installed]
libpam0g
  Depends: debconf (>= 0.5) [Installed]
  Depends: debconf-2.0 [NotInstalled]
  Depends: libaudit1 (>= 1:2.2.1) [Installed]
  Depends: libc6 (>= 2.14) [Installed]
libsemanage1
  Depends: libaudit1 (>= 1:2.2.1) [Installed]
  Depends: libbz2-1.0 [Installed]
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libselinux1 (>= 2.1.12) [Installed]
  Depends: libsemanage-common (= 2.3-1build3) [Installed]
  Depends: libsepol1 (>= 2.1.4) [Installed]
  Depends: libustr-1.0-1 (>= 1.0.4) [Installed]
libsemanage-common
libsepol1
  Depends: libc6 (>= 2.14) [Installed]
libustr-1.0-1
  Depends: libc6 (>= 2.14) [Installed]
libreoffice-common
  Depends: libreoffice-style [NotInstalled]
  Depends: libreoffice-style-default [NotInstalled]
  Depends: ure [Installed]
  PreDepends: dpkg (>= 1.15.7.2~) [Installed]
libreoffice-style
libreoffice-style-default
ure
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libgcc1 (>= 1:3.0) [Installed]
  Depends: libstdc++6 (>= 5.2) [Installed]
  Depends: libxml2 (>= 2.7.4) [Installed]
  Depends: uno-libs3 (= 5.1.2-0ubuntu1) [Installed]
uno-libs3
  Depends: libc6 (>= 2.15) [Installed]
  Depends: libgcc1 (>= 1:3.0) [Installed]
  Depends: libstdc++6 (>= 5.2) [Installed]
librevenge-0.0-0
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libgcc1 (>= 1:3.0) [Installed]
  Depends: libstdc++6 (>= 5.2) [Installed]
  Depends: zlib1g (>= 1:1.1.4) [Installed]
libsm6
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libice6 (>= 1:1.0.0) [Installed]
  Depends: libuuid1 (>= 2.16) [Installed]
  PreDepends: multiarch-support [Installed]
lp-solve
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libcolamd2.9.1 [Installed]
libcolamd2.9.1
  Depends: libc6 (>= 2.4) [Installed]
  Depends: libsuitesparseconfig4.4.6 [Installed]
libsuitesparseconfig4.4.6
  Depends: libc6 (>= 2.17) [Installed]
libreoffice-base
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libgcc1 (>= 1:3.0) [Installed]
  Depends: libreoffice-base-core (= 1:5.1.2-0ubuntu1) [Installed]
  Depends: libreoffice-base-drivers (= 1:5.1.2-0ubuntu1) [NotInstalled]
  Depends: libreoffice-core (= 1:5.1.2-0ubuntu1) [Installed]
  Depends: libstdc++6 (>= 5) [Installed]
  Depends: uno-libs3 (>= 5.1.0~alpha) [Installed]
  Depends: ure [Installed]
libreoffice-base-core
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libgcc1 (>= 1:3.4) [Installed]
  Depends: libreoffice-core (= 1:5.1.2-0ubuntu1) [Installed]
  Depends: libstdc++6 (>= 5) [Installed]
  Depends: uno-libs3 (>= 5.1.0~alpha) [Installed]
  Depends: ure [Installed]
libreoffice-base-drivers
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libgcc1 (>= 1:3.0) [Installed]
  Depends: libreoffice-core (= 1:5.1.2-0ubuntu1) [Installed]
  Depends: libstdc++6 (>= 5) [Installed]
  Depends: uno-libs3 (>= 5.1.0~alpha) [Installed]
  Depends: ure [Installed]
libreoffice-calc
  Depends: libc6 (>= 2.23) [Installed]
  Depends: libetonyek-0.1-1 [Installed]
  Depends: libgcc1 (>= 1:3.0) [Installed]
  Depends: libicu55 (>= 55.1-1~) [Installed]
  Depends: libmwaw-0.3-3 [Installed]
  Depends: libodfgen-0.1-1 [Installed]
  Depends: liborcus-0.10-0v5 (>= 0.9.2-4ubuntu2) [Installed]
  Depends: libreoffice-base-core (= 1:5.1.2-0ubuntu1) [Installed]
  Depends: libreoffice-core (= 1:5.1.2-0ubuntu1) [Installed]
  Depends: librevenge-0.0-0 [Installed]
  Depends: libstdc++6 (>= 5.2) [Installed]
  Depends: libwps-0.4-4 [Installed]
  Depends: libxml2 (>= 2.7.4) [Installed]
  Depends: uno-libs3 (>= 5.1.0~alpha) [Installed]
  Depends: ure [Installed]
libetonyek-0.1-1
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libgcc1 (>= 1:3.0) [Installed]
  Depends: liblangtag1 (>= 0.5.0) [Installed]
  Depends: librevenge-0.0-0 [Installed]
  Depends: libstdc++6 (>= 5.2) [Installed]
  Depends: libxml2 (>= 2.7.4) [Installed]
  Depends: zlib1g (>= 1:1.1.4) [Installed]
libmwaw-0.3-3
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libgcc1 (>= 1:3.0) [Installed]
  Depends: librevenge-0.0-0 [Installed]
  Depends: libstdc++6 (>= 5.2) [Installed]
libodfgen-0.1-1
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libgcc1 (>= 1:3.0) [Installed]
  Depends: librevenge-0.0-0 [Installed]
  Depends: libstdc++6 (>= 5.2) [Installed]
liborcus-0.10-0v5
  Depends: libboost-iostreams1.58.0 [Installed]
  Depends: libboost-system1.58.0 [Installed]
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libgcc1 (>= 1:3.0) [Installed]
  Depends: libstdc++6 (>= 5.2) [Installed]
  Depends: zlib1g (>= 1:1.1.4) [Installed]
libboost-iostreams1.58.0
  Depends: libbz2-1.0 [Installed]
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libgcc1 (>= 1:3.0) [Installed]
  Depends: libstdc++6 (>= 5.2) [Installed]
  Depends: zlib1g (>= 1:1.1.4) [Installed]
libwps-0.4-4
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libgcc1 (>= 1:4.0) [Installed]
  Depends: librevenge-0.0-0 [Installed]
  Depends: libstdc++6 (>= 5.2) [Installed]
libreoffice-draw
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libcdr-0.1-1 [Installed]
  Depends: libdbus-1-3 (>= 1.9.14) [Installed]
  Depends: libfreehand-0.1-1 [Installed]
  Depends: libgcc1 (>= 1:3.0) [Installed]
  Depends: libglib2.0-0 (>= 2.15.0) [Installed]
  Depends: libmspub-0.1-1 [Installed]
  Depends: libmwaw-0.3-3 [Installed]
  Depends: libodfgen-0.1-1 [Installed]
  Depends: libpagemaker-0.0-0 (>= 0.0) [Installed]
  Depends: libreoffice-core (= 1:5.1.2-0ubuntu1) [Installed]
  Depends: librevenge-0.0-0 [Installed]
  Depends: libstdc++6 (>= 5.2) [Installed]
  Depends: libvisio-0.1-1 [Installed]
  Depends: libwpg-0.3-3 [Installed]
  Depends: libxml2 (>= 2.7.4) [Installed]
  Depends: uno-libs3 (>= 5.1.0~alpha) [Installed]
  Depends: ure [Installed]
  Depends: zlib1g (>= 1:1.1.4) [Installed]
libcdr-0.1-1
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libgcc1 (>= 1:3.0) [Installed]
  Depends: libicu55 (>= 55.1-1~) [Installed]
  Depends: liblcms2-2 (>= 2.2+git20110628) [Installed]
  Depends: librevenge-0.0-0 [Installed]
  Depends: libstdc++6 (>= 5.2) [Installed]
  Depends: zlib1g (>= 1:1.1.4) [Installed]
libfreehand-0.1-1
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libgcc1 (>= 1:3.0) [Installed]
  Depends: liblcms2-2 (>= 2.2+git20110628) [Installed]
  Depends: librevenge-0.0-0 [Installed]
  Depends: libstdc++6 (>= 4.1.1) [Installed]
  Depends: zlib1g (>= 1:1.1.4) [Installed]
libmspub-0.1-1
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libgcc1 (>= 1:3.0) [Installed]
  Depends: libicu55 (>= 55.1-1~) [Installed]
  Depends: librevenge-0.0-0 [Installed]
  Depends: libstdc++6 (>= 5.2) [Installed]
  Depends: zlib1g (>= 1:1.1.4) [Installed]
libpagemaker-0.0-0
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libgcc1 (>= 1:3.0) [Installed]
  Depends: librevenge-0.0-0 [Installed]
  Depends: libstdc++6 (>= 5.2) [Installed]
libvisio-0.1-1
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libgcc1 (>= 1:3.0) [Installed]
  Depends: libicu55 (>= 55.1-1~) [Installed]
  Depends: librevenge-0.0-0 [Installed]
  Depends: libstdc++6 (>= 5.2) [Installed]
  Depends: libxml2 (>= 2.7.4) [Installed]
libwpg-0.3-3
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libgcc1 (>= 1:3.0) [Installed]
  Depends: librevenge-0.0-0 [Installed]
  Depends: libstdc++6 (>= 4.1.1) [Installed]
  Depends: libwpd-0.10-10 [Installed]
libwpd-0.10-10
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libgcc1 (>= 1:3.0) [Installed]
  Depends: librevenge-0.0-0 [Installed]
  Depends: libstdc++6 (>= 5.2) [Installed]
libreoffice-impress
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libetonyek-0.1-1 [Installed]
  Depends: libgcc1 (>= 1:3.0) [Installed]
  Depends: libmwaw-0.3-3 [Installed]
  Depends: libodfgen-0.1-1 [Installed]
  Depends: libreoffice-core (= 1:5.1.2-0ubuntu1) [Installed]
  Depends: libreoffice-draw (= 1:5.1.2-0ubuntu1) [Installed]
  Depends: librevenge-0.0-0 [Installed]
  Depends: libstdc++6 (>= 5) [Installed]
  Depends: uno-libs3 (>= 5.1.0~alpha) [Installed]
  Depends: ure [Installed]
libreoffice-java-common
  Depends: libreoffice-common (= 1:5.1.2-0ubuntu1) [Installed]
libreoffice-math
  Depends: fonts-opensymbol [Installed]
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libgcc1 (>= 1:3.0) [Installed]
  Depends: libreoffice-core (= 1:5.1.2-0ubuntu1) [Installed]
  Depends: libstdc++6 (>= 5) [Installed]
  Depends: uno-libs3 (>= 5.1.0~alpha) [Installed]
  Depends: ure [Installed]
libreoffice-report-builder-bin
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libgcc1 (>= 1:3.0) [Installed]
  Depends: libreoffice-base [NotInstalled]
  Depends: libreoffice-core (= 1:5.1.2-0ubuntu1) [Installed]
  Depends: libstdc++6 (>= 5) [Installed]
  Depends: uno-libs3 (>= 5.1.0~alpha) [Installed]
  Depends: ure [Installed]
libreoffice-writer
  Depends: libabw-0.1-1v5 [Installed]
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libe-book-0.1-1 [Installed]
  Depends: libetonyek-0.1-1 [Installed]
  Depends: libgcc1 (>= 1:3.0) [Installed]
  Depends: libicu55 (>= 55.1-1~) [Installed]
  Depends: libmwaw-0.3-3 [Installed]
  Depends: libodfgen-0.1-1 [Installed]
  Depends: libreoffice-base-core (= 1:5.1.2-0ubuntu1) [Installed]
  Depends: libreoffice-core (= 1:5.1.2-0ubuntu1) [Installed]
  Depends: librevenge-0.0-0 [Installed]
  Depends: libstdc++6 (>= 5.2) [Installed]
  Depends: libwpd-0.10-10 [Installed]
  Depends: libwpg-0.3-3 [Installed]
  Depends: libwps-0.4-4 [Installed]
  Depends: libxml2 (>= 2.7.4) [Installed]
  Depends: uno-libs3 (>= 5.1.0~alpha) [Installed]
  Depends: ure [Installed]
  Depends: zlib1g (>= 1:1.1.4) [Installed]
libabw-0.1-1v5
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libgcc1 (>= 1:3.0) [Installed]
  Depends: librevenge-0.0-0 [Installed]
  Depends: libstdc++6 (>= 5.2) [Installed]
  Depends: libxml2 (>= 2.7.4) [Installed]
  Depends: zlib1g (>= 1:1.1.4) [Installed]
libe-book-0.1-1
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libgcc1 (>= 1:3.0) [Installed]
  Depends: libicu55 (>= 55.1-1~) [Installed]
  Depends: librevenge-0.0-0 [Installed]
  Depends: libstdc++6 (>= 5.2) [Installed]
  Depends: libxml2 (>= 2.7.4) [Installed]
  Depends: zlib1g (>= 1:1.1.4) [Installed]
python3-uno
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libgcc1 (>= 1:3.0) [Installed]
  Depends: libpython3.5 (>= 3.5.0~b1) [Installed]
  Depends: libreoffice-core (= 1:5.1.2-0ubuntu1) [Installed]
  Depends: libstdc++6 (>= 5) [Installed]
  Depends: python3 (<< 3.6) [Installed]
  Depends: python3.5 [Installed]
  Depends: uno-libs3 (>= 5.1.0~alpha) [Installed]
  Depends: ure [Installed]
libpython3.5
  Depends: libc6 (>= 2.17) [Installed]
  Depends: libexpat1 (>= 2.1~beta3) [Installed]
  Depends: libpython3.5-stdlib (= 3.5.1-10) [Installed]
  Depends: zlib1g (>= 1:1.2.0) [Installed]
libpython3.5-stdlib
  Depends: libbz2-1.0 [Installed]
  Depends: libc6 (>= 2.15) [Installed]
  Depends: libdb5.3 [Installed]
  Depends: libffi6 (>= 3.0.4) [Installed]
  Depends: liblzma5 (>= 5.1.1alpha+20120614) [Installed]
  Depends: libmpdec2 [Installed]
  Depends: libncursesw5 (>= 6) [Installed]
  Depends: libpython3.5-minimal (= 3.5.1-10) [Installed]
  Depends: libreadline6 (>= 6.0) [Installed]
  Depends: libsqlite3-0 (>= 3.5.9) [Installed]
  Depends: libtinfo5 (>= 6) [Installed]
  Depends: mime-support [Installed]
libmpdec2
  Depends: libc6 (>= 2.14) [Installed]
libncursesw5
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libtinfo5 (= 6.0+20160213-1ubuntu1) [Installed]
libpython3.5-minimal
  Depends: libc6 (>= 2.14) [Installed]
  Depends: libssl1.0.0 (>= 1.0.2~beta3) [Installed]
libssl1.0.0
  Depends: debconf (>= 0.5) [Installed]
  Depends: debconf-2.0 [NotInstalled]
  Depends: libc6 (>= 2.14) [Installed]
libreadline6
  Depends: libc6 (>= 2.15) [Installed]
  Depends: libtinfo5 (>= 6) [Installed]
  Depends: readline-common [Installed]
readline-common
  Depends: dpkg (>= 1.15.4) [Installed]
  Depends: install-info [Installed]
install-info
  Depends: libc6 (>= 2.14) [Installed]
  PreDepends: dpkg (>= 1.16.1) [Installed]
mime-support
python3
  Depends: dh-python [Installed]
  Depends: libpython3-stdlib (= 3.5.1-3) [Installed]
  Depends: python3.5 (>= 3.5.1-2~) [Installed]
  PreDepends: python3-minimal (= 3.5.1-3) [Installed]
dh-python
  Depends: python3:any (>= 3.3.2-2~) [NotInstalled]
python3:any
libpython3-stdlib
  Depends: libpython3.5-stdlib (>= 3.5.1-2~) [Installed]
python3.5
  Depends: libpython3.5-stdlib (= 3.5.1-10) [Installed]
  Depends: mime-support [Installed]
  Depends: python3.5-minimal (= 3.5.1-10) [Installed]
python3.5-minimal
  Depends: libexpat1 (>= 2.1~beta3) [Installed]
  Depends: libpython3.5-minimal (= 3.5.1-10) [Installed]
  Depends: zlib1g (>= 1:1.2.0) [Installed]
  PreDepends: libc6 (>= 2.17) [Installed]
python3-minimal
  Depends: dpkg (>= 1.13.20) [Installed]
  Depends: python3.5-minimal (>= 3.5.1-2~) [Installed]
user@hostname:~$ apt-rdepends -pr libreoffice
Reading package lists... Done
Building dependency tree       
Reading state information... Done
libreoffice
  Reverse Depends: libjodconverter-java (2.2.2-7) [NotInstalled]
  Reverse Depends: libreoffice-subsequentcheckbase (1:5.1.2-0ubuntu1) [NotInstalled]
libjodconverter-java
  Reverse Depends: jodconverter (>= 2.2.2-8) [NotInstalled]
  Reverse Depends: natbraille (2.0rc3-2) [NotInstalled]
jodconverter
natbraille
libreoffice-subsequentcheckbase

user@hostname:~$ sudo apt install signing-party
Reading package lists... Done
Building dependency tree       
Reading state information... Done
The following packages were automatically installed and are no longer required:
  libboost-program-options1.58.0 libfreetype6:i386 libfuse2:i386 libjs-modernizr
  libjs-underscore libllvm4.0 libllvm5.0 libpng12-0:i386 libqt4-help libqt4-scripttools
  libqt4-test libqtassistantclient4 python-qt4 python-sip xxdiff
Use 'sudo apt autoremove' to remove them.
The following additional packages will be installed:
  libb-hooks-op-check-perl libbareword-filehandles-perl libclass-method-modifiers-perl
  libclass-methodmaker-perl libclass-xsaccessor-perl libconvert-binhex-perl
  libdata-perl-perl libdevel-caller-perl libdevel-globaldestruction-perl
  libdevel-lexalias-perl libgd-perl libgnupg-interface-perl libimport-into-perl
  libindirect-perl liblexical-sealrequirehints-perl libmime-tools-perl
  libmodule-runtime-perl libmoo-perl libmoox-handlesvia-perl libmoox-late-perl
  libmultidimensional-perl libnet-idn-encode-perl libpadwalker-perl
  libparams-classify-perl librole-tiny-perl libstrictures-perl
  libsub-exporter-progressive-perl libterm-readkey-perl libtext-template-perl
  libtype-tiny-perl libtype-tiny-xs-perl postfix qprint
Suggested packages:
  libscalar-number-perl libdevel-stacktrace-perl procmail postfix-mysql postfix-pgsql
  postfix-ldap postfix-pcre sasl2-bin dovecot-common postfix-cdb postfix-doc wipe mutt
  texlive-latex-recommended texlive-latex-extra texlive-xetex fonts-droid
  texlive-font-utils qrencode
The following NEW packages will be installed:
  libb-hooks-op-check-perl libbareword-filehandles-perl libclass-method-modifiers-perl
  libclass-methodmaker-perl libclass-xsaccessor-perl libconvert-binhex-perl
  libdata-perl-perl libdevel-caller-perl libdevel-globaldestruction-perl
  libdevel-lexalias-perl libgd-perl libgnupg-interface-perl libimport-into-perl
  libindirect-perl liblexical-sealrequirehints-perl libmime-tools-perl
  libmodule-runtime-perl libmoo-perl libmoox-handlesvia-perl libmoox-late-perl
  libmultidimensional-perl libnet-idn-encode-perl libpadwalker-perl
  libparams-classify-perl librole-tiny-perl libstrictures-perl
  libsub-exporter-progressive-perl libterm-readkey-perl libtext-template-perl
  libtype-tiny-perl libtype-tiny-xs-perl postfix qprint signing-party
0 upgraded, 34 newly installed, 0 to remove and 0 not upgraded.
Need to get 2.758 kB of archives.
After this operation, 30,0 MB of additional disk space will be used.
Do you want to continue? [Y/n] y
Get:1 http://id.archive.ubuntu.com/ubuntu xenial/universe amd64 libb-hooks-op-check-perl amd64 0.19-2build2 [9.384 B]
Get:2 http://id.archive.ubuntu.com/ubuntu xenial/universe amd64 liblexical-sealrequirehints-perl amd64 0.009-1build1 [13,1 kB]
Get:3 http://id.archive.ubuntu.com/ubuntu xenial/universe amd64 libbareword-filehandles-perl amd64 0.003-1build3 [7.758 B]
Get:4 http://id.archive.ubuntu.com/ubuntu xenial/universe amd64 libclass-method-modifiers-perl all 2.11-1 [15,7 kB]
Get:5 http://id.archive.ubuntu.com/ubuntu xenial/universe amd64 libclass-methodmaker-perl amd64 2.24-1build1 [179 kB]
Get:5 http://id.archive.ubuntu.com/ubuntu xenial/universe amd64 libclass-methodmaker-perl amd64 2.24-1build1 [179 kB]
Get:5 http://id.archive.ubuntu.com/ubuntu xenial/universe amd64 libclass-methodmaker-perl amd64 2.24-1build1 [179 kB]
Get:5 http://id.archive.ubuntu.com/ubuntu xenial/universe amd64 libclass-methodmaker-perl amd64 2.24-1build1 [179 kB]
Get:5 http://id.archive.ubuntu.com/ubuntu xenial/universe amd64 libclass-methodmaker-perl amd64 2.24-1build1 [179 kB]
Get:5 http://id.archive.ubuntu.com/ubuntu xenial/universe amd64 libclass-methodmaker-perl amd64 2.24-1build1 [179 kB]
Get:5 http://id.archive.ubuntu.com/ubuntu xenial/universe amd64 libclass-methodmaker-perl amd64 2.24-1build1 [179 kB]
Get:6 http://id.archive.ubuntu.com/ubuntu xenial/universe amd64 libclass-xsaccessor-perl amd64 1.19-2build4 [31,7 kB]
Get:6 http://id.archive.ubuntu.com/ubuntu xenial/universe amd64 libclass-xsaccessor-perl amd64 1.19-2build4 [31,7 kB]
Get:7 http://id.archive.ubuntu.com/ubuntu xenial/main amd64 libconvert-binhex-perl all 1.125-1 [29,7 kB]
Get:8 http://id.archive.ubuntu.com/ubuntu xenial/universe amd64 libparams-classify-perl amd64 0.013-5build1 [21,1 kB]
Get:9 http://id.archive.ubuntu.com/ubuntu xenial/universe amd64 libmodule-runtime-perl all 0.014-2 [15,6 kB]
Get:10 http://id.archive.ubuntu.com/ubuntu xenial/universe amd64 librole-tiny-perl all 2.000001-2 [16,9 kB]
Get:11 http://id.archive.ubuntu.com/ubuntu xenial/universe amd64 libstrictures-perl all 2.000002-1 [17,4 kB]
Get:12 http://id.archive.ubuntu.com/ubuntu xenial/universe amd64 libdata-perl-perl all 0.002009-1 [49,6 kB]
Get:12 http://id.archive.ubuntu.com/ubuntu xenial/universe amd64 libdata-perl-perl all 0.002009-1 [49,6 kB]
Get:13 http://id.archive.ubuntu.com/ubuntu xenial/universe amd64 libpadwalker-perl amd64 2.2-1build1 [15,1 kB]
Get:14 http://id.archive.ubuntu.com/ubuntu xenial/universe amd64 libdevel-caller-perl amd64 2.06-1build3 [10,5 kB]
Get:15 http://id.archive.ubuntu.com/ubuntu xenial/universe amd64 libsub-exporter-progressive-perl all 0.001011-1 [7.064 B]
Get:16 http://id.archive.ubuntu.com/ubuntu xenial/universe amd64 libdevel-globaldestruction-perl all 0.13-1 [7.664 B]
Get:17 http://id.archive.ubuntu.com/ubuntu xenial/universe amd64 libdevel-lexalias-perl amd64 0.05-1build3 [8.514 B]
Get:18 http://id.archive.ubuntu.com/ubuntu xenial/universe amd64 libimport-into-perl all 1.002005-1 [11,0 kB]
Get:19 http://id.archive.ubuntu.com/ubuntu xenial/universe amd64 libmoo-perl all 2.000002-1 [57,1 kB]
Get:20 http://id.archive.ubuntu.com/ubuntu xenial/universe amd64 libmoox-handlesvia-perl all 0.001008-2 [21,5 kB]
Get:21 http://id.archive.ubuntu.com/ubuntu xenial/universe amd64 libtype-tiny-perl all 1.000005-1 [247 kB]
Get:21 http://id.archive.ubuntu.com/ubuntu xenial/universe amd64 libtype-tiny-perl all 1.000005-1 [247 kB]
Get:21 http://id.archive.ubuntu.com/ubuntu xenial/universe amd64 libtype-tiny-perl all 1.000005-1 [247 kB]
Get:22 http://id.archive.ubuntu.com/ubuntu xenial/universe amd64 libmoox-late-perl all 0.015-2 [11,8 kB]
Get:23 http://id.archive.ubuntu.com/ubuntu xenial/universe amd64 libgnupg-interface-perl all 0.52-2 [61,4 kB]
Get:24 http://id.archive.ubuntu.com/ubuntu xenial/universe amd64 libindirect-perl amd64 0.36-1build1 [21,8 kB]
Get:25 http://id.archive.ubuntu.com/ubuntu xenial/main amd64 libmime-tools-perl all 5.507-1 [207 kB]
Get:26 http://id.archive.ubuntu.com/ubuntu xenial/universe amd64 libmultidimensional-perl amd64 0.010-1build3 [6.880 B]
Get:27 http://id.archive.ubuntu.com/ubuntu xenial/universe amd64 libnet-idn-encode-perl amd64 2.300-1build1 [74,0 kB]
Get:28 http://id.archive.ubuntu.com/ubuntu xenial/universe amd64 libterm-readkey-perl amd64 2.33-1build1 [27,2 kB]
Get:29 http://id.archive.ubuntu.com/ubuntu xenial/universe amd64 libtext-template-perl all 1.46-1 [51,5 kB]
Get:30 http://id.archive.ubuntu.com/ubuntu xenial/universe amd64 libtype-tiny-xs-perl amd64 0.012-1build1 [22,9 kB]
Get:31 http://id.archive.ubuntu.com/ubuntu xenial-updates/main amd64 postfix amd64 3.1.0-3ubuntu0.3 [1.152 kB]
Get:31 http://id.archive.ubuntu.com/ubuntu xenial-updates/main amd64 postfix amd64 3.1.0-3ubuntu0.3 [1.152 kB]
Get:32 http://id.archive.ubuntu.com/ubuntu xenial/universe amd64 qprint amd64 1.1.dfsg.2-2 [9.234 B]
Get:33 http://id.archive.ubuntu.com/ubuntu xenial/main amd64 libgd-perl amd64 2.53-2.1 [162 kB]
Get:34 http://id.archive.ubuntu.com/ubuntu xenial/universe amd64 signing-party amd64 2.2-1 [157 kB]
Fetched 2.177 kB in 26min 29s (1.369 B/s)                                                
Extracting templates from packages: 100%
Preconfiguring packages ...
Selecting previously unselected package libb-hooks-op-check-perl.
(Reading database ... 282997 files and directories currently installed.)
Preparing to unpack .../libb-hooks-op-check-perl_0.19-2build2_amd64.deb ...
Unpacking libb-hooks-op-check-perl (0.19-2build2) ...
Selecting previously unselected package liblexical-sealrequirehints-perl.
Preparing to unpack .../liblexical-sealrequirehints-perl_0.009-1build1_amd64.deb ...
Unpacking liblexical-sealrequirehints-perl (0.009-1build1) ...
Selecting previously unselected package libbareword-filehandles-perl.
Preparing to unpack .../libbareword-filehandles-perl_0.003-1build3_amd64.deb ...
Unpacking libbareword-filehandles-perl (0.003-1build3) ...
Selecting previously unselected package libclass-method-modifiers-perl.
Preparing to unpack .../libclass-method-modifiers-perl_2.11-1_all.deb ...
Unpacking libclass-method-modifiers-perl (2.11-1) ...
Selecting previously unselected package libclass-methodmaker-perl.
Preparing to unpack .../libclass-methodmaker-perl_2.24-1build1_amd64.deb ...
Unpacking libclass-methodmaker-perl (2.24-1build1) ...
Selecting previously unselected package libclass-xsaccessor-perl.
Preparing to unpack .../libclass-xsaccessor-perl_1.19-2build4_amd64.deb ...
Unpacking libclass-xsaccessor-perl (1.19-2build4) ...
Selecting previously unselected package libconvert-binhex-perl.
Preparing to unpack .../libconvert-binhex-perl_1.125-1_all.deb ...
Unpacking libconvert-binhex-perl (1.125-1) ...
Selecting previously unselected package libparams-classify-perl.
Preparing to unpack .../libparams-classify-perl_0.013-5build1_amd64.deb ...
Unpacking libparams-classify-perl (0.013-5build1) ...
Selecting previously unselected package libmodule-runtime-perl.
Preparing to unpack .../libmodule-runtime-perl_0.014-2_all.deb ...
Unpacking libmodule-runtime-perl (0.014-2) ...
Selecting previously unselected package librole-tiny-perl.
Preparing to unpack .../librole-tiny-perl_2.000001-2_all.deb ...
Unpacking librole-tiny-perl (2.000001-2) ...
Selecting previously unselected package libstrictures-perl.
Preparing to unpack .../libstrictures-perl_2.000002-1_all.deb ...
Unpacking libstrictures-perl (2.000002-1) ...
Selecting previously unselected package libdata-perl-perl.
Preparing to unpack .../libdata-perl-perl_0.002009-1_all.deb ...
Unpacking libdata-perl-perl (0.002009-1) ...
Selecting previously unselected package libpadwalker-perl.
Preparing to unpack .../libpadwalker-perl_2.2-1build1_amd64.deb ...
Unpacking libpadwalker-perl (2.2-1build1) ...
Selecting previously unselected package libdevel-caller-perl.
Preparing to unpack .../libdevel-caller-perl_2.06-1build3_amd64.deb ...
Unpacking libdevel-caller-perl (2.06-1build3) ...
Selecting previously unselected package libsub-exporter-progressive-perl.
Preparing to unpack .../libsub-exporter-progressive-perl_0.001011-1_all.deb ...
Unpacking libsub-exporter-progressive-perl (0.001011-1) ...
Selecting previously unselected package libdevel-globaldestruction-perl.
Preparing to unpack .../libdevel-globaldestruction-perl_0.13-1_all.deb ...
Unpacking libdevel-globaldestruction-perl (0.13-1) ...
Selecting previously unselected package libdevel-lexalias-perl.
Preparing to unpack .../libdevel-lexalias-perl_0.05-1build3_amd64.deb ...
Unpacking libdevel-lexalias-perl (0.05-1build3) ...
Selecting previously unselected package libimport-into-perl.
Preparing to unpack .../libimport-into-perl_1.002005-1_all.deb ...
Unpacking libimport-into-perl (1.002005-1) ...
Selecting previously unselected package libmoo-perl.
Preparing to unpack .../libmoo-perl_2.000002-1_all.deb ...
Unpacking libmoo-perl (2.000002-1) ...
Selecting previously unselected package libmoox-handlesvia-perl.
Preparing to unpack .../libmoox-handlesvia-perl_0.001008-2_all.deb ...
Unpacking libmoox-handlesvia-perl (0.001008-2) ...
Selecting previously unselected package libtype-tiny-perl.
Preparing to unpack .../libtype-tiny-perl_1.000005-1_all.deb ...
Unpacking libtype-tiny-perl (1.000005-1) ...
Selecting previously unselected package libmoox-late-perl.
Preparing to unpack .../libmoox-late-perl_0.015-2_all.deb ...
Unpacking libmoox-late-perl (0.015-2) ...
Selecting previously unselected package libgnupg-interface-perl.
Preparing to unpack .../libgnupg-interface-perl_0.52-2_all.deb ...
Unpacking libgnupg-interface-perl (0.52-2) ...
Selecting previously unselected package libindirect-perl.
Preparing to unpack .../libindirect-perl_0.36-1build1_amd64.deb ...
Unpacking libindirect-perl (0.36-1build1) ...
Selecting previously unselected package libmime-tools-perl.
Preparing to unpack .../libmime-tools-perl_5.507-1_all.deb ...
Unpacking libmime-tools-perl (5.507-1) ...
Selecting previously unselected package libmultidimensional-perl.
Preparing to unpack .../libmultidimensional-perl_0.010-1build3_amd64.deb ...
Unpacking libmultidimensional-perl (0.010-1build3) ...
Selecting previously unselected package libnet-idn-encode-perl.
Preparing to unpack .../libnet-idn-encode-perl_2.300-1build1_amd64.deb ...
Unpacking libnet-idn-encode-perl (2.300-1build1) ...
Selecting previously unselected package libterm-readkey-perl.
Preparing to unpack .../libterm-readkey-perl_2.33-1build1_amd64.deb ...
Unpacking libterm-readkey-perl (2.33-1build1) ...
Selecting previously unselected package libtext-template-perl.
Preparing to unpack .../libtext-template-perl_1.46-1_all.deb ...
Unpacking libtext-template-perl (1.46-1) ...
Selecting previously unselected package libtype-tiny-xs-perl.
Preparing to unpack .../libtype-tiny-xs-perl_0.012-1build1_amd64.deb ...
Unpacking libtype-tiny-xs-perl (0.012-1build1) ...
Selecting previously unselected package postfix.
Preparing to unpack .../postfix_3.1.0-3ubuntu0.3_amd64.deb ...
Unpacking postfix (3.1.0-3ubuntu0.3) ...
Selecting previously unselected package qprint.
Preparing to unpack .../qprint_1.1.dfsg.2-2_amd64.deb ...
Unpacking qprint (1.1.dfsg.2-2) ...
Selecting previously unselected package libgd-perl.
Preparing to unpack .../libgd-perl_2.53-2.1_amd64.deb ...
Unpacking libgd-perl (2.53-2.1) ...
Selecting previously unselected package signing-party.
Preparing to unpack .../signing-party_2.2-1_amd64.deb ...
Unpacking signing-party (2.2-1) ...
Processing triggers for man-db (2.7.5-1) ...
Processing triggers for libc-bin (2.23-0ubuntu10) ...
Processing triggers for ufw (0.35-0ubuntu2) ...
Processing triggers for systemd (229-4ubuntu21.15) ...
Processing triggers for ureadahead (0.100.0-19) ...
ureadahead will be reprofiled on next reboot
Setting up libb-hooks-op-check-perl (0.19-2build2) ...
Setting up liblexical-sealrequirehints-perl (0.009-1build1) ...
Setting up libbareword-filehandles-perl (0.003-1build3) ...
Setting up libclass-method-modifiers-perl (2.11-1) ...
Setting up libclass-methodmaker-perl (2.24-1build1) ...
Setting up libclass-xsaccessor-perl (1.19-2build4) ...
Setting up libconvert-binhex-perl (1.125-1) ...
Setting up libparams-classify-perl (0.013-5build1) ...
Setting up libmodule-runtime-perl (0.014-2) ...
Setting up librole-tiny-perl (2.000001-2) ...
Setting up libstrictures-perl (2.000002-1) ...
Setting up libdata-perl-perl (0.002009-1) ...
Setting up libpadwalker-perl (2.2-1build1) ...
Setting up libdevel-caller-perl (2.06-1build3) ...
Setting up libsub-exporter-progressive-perl (0.001011-1) ...
Setting up libdevel-globaldestruction-perl (0.13-1) ...
Setting up libdevel-lexalias-perl (0.05-1build3) ...
Setting up libimport-into-perl (1.002005-1) ...
Setting up libmoo-perl (2.000002-1) ...
Setting up libmoox-handlesvia-perl (0.001008-2) ...
Setting up libtype-tiny-perl (1.000005-1) ...
Setting up libmoox-late-perl (0.015-2) ...
Setting up libgnupg-interface-perl (0.52-2) ...
Setting up libindirect-perl (0.36-1build1) ...
Setting up libmime-tools-perl (5.507-1) ...
Setting up libmultidimensional-perl (0.010-1build3) ...
Setting up libnet-idn-encode-perl (2.300-1build1) ...
Setting up libterm-readkey-perl (2.33-1build1) ...
Setting up libtext-template-perl (1.46-1) ...
Setting up libtype-tiny-xs-perl (0.012-1build1) ...
Setting up postfix (3.1.0-3ubuntu0.3) ...
Adding group `postfix' (GID 131) ...
Done.
Adding system user `postfix' (UID 122) ...
Adding new user `postfix' (UID 122) with group `postfix' ...
Not creating home directory `/var/spool/postfix'.
Creating /etc/postfix/dynamicmaps.cf
Adding group `postdrop' (GID 132) ...
Done.
setting myhostname: bagidata-pc
setting alias maps
setting alias database
mailname is not a fully qualified domain name.  Not changing /etc/mailname.
setting destinations: $myhostname, bagidata-pc, localhost.localdomain, , localhost
setting relayhost: 
setting mynetworks: 127.0.0.0/8 [::ffff:127.0.0.0]/104 [::1]/128
setting mailbox_size_limit: 0
setting recipient_delimiter: +
setting inet_interfaces: all
setting inet_protocols: all
/etc/aliases does not exist, creating it.
WARNING: /etc/aliases exists, but does not have a root alias.

Postfix is now set up with a default configuration.  If you need to make 
changes, edit
/etc/postfix/main.cf (and others) as needed.  To view Postfix configuration
values, see postconf(1).

After modifying main.cf, be sure to run '/etc/init.d/postfix reload'.

Running newaliases
Setting up qprint (1.1.dfsg.2-2) ...
Setting up libgd-perl (2.53-2.1) ...
Setting up signing-party (2.2-1) ...
Processing triggers for libc-bin (2.23-0ubuntu10) ...
Processing triggers for systemd (229-4ubuntu21.15) ...
Processing triggers for ureadahead (0.100.0-19) ...
Processing triggers for ufw (0.35-0ubuntu2) ...


user@hostname:~$ apt-rdepends -d libreoffice | springgraph > libreoffice.png
Reading package lists... Done
Building dependency tree       
Reading state information... Done
springgraph iterating until reaches 0.3

76.4066958159975
45.4869609834106
34.4920603147454
27.2236536865645
23.6642651018263
...
0.3056012371465
0.302572610016509
Iterations: 11236
user@hostname:~$ 
```
