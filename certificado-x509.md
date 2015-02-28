# Creación de un certificado X509 para nuestro servidor proxy inverso

Nos basamos en la documentación publicada en http://olea.org/diario/archive/2014/Ene.-15-1.html

Descargamos el script para generar nuestra solicitud de certificado para el servidor:

``` console
$ curl http://svn.cacert.org/CAcert/Software/CSRGenerator/csr -o csr.sh
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  4251  100  4251    0     0   3108      0  0:00:01  0:00:01 --:--:--  3107
``` 

Y lo lanzamos:
``` console
$ sh csr.sh
Private Key and Certificate Signing Request Generator
This script was designed to suit the request format needed by
the CAcert Certificate Authority. www.CAcert.org

Short Hostname (ie. imap big_srv www2): odoo
FQDN/CommonName (ie. www.example.com) : proxy.ejemplo.com
Type SubjectAltNames for the certificate, one per line. Enter a blank line to finish
SubjectAltName: DNS:
Running OpenSSL...
Generating a 2048 bit RSA private key
..................................................+++
.....................+++
writing new private key to '/home/usuario/odoo_privatekey.pem'
-----
Copy the following Certificate Request and paste into CAcert website to obtain a Certificate.
When you receive your certificate, you 'should' name it something like odoo_server.pem

-----BEGIN CERTIFICATE REQUEST-----
blahblahblahblahblahblahblahblahblahblahblahblahblahblahblahblah
blahblahblahblahblahblahblahblahblahblahblahblahblahblahblahblah
blahblahblahblahblahblahblahblahblahblahblahblahblahblahblahblah
blahblahblahblahblahblahblahblahblahblahblahblahblahblahblahblah
blahblahblahblahblahblahblahblahblahblahblahblahblahblahblahblah
blahblahblahblahblahblahblahblahblahblahblahblahblahblahblahblah
blahblahblahblahblahblahblahblahblahblahblahblahblahblahblahblah
blahblahblahblahblahblahblahblahblahblahblahblahblahblahblahblah
blahblahblahblahblahblahblahblahblahblahblahblahblahblahblahblah
blahblahblahblahblahblahblahblahblahblahblahblahblahblahblahblah
blahblahblahblahblahblahblahblahblahblahblahblahblahblahblahblah
blahblahblahblahblahblahblahblahblahblahblahblahblahblahblahblah
blahblahblahblahblahblahblahblahblahblahblah
-----END CERTIFICATE REQUEST-----

The Certificate request is also available in /home/usuario/odoo_csr.pem
The Private Key is stored in /home/usuario/odoo_privatekey.pem

```

