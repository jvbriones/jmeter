# jmeter
REST API using jMeter

## Instructions

1) Place the library "json-20160212.jar" in jMeter/lib folder. This library is used to work with Json objects.
2) Import the Testplan "random_apartments_generator.jmx" into Jmeter.

## Implementation Steps
- Retrieve via Http request a list of Countries from https://restcountries.eu/
  - With a Json extractor save the JSON response
- with BeanShell sampler, for each Capital obtained in the step before, generate a dataset of randomised apartments. 
  The Data generated is appended to the previous JSON data structure, keeping the apartments organized by city and avoiding duplications.
- with BeanShell sampler, retreive information from web services http://openweathermap.org/ and https://fixer.io. Update the information in
  the same JSON data structure for optimization and then generate 2 JSON arrays organized again by City and common elements, containing only "Recommended" or
  "Good Investment" Apartments


