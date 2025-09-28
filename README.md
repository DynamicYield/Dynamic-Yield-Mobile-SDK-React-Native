# Dynamic Yield React Native SDK

## Overview

The **Dynamic Yield React Native SDK**  provides a complete interface to our Experience API that covers all major implementation aspects, including tracking pageviews, assigning targeted experiences, and tracking clicks and events.

## Documentation & Resources

For detailed implementation guides, SDK references, and troubleshooting, refer to the following resources:

- [Implement Mobile SDKs on Your App](https://dy.dev/docs/implement-mobile-sdk)
- [React-Native SDK Documentation](https://dy.dev/docs/react-sdk)
- [Release Notes](https://github.com/DynamicYield/Dynamic-Yield-Mobile-SDK-React-Native/releases)

## Compatibility

This library supports **React Native version 0.77.0 and above**.

## Installation prerequisites

| OS    | Minimum Version | Minimum Build Environment         |
|-------|-----------------|----------------------------------|
| iOS   | 14              | swift-tools-version: 5.9          |

| OS      | MinSDK |
|---------|--------|
| Android | 24     | 

### Generate a personal access token for GitHub

In your GitHub account:

- If you don't have a user, register to Github.
- Go to Settings › Developer Settings › Personal Access Tokens › Generate new token
- Make sure you select the following scopes: (“read:packages") and Generate a token
- Make sure to copy your new personal access token. You won't be able to see it again! Your only option if it's lost is to generate a new key.

## Installing the React Native SDK

### Add authentication

First add a `.npmrc` file to your root project with your token:

```ini
@dynamicyield:registry=https://npm.pkg.github.com/
//npm.pkg.github.com/:_authToken=${GITHUB_TOKEN}
```

### Install Package

Then you can use the React Native SDK via npm:

```sh
npm install @dynamicyield/react-native-sdk@1.2.0
```
