## Covid Postman Collection <!-- omit in toc -->

This repository just aims to provide ready-to-import Postman Collection and some examples of use to play with data coming from repository [https://github.com/NovelCOVID/API/](https://github.com/NovelCOVID/API/)

- [Examples](#examples)
  - [CURL](#curl)
  - [Javascript](#javascript)
  - [Python](#python)

### Examples

Some example over API of the Postman API.

#### CURL

|  GET Request  | Output  |
| ------------ | ------------ |
| `curl --location --request GET 'https://corona.lmao.ninja/all'` | Returns all total cases, recovery, and deaths. |
| `curl --location --request GET 'https://corona.lmao.ninja/countries'` | Returns data of all countries that has COVID-19 |
| `curl --location --request GET 'https://corona.lmao.ninja/countries?sort=country'` | Returns data of each country sorted by the parameter |
| `curl --location --request GET 'https://corona.lmao.ninja/countries/ITALY'` | Returns data of a specific country. If an exact name match is desired pass ?strict=true in the query string |
| `curl --location --request GET 'https://corona.lmao.ninja/states'` | Returns all United States of America and their Corona data |
| `curl --location --request GET 'https://corona.lmao.ninja/v2/historical'` | Get historical data from the start of 2020. (JHU CSSE GISand Data) |
| `curl --location --request GET 'https://corona.lmao.ninja/v2/historical/ITALY'` | Get historical data from the start of 2020 for a specific country. (JHU CSSE GISand Data) |
| `curl --location --request GET 'https://corona.lmao.ninja/v2/jhucsse'` | Return data from the Johns Hopkins CSSE Data Repository (Country, province, confirmed, death, recovered) |

#### Javascript

Returns all total cases, recovery, and deaths.

```
var request = require('request');
var options = {
  'method': 'GET',
  'url': 'https://corona.lmao.ninja/all',
  'headers': {
  }
};
request(options, function (error, response) { 
  if (error) throw new Error(error);
  console.log(response.body);
});
```

Returns data of all countries that has COVID-19.

```
var request = require('request');
var options = {
  'method': 'GET',
  'url': 'https://corona.lmao.ninja/countries',
  'headers': {
  }
};
request(options, function (error, response) { 
  if (error) throw new Error(error);
  console.log(response.body);
});
```

Returns data of each country sorted by the parameter.

```
var request = require('request');
var options = {
  'method': 'GET',
  'url': 'https://corona.lmao.ninja/countries?sort=country',
  'headers': {
  }
};
request(options, function (error, response) { 
  if (error) throw new Error(error);
  console.log(response.body);
});
```

Returns data of a specific country. If an exact name match is desired pass ?strict=true in the query string.

```
var request = require('request');
var options = {
  'method': 'GET',
  'url': 'https://corona.lmao.ninja/countries/ITALY',
  'headers': {
  }
};
request(options, function (error, response) { 
  if (error) throw new Error(error);
  console.log(response.body);
});
```

Returns all United States of America and their Corona data.

```
var request = require('request');
var options = {
  'method': 'GET',
  'url': 'https://corona.lmao.ninja/states',
  'headers': {
  }
};
request(options, function (error, response) { 
  if (error) throw new Error(error);
  console.log(response.body);
});
```

Get historical data from the start of 2020. (JHU CSSE GISand Data).

```
var request = require('request');
var options = {
  'method': 'GET',
  'url': 'https://corona.lmao.ninja/v2/jhucsse',
  'headers': {
  }
};
request(options, function (error, response) { 
  if (error) throw new Error(error);
  console.log(response.body);
});
```

Get historical data from the start of 2020 for a specific country. (JHU CSSE GISand Data).

```
var request = require('request');
var options = {
  'method': 'GET',
  'url': 'https://corona.lmao.ninja/v2/historical',
  'headers': {
  }
};
request(options, function (error, response) { 
  if (error) throw new Error(error);
  console.log(response.body);
});
```

Return data from the Johns Hopkins CSSE Data Repository (Country, province, confirmed, death, recovered).

```
var request = require('request');
var options = {
  'method': 'GET',
  'url': 'https://corona.lmao.ninja/v2/historical/ITALY',
  'headers': {
  }
};
request(options, function (error, response) { 
  if (error) throw new Error(error);
  console.log(response.body);
});
```

#### Python

Returns all total cases, recovery, and deaths.

```
import requests

url = "https://corona.lmao.ninja/all"

payload = {}
headers= {}

response = requests.request("GET", url, headers=headers, data = payload)

print(response.text.encode('utf8'))
```

Returns data of all countries that has COVID-19.

```
import requests

url = "https://corona.lmao.ninja/countries"

payload = {}
headers= {}

response = requests.request("GET", url, headers=headers, data = payload)

print(response.text.encode('utf8'))
```

Returns data of each country sorted by the parameter.

```
import requests

url = "https://corona.lmao.ninja/countries?sort=country"

payload = {}
headers= {}

response = requests.request("GET", url, headers=headers, data = payload)

print(response.text.encode('utf8'))
```

Returns data of a specific country. If an exact name match is desired pass ?strict=true in the query string.

```
import requests

url = "https://corona.lmao.ninja/countries/ITALY"

payload = {}
headers= {}

response = requests.request("GET", url, headers=headers, data = payload)

print(response.text.encode('utf8'))
```

Returns all United States of America and their Corona data.

```
import requests

url = "https://corona.lmao.ninja/states"

payload = {}
headers= {}

response = requests.request("GET", url, headers=headers, data = payload)

print(response.text.encode('utf8'))
```

Get historical data from the start of 2020. (JHU CSSE GISand Data).

```
import requests

url = "https://corona.lmao.ninja/v2/jhucsse"

payload = {}
headers= {}

response = requests.request("GET", url, headers=headers, data = payload)

print(response.text.encode('utf8'))
```

Get historical data from the start of 2020 for a specific country. (JHU CSSE GISand Data).

```
import requests

url = "https://corona.lmao.ninja/v2/historical"

payload = {}
headers= {}

response = requests.request("GET", url, headers=headers, data = payload)

print(response.text.encode('utf8'))
```

Return data from the Johns Hopkins CSSE Data Repository (Country, province, confirmed, death, recovered).

```
import requests

url = "https://corona.lmao.ninja/v2/historical/ITALY"

payload = {}
headers= {}

response = requests.request("GET", url, headers=headers, data = payload)

print(response.text.encode('utf8'))
```