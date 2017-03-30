# coursera-dwbi
Materials for Coursera: Data Warehousing for Business Intelligence

### build
- oracle
  - oracle has been downloaded to 12.2.0.1/linux64_12202_database.zip
  - run `./buildDockerImage.sh`
- pentaho/pivot4j
  - pentaho has been unzipped to ./pentaho-server
  - pivot4j plugin unzipped to ./pentaho-server/pentaho-solutions/system
  ```
  docker build -f Dockerfile.pentaho -t pentaho .
  ```

### debug
```
docker run --rm --name db \
    -v $PWD/data:/opt/oracle/oradata \
    -v $PWD:/usr/src \
    -p 1521:1521 -p 5500:5500 \
    -ti oracle/database:12.2.0.1-ee

# password below changes whenever new data directory is mounted
docker exec -it db sqlplus sys/l81qimtT6uM=1@ORCLPDB1 as sysdba
# or, use SQLDeveloper
```
```
docker run --rm --name pentaho \
    -v $PWD:/usr/src \
    -p 8080:8080 \
    -ti pentaho
```
