FROM scratch
MAINTAINER Michael A. Smith <msmith3@ebay.com>
ADD mysql_files.tar.xz .
ENV MYSQL_MAJOR 5.5
ENV MYSQL_VERSION 5.5.43
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin
ENV PATH $PATH:/bin:/usr/local/mysql/bin:/usr/local/mysql/scripts
ENV MYSQL_ROOT_PASSWORD mage
ENV MYSQL_USER mage
ENV MYSQL_PASSWORD mage
ENV MYSQL_DATABASE mage
ENTRYPOINT ["/entrypoint.sh"]
EXPOSE 3306
CMD ["mysqld"]
RUN /entrypoint.sh mysqld \
  & sleep 10 \
 && kill $! \
 && wait $!
