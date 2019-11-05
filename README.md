# Instalacion-Kivy
 Instalación manual (en Raspbian Jessie / Stretch) 
Pasos:
  1.-Istrucciones, para Python 3.

Instalar las dependencias:

sudo apt update
sudo apt install libsdl2-dev libsdl2-image-dev libsdl2-mixer-dev libsdl2-ttf-dev \
   pkg-config libgl1-mesa-dev libgles2-mesa-dev \
   python3-setuptools libgstreamer1.0-dev git-core \
   gstreamer1.0-plugins-{bad,base,good,ugly} \
   gstreamer1.0-{omx,alsa} python3-dev libmtdev-dev \
   xclip xsel libjpeg-dev
Instalar dependencias de pip:

python3 -m pip install --upgrade --user pip setuptools
python3 -m pip install --upgrade --user Cython == 0.29.10 pillow

Si da un error de Cython de que no tiene un PATH le ponemos en el barshscr en la ultima linea.
export PATH=/home/pi/.local/bin:$PATH 

Instale Kivy a Python globalmente

Puede instalarlo como un paquete normal de Python3 con:

# to get the last release from pypi
  python3 -m pip install --user kivy

# to install master
  python3 -m pip install --user https://github.com/kivy/kivy/archive/master.zip

# or clone locally then pip install
  git clone https://github.com/kivy/kivy
  cd kivy
  python3 -m pip install --user .
