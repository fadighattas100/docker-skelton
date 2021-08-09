
FROM  ubuntu:18.04
ENV TZ=America/Los_Angeles
#ENV APACHE_DOCUMENT_ROOT /var/www/html

USER root

RUN apt-get update && apt-get upgrade -y
RUN apt-get install -y git \
 apt-utils \
 curl \
 vim \
 #apache2 \
 zip \
 unzip \
 python \
 python-pip \
 python3 \
 python3-pip

RUN python --version
RUN pip --version
RUN python3 --version
RUN pip3 --version


#https://stackoverflow.com/questions/36399848/install-node-in-dockerfile
#https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-ubuntu-20-04
#https://nodejs.org/en/
#Node 
ENV NODE_VERSION=14.17.4
RUN curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash
ENV NVM_DIR=/root/.nvm
RUN . "$NVM_DIR/nvm.sh" && nvm install ${NODE_VERSION}
RUN . "$NVM_DIR/nvm.sh" && nvm use v${NODE_VERSION}
RUN . "$NVM_DIR/nvm.sh" && nvm alias default v${NODE_VERSION}
ENV PATH="/root/.nvm/versions/node/v${NODE_VERSION}/bin/:${PATH}"
RUN node --version
RUN npm --version

		
WORKDIR /var/www/html 

#run apache from docker file
#CMD ["apachectl", "-D", "FOREGROUND"]

EXPOSE 80

#RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
#RUN apt-get install -y php libapache2-mod-php php-mysql php7.2-cli php7.2-curl php7.2-gd php7.2-mbstring php7.2-mysql php7.2-xml php-xml
#RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

#RUN sed -ri -e 's#DocumentRoot /var/www/html#DocumentRoot /var/www/html#' /etc/apache2/sites-available/000-default.conf

#RUN git clone https://github.com/csuntechlab/affinity.git

RUN mkdir -p /var/www/html/UI/;

#you don't need copy it's already will be copied form docker-composer
#    volumes:
#     - ../code/:/var/www/html/UI/
#COPY ./code /var/www/html/UI/

#RUN chown -hR www-data:www-data project-folder/
#RUN ln -s /var/www/html/project-folder/ public

WORKDIR /var/www/html/project-folder/
#RUN composer install

