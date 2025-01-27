# React Native Dimensions API Undefined on Android

This repository demonstrates a common issue encountered when using the `Dimensions` API in React Native on Android devices. The problem arises when attempting to access screen dimensions before they are fully loaded, resulting in undefined values for width and height.

## Problem Description

The `Dimensions.get('window')` method might return `undefined` if called too early in the component's lifecycle. This can lead to crashes or unpredictable rendering behavior.

## Solution

The solution involves using the `Dimensions` API's `addEventListener` method to listen for changes in screen dimensions.  This ensures that you always have the correct values, even on slower Android devices or when orientation changes. This prevents the issues caused by trying to use the dimensions before they are available. 