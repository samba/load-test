# Load / Integration Tests

These tests simulate actual end user usage of the application. They are used to validate the overall functionality and can also be used to put simulated load on the system. The tests are written using [locust.io](http://locust.io)

### Parameters
* `[host]` - The hostname (and port if applicable) where the application is exposed. (Required)
* `[number of clients]` - The nuber of concurrent end users to simulate. (Optional: Default is 2)
* `[runtime for requests]` - The time to run requests before terminating. (Optional: Default is 300s)

## Running locally

### Requirements 
* locust `pip install locustio`

`./runLocust.sh -h [host] -c [number of clients] -t [runtime for requests]`


## Running in Docker Container
* Build `docker build -t load-test .`
* Run `docker run load-test -h [host] -c [number of clients] -t [runtime for requests]`
