CLAVIN Rest
===========

## Quick Start 

### Download the CLAVIN Rest Server 

    curl -L https://github.com/tlpinney/CLAVIN-rest/releases/download/0.2.0/clavin-rest-0.2.0.jar -o clavin-rest.jar

### Download Geonames 
  
    curl -O http://download.geonames.org/export/dump/allCountries.zip

### Unzip Geonames 

    unzip allCountries.zip

### Download CLAVIN yaml configuration file 

    curl -O https://raw.githubusercontent.com/Berico-Technologies/CLAVIN-rest/master/clavin-rest.yml 

### Create a CLAVIN gazetteer 
    
    java -Xmx4096m -jar clavin-rest.jar index clavin-rest.yml

### Run the CLAVIN rest server 

    java -Xmx2048m -jar clavin-rest.jar server clavin-rest.yml 

### Geotag an article  

    curl -O https://raw.githubusercontent.com/Berico-Technologies/CLAVIN/master/src/test/resources/sample-docs/Somalia-doc.txt

    curl -s --data @Somalia-doc.txt --header "Content-Type: text/plain" http://localhost:9090/api/v0/geotag


## Package creation 

    git clone https://github.com/Berico-Technologies/CLAVIN-rest
    cd CLAVIN-rest
    mvn package 


