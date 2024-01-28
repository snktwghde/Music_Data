Examining the music store data on MSSQL and understanding the business by answering some simple questions. 

## For Practice on a docker container

# Make sure [docker](https://www.docker.com) and sqlcmd(https://learn.microsoft.com/en-us/sql/tools/sqlcmd/sqlcmd-utility?view=sql-server-ver16&tabs=go%2Clinux&pivots=cs1-powershell)

1. Pull the SQL server image:
```
sudo docker pull mcr.microsoft.com/mssql/server:2022-latest

```

2. Run it:
```
sudo docker run -e "ACCEPT_EULA=Y" -e "MSSQL_SA_PASSWORD=<YourStrong@Passw0rd>" \
   -p 1433:1433 --name sql1 --hostname sql1 \
   -d \
   mcr.microsoft.com/mssql/server:2022-latest
```
3. To view it use:

```
sudo docker ps -a

```
4. To connect on it use:

```
/opt/mssql-tools/bin/sqlcmd -S localhost -U SA -P "<YourStrong@Passw0rd>"

```
5. To quit type 'quit'
6. To stop the container type:

```
docker stop <id>

```
