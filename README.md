# Expo Constants.deviceId undefined in Background Tasks

This repository demonstrates a bug where `Constants.deviceId` from Expo returns `undefined` when accessed within a background task.  This issue can disrupt functionality reliant on unique user identification or data synchronization.

The `bug.js` file showcases the problem: attempting to retrieve `Constants.deviceId` while the app is in the background yields `undefined`, while the same code in the foreground works as expected.

The `bugSolution.js` file provides a workaround to mitigate this issue by using asynchronous storage to persist the `deviceId` and retrieve it even in background tasks.