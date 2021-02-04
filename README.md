# Welcome to Managing Ports Module

To Run the Image on your local first clone this Repo:

    $ git clone git@github.com:dahiyaashish/managing-ports.git
    $ cd managing-ports
    $ docker build -t apacheimage . #You can change the apacheimage name to any name
    $ docker run -it -d -p 8080:80 apacheimage #Replace the apacheimage with your image name
    $ docker ps | grep apacheimage # Replace the apacheimage with your image name
    $ curl -v -XGET http://localhost:8080 # Or open browser and hit http://localhost:8080
   
   You can mention as many port you want based on your application like:

    $ docker run -it -p 127.0.0.1:8080:80,127.0.0.1:8081:443 image_name
    $ docker run -it -p 192.168.1.111:8080:80,92.168.1.111:8081:443 image_name

