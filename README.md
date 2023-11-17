# Performance Profiler

The Performance Profiler module is a middleware designed to monitor and record HTTP request performance by measuring response times and logging relevant information. It is specifically crafted to assist developers in monitoring, recording, and optimizing HTTP request performances. It is especially useful when interacting with third-party APIs like Google Places API, where responses can be voluminous, complex, and potentially slow.

## Description

This module provides a real-time overview of your application's performance. It records the total time, average time, as well as detailed statistics for each route. The data is written into a log file with daily rotation and can be accessed through a specific route.

## Features

**Response Time Measurement**: Accurate tracking of response time for each request, allowing for the identification of the most time-consuming operations.
**Detailed Logging**: Records relevant metrics in rotating logs for continuous monitoring without bloating storage.
**Performance Analysis**: Automatically categorizes requests according to performance thresholds for quick diagnosis of weak points.

### Prerequisites

- Node.js (recommended version: 14.x or higher)
- An Express.js application

## Installation

Clone the repository of a Test project for the middleware and install the necessary dependencies.

```   bash ``` 
- git clone https://github.com/Fatysami/NodePulseProfiler.git
- cd your-project-name
- npm install perfo-profiler

## Usage

To use this module in your project, import it and use it as middleware in your Express.js application.

```javascript ``` 
const express = require('express');
const { performanceProfilerMiddleware } = require('perfo-profiler');

const app = express();

// Apply the middleware to all routes
app.use(performanceProfilerMiddleware);

// Define your routes as usual
app.get('/', (req, res) => {
  res.send('Hello World!');
});

// ...

app.listen(3000, () => {
  console.log('Server listening on port 3000');
});

## Contact
Fatima ezzahraa SAMI - fatimaezzahraa1983@gmail.com


