# SpringBoot-H2-database
##How To use H2-database
1)First you need to add the h2- database dependency.
2)Inside the application.properties file write 
  spring.datasource.url=jdbc:h2:mem:testdb                     #If you don't want to persisit the data
  spring.datasource.url=jdbc:h2:file:D:/h2db/ecartjpa          #If you want to persist the data
  spring.datasource.driverClassName=org.h2.Driver
  spring.datasource.username=sa
  spring.datasource.password=password
  spring.jpa.database-platform=org.hibernate.dialect.H2Dialect
  
  Imp things
  Inside the src/main/resource folder create
  1) schema.sql 
   { write the query for table creation
    for eg- 
           DROP TABLE IF EXISTS CATEGORIES;

           CREATE TABLE CATEGORIES(category_id INT PRIMARY_KEY AUTO_INCREMENT,category_nameVARCHAR(200));
           
   }
   
  2) data.sql
     {
     INSERT INTO CATEGORIES VALUES(?,?,?);
     }
     
     
                   
  
