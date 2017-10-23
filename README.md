# Testing Google Geocoding API

The aim of this application is check the parameters used by the Geocoding API service, as well as the response of it.

Google Maps Geocoding API is a service that provides geocoding and reverse geocoding of addresses.

### Areas
The two main areas are:
 - Geocoding is the process of converting addresses (like a street address) into geographic coordinates (like latitude and longitude).
 - Reverse geocoding is the process of converting geographic coordinates into a human-readable address.

See more information about the service [here](https://developers.google.com/maps/documentation/geocoding/start)



### Test coverage
- Geocoding
  - Test mandatory parameters as address or components
  -  Test optional parametes
  - Test invalid parameters

- Reverse geocoding
  - Test mandatory parameters
  - Test invalid parameters

### Installation

It's necessary to have installed the `bundler` gem. info [here](https://github.com/bundler/bundler)

In root folder, install all gems

```sh
  bundle install
```

### How to use it

##### parameters
- **key**: Google API key. It is possible to define a default key in the `env.rb` file, and not pass it as a parameter. 

Find more information about the Google API key [here](https://developers.google.com/maps/documentation/geocoding/start#get-a-key)

- **parallel**: num of threads for the parallel execution. If it's not defined, the default value is 10

##### Execute all tests without parallel execution
```bash
  bundle exec rake all_tests key=enter_valid_key
```

##### Execute all tests in parallel
```sh
  bundle exec rake parallel_all_tests key=enter_valid_key parallel=num_parallel
```

### Report
The report of the last execution is automatically saved in `features/reports.html`
