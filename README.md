# coursera-dwbi
Materials for Coursera: Data Warehousing for Business Intelligence

### debug
```
docker run --rm --name db \
    -v $PWD/data:/opt/oracle/oradata \
    -v $PWD:/usr/src/app \
    -ti oracle/database:12.2.0.1-ee
# password below changes whenever new data directory is mounted
docker exec -it db sqlplus sys/bKBEX2gxl+4=1@ORCLPDB1 as sysdba
```
