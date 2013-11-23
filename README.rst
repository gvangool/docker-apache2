docker-apache2
==============
This is a small base image for Apache2 (PHP?) containers.

So you could do something like::

  FROM gvangool/apache2
  RUN apt-get update && apt-get install -y php5 libapache2-mod-php5 php5-mysql php5-cli
  RUN a2enmod rewrite && a2enmod php
  ADD site.conf /etc/apache2/sites-enabled/
  ADD src /var/www/
