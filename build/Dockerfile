FROM archlinux as build-deps


RUN pacman -Sy --noconfirm git curl
RUN git clone https://github.com/rotki/rotki.git
WORKDIR /rotki
RUN pacman -Sy --noconfirm python-pip
RUN pacman -Sy --noconfirm zeromq
RUN pacman -Sy --noconfirm nodejs
RUN pacman -Sy --noconfirm make npm
RUN pacman -Sy --noconfirm sqlcipher
RUN pacman -Sy --noconfirm gcc 
RUN pacman -Sy --noconfirm python-virtualenv

RUN virtualenv rotki
RUN pip install -r requirements.txt
RUN pip install -r requirements_dev.txt

ENTRYPOINT echo "Starting API" && python -m rotkehlchen --loglevel debug
# RUN ls -l
# RUN ls -l rotki

#RUN npm install && npm start

#RUN python -m pip install --upgrade pip eth_utils


#RUN ./package.sh

#ENTRYPOINT /opt/rotki-linux-x64-v1.0.4/rotki-v1.0.4
