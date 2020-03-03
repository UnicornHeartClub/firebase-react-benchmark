# Firebase Realtime Database Benchmark

The purpose of this repository is to examine the performance impact of using
[Firebase Realtime Database](https://firebase.google.com/docs/database/)
listeners in an application built using [React](https://reactjs.org).

## Results

_Work in progress_

## How It Works

This benchmark seeks to answer the following questions:

 - How much CPU is being consumed by listeners?
 - How much memory is being consumed listeners?
 - What is the measured rendering time for child_added events?
 - What is the measured rendering time for child_removed events?
 - What is the measured rendering time for child_changed events?
 - What is the measured rendering time for value events?

A simple React application is used to initialize listeners and measure the
  performance impact for different events. A second script (outside the web
  application) is used to simulate random event changes to the database.

The application independently measures the performance impact of using 1, 10,
100, 1000, and 10000 listeners across data sets that range from 1kb-256kb. The
performance cost of using small datasets vs large datasets is also
independently measured.

## Running Benchmark

This repository contains two main scripts:

- `start` - Starts the web application where benchmarks are measured and displayed
- `simulate` - Simulate random data updates to a series of data

Start the web application and follow the instructions on the screen to sample
performance data.

## License

MIT
