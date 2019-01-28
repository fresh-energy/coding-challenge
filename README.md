# Candidate coding challenge

We appreciate your interest in Fresh Energy, and we want to thank you for taking your time to carry out our coding challenge. All submissions will be reviewed carefully.

## The problem

At Fresh Energy, smart meter data is at the core of what we do. We want to see what you can do with it.

The challenge is to read from a stream of smart meter data, and display the meter's consumption in real time, on a web page. We will provide you with a single `.jar` file that produces the data stream. We want to see you use [React](https://reactjs.org/) on the frontend, and [Spring Boot](https://spring.io/projects/spring-boot) for the backend. When you're finished, your live graph should be a pleasure to behold. Here's a concept wireframe for how it may look:


INSERT GRAPH WIREFRAME HERE


## Data stream format

Our `.jar` will produce a stream of JSON messages in TCP packets. This stream will include data for several smart meters, including consumption data and status messages on the health of the smart meters.

A sample consumption message:

```json
{
  "meterId": "testMeter1",
  "timestamp": "1548687561760",
  "data": {
    "power": "1300W",
    "voltage": "230V",
    "frequency": "50.023Hz"
  }
}
```

A sample status message:

```json
{
  "meterId": "testMeter2",
  "timestamp": "1548687727341",
  "status": {
    "transmission_quality": "good",
    "internet_connectivity": "good",
    "system_uptime": "250 days",
    "messages_sent": "64739"
  }
}
```
