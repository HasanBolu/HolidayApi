# HolidayApi
Rpc api fetchs all public holiday of countries below using https://github.com/martinjw/Holiday project. 
The Holiday project added as a git sub module and You should run following two commands to get Holiday project files after cloned this repository

```git
git submodule init 
git submodule update
```
- Europe
  - Austria 
  - Belgium 
  - Czech Republic 
  - ECB 
  - France 
  - Germany 
  - Ireland 
  - Italy 
  - Luxembourg 
  - Netherlands 
  - Norway 
  - Poland 
  - Slovakia 
  - Spain 
  - Sweden 
  - Switzerland
  - UK
- E. Europe/Asia
  - Kazakhstan
- N America
  - Canada 
  - USA
- Oceania
  - Australia 
  - New Zealand
- Asia
  - Japan

# Running via Docker

## Building docker image
```
docker build -t holidayapi .
```
## Running via docker-compose
After you built docker image, you can run the docker-compose command below to start holidayapi service
```
docker-compose -f docker-compose.yml up
```
You can change the port in docker-compose.yml to host it on different port of localhost

# Example Request
then you will be able to request the http://localhost:5000/holiday url with the following example body 

```json
{
    "id":1,
    "jsonrpc":"2.0",
    "method": "PublicHolidays",
    "params":{
	"start" : 2019,
	"end" : 2020
    }
}
```


