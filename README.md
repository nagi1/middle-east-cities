# Middle east cities

Database of cities regions and details for some middle east countries.

## Features

- Current available cities **(Egypt, Saudi Arabia, UAE, Kuwait)**
- Only include cities with population **over than 5000**.
- Cities Ordered by population in descending order (crowned cities first)
- Available in arabic and english.
- json format (currently).
- City details include regions and Geolocation information.
- Unique Id for every city.

## City counts

- **Egypt:** 239
- **Saudi Arabia**: 96
- **UAE**: 35
- **Kuwait**: 25

## Usage

Json files named in form of country code and language code

   `example: eg_ar => Egypt Cities in arabic language`

## Example

Get cities grouped by region

```js
const fs = require('fs');
const groupby = require('lodash/groupby');

const input = './json/eg_ar.json';

fs.readFile(input, (err, data) => {
	const cities = JSON.parse(data).cities;
	console.log(
		groupby(cities, (obj) => {
			return obj.region;
		}),
	);
});
```

## See also

[awesome-cities](https://github.com/nagi1/awesome-cities)

## Todo

- [ ] Add some missing key cities in egypt

- [ ] Covert to .sql (MySQL)

- [ ] Add more usage example


## References

Geodb-cities
