FROM phpdockerio/php:8.1-fpm
WORKDIR "/application"

RUN apt-get update; \
    apt-get -y --no-install-recommends install \
    git \ 
    php8.1-bcmath \ 
    php8.1-gd \ 
    php8.1-imagick \ 
    php8.1-imap \ 
    php8.1-mysql \ 
    php8.1-pgsql; \
    apt-get clean; \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*

RUN apt-get install -y curl 
RUN curl -fsSL https://deb.nodesource.com/setup_19.x |bash - &&\
apt-get install -y nodejs

RUN npm install puppeteer
RUN apt-get install -y wget
RUN apt-get install -y fonts-liberation libasound2 libatk-bridge2.0-0  libatk1.0-0 libatspi2.0-0 libdbus-1-3 libgbm1 libglib2.0-0 libx11-6 libxcomposite1 libxdamage1 libxfixes3 libxkbcommon0 libxrandr2 xdg-utils libnspr4 libnss3 libu2f-udev libvulkan1 
RUN wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
RUN dpkg -i google-chrome-stable_current_amd64.deb
RUN apt -f install
RUN apt install google-chrome-stable


