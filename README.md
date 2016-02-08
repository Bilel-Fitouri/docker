# Glu
 docker build -t glu . <br/>
 docker run -p 8080:8080 --name glu -d glu start
 
# Tomcat
 docker build -t tomcat .<br/>
 docker run --name tomcat -p 8080:8080 tomcat
 
# Redis
 docker build -t redis . <br/>
 docker run --name redis -p 8080:8080 redis
