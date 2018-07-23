# react-native-leak

This repo exists to reproduce an issue in React Native 0.56.0.

In short, downloading the following <1KiB file causes a memory leak: http://ashoat.com/rnleak.json

The file consists of an array of arrays. The inner arrays are all one element long, and contain an object with a single string key pointing to null.
