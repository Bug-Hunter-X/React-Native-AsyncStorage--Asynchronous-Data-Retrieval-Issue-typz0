# React Native AsyncStorage Asynchronous Data Retrieval Issue

This repository demonstrates a common error in React Native applications when using AsyncStorage to store and retrieve data. The problem occurs when trying to access data before it has been fully written to AsyncStorage.  This typically results in unexpected null values or stale data being returned.  The solution involves ensuring proper handling of asynchronous operations.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` or `yarn install` to install dependencies.
3. Run the app on an Android or iOS emulator/device.
4. Observe the console output, which will initially show null because data retrieval happens before storage is complete.

## Solution

The solution involves using `await` or `.then()` to ensure the data is stored before attempting to retrieve it.  The corrected code example is provided in `bugSolution.js`.