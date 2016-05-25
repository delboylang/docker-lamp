# docker-lamp

# Php5.6 with Apache and mysql. 

Once checked out open the command line client in the directory, i tend to use git bash. 

docker-machine start default  

Will bring up docker machine 

eval $(docker-machine env default ) 

will set the correct path for windows bash  

docker-compose up -d

Will instantiate the machine and get everything working 

You can then get onto said machine and do what you want with it the command below

winpty docker exec -i -t ss4_web_1 bash (if on git bash )

then run the below 

composer create-project silverstripe/installer /var/www/silverstripe/public  4.0.0-alpha1

Will install 

Other usefull commands 

docker rm $(docker ps -a -q) -f
Will remove any running docker files . 

Check the docker-compose file for any database conection fields. 