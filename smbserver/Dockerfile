# Version: 0.0.1
# Aitor Galilea@edt M06 2018-2019
# Servidor SAMBA con LDAP como backend
#-------------------------------------
FROM fedora:27
LABEL author="@edt ASIX M06-ASO"
LABEL description="SAMBA server 2018-2019"
RUN dnf -y install procps passwd samba samba-client openldap-clients nss-pam-ldapd authconfig smbldap-tools
RUN mkdir /opt/docker
COPY * /opt/docker/
RUN chmod +x /opt/docker/install.sh /opt/docker/startup.sh /opt/docker/authconfig.conf
WORKDIR /opt/docker
CMD ["/opt/docker/startup.sh"]

