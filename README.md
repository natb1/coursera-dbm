# coursera-dwbi
Materials for Coursera: Data Warehousing for Business Intelligence

### debug
```
docker run --rm --name db \
    -v $PWD/data:/opt/oracle/oradata \
    -v $PWD:/usr/src \
    -p 1521:1521 -p 5500:5500 \
    -ti oracle/database:12.2.0.1-ee

# password below changes whenever new data directory is mounted
docker exec -it db sqlplus sys/l81qimtT6uM=1@ORCLPDB1 as sysdba
```
