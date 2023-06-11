Steps I Followed
1.)Creating two directories in root directory (/var/www/html) named as Website 1 and Website 2 using command mkdir website1 /website2.
2)Create index.html find using vi /var/www/html/website1 and entering a simple html code given below.
 <!DOCTYPE html>
<html>
<head>
    <title>Web Gawd can stop you anywhere</title>
</head>
<body>
    <h1>Forbidden by Web Gawd</h1>
    <p>You should be an Authenticated user. Contact web gawd!</p>
</body>
</html>

3) Editing Hosts File and entering ip's wrt website name (vi /etc/hosts) ![Screenshot (27)]   (https://github.com/PclubLAMPStack/virtual-hosting-and-security-Gautam-405/assets/130830945/a545b2d1-e970-43bc-9b71-a414b67b8928)
4) Editing ifcfg-ens33 file (vi /etc/sysconfig/ifcfg-ens33)![Screenshot (28)](https://github.com/PclubLAMPStack/virtual-hosting-and-security-Gautam-405/assets/130830945/481c4412-b10d-4f14-a533-ded64bd84438)

5) Editing httpd.conf file (vi /etc/httpd/conf/httpd.conf)![Screenshot (29)](https://github.com/PclubLAMPStack/virtual-hosting-and-security-Gautam-405/assets/130830945/a783c4ab-83b0-4692-b6eb-20a09a909e1a)

6) Adding forbidden.html to noindex directory in /usr/share/httpd/noindex(vi /usr/share/httpd/noindex/forbidden.html)![Screenshot (30)](https://github.com/PclubLAMPStack/virtual-hosting-and-security-Gautam-405/assets/130830945/f3e2d419-e0cc-4d40-8c5a-5661a02c0db0)

7) Editing welcome.conf file in /etc/httpd/conf.d (vi /etc/httpd/conf.d/welcome.conf) to get desrired output when error  of authorization is executed.![Screenshot (37)](https://github.com/PclubLAMPStack/virtual-hosting-and-security-Gautam-405/assets/130830945/1c1940fd-916a-46dd-b227-36c425df742e)

8) Creating users-
   htpasswd -c -w /etc/httpd/webpass user1
   htpasswd  -w /etc/httpd/webpass user2
   htpasswd  -w /etc/httpd/webpass user3
   htpasswd  -w /etc/httpd/webpass user4
9)   Accessing websites from c 10 & c20
      C10-
      Reaching website 2-![Screenshot (33)](https://github.com/PclubLAMPStack/virtual-hosting-and-security-Gautam-405/assets/130830945/14fd40d6-8d42-4b65-b7b6-52717c2462ed)
      Reaching website 1 from user 1  & 3 -![Screenshot (32)](https://github.com/PclubLAMPStack/virtual-hosting-and-security-Gautam-405/assets/130830945/1faca042-4bb7-4315-9007-a3af76b9a4f8)
      Reaching website 1 from user2 -![Screenshot (34)](https://github.com/PclubLAMPStack/virtual-hosting-and-security-Gautam-405/assets/130830945/8c764b1c-4141-4dd6-8ead-5856d917c0c1)
       C20-
       Reaching Website 1 -![Screenshot (40)](https://github.com/PclubLAMPStack/virtual-hosting-and-security-Gautam-405/assets/130830945/1e297ece-ff8f-4548-b078-6c9a6c1137bc)
       Reaching website 2 from user 1-![Screenshot (35)](https://github.com/PclubLAMPStack/virtual-hosting-and-security-Gautam-405/assets/130830945/7857f8cd-22be-4e96-a05f-7b7847955ef2)
       ![Screenshot (36)](https://github.com/PclubLAMPStack/virtual-hosting-and-security-Gautam-405/assets/130830945/bb8c8dc4-82b4-4ff3-a62c-84745bbfdfff)

