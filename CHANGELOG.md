<!-- markdownlint-disable MD001 MD004 MD012 MD024 -->

# Changelog

## [1.4.0] (2026-03-05)

## Overview

Version 1.4.0 introduces significant enhancements to the React-Native SDK, expanding its capabilities for implementing Dynamic Yield in native applications through API Campaigns.  
The React-Native SDK provides a comprehensive interface to the Experience API, covering all major implementation areas, including:

*   Tracking pageviews
*   Assigning targeted experiences
*   Tracking clicks and custom events
*   Retrieving semantic search campaigns
*   Retrieving visual search campaigns
*   Retrieving Shopping Muse (assistant) campaigns

***

## 🌟 New Features

### **1. Full Support for Semantic Search**

The SDK now fully supports Semantic Search campaigns, enabling AI‑driven search interactions and smarter, context‑aware results.

### **2. Full Support for Visual Search**

Visual Search is now fully integrated, allowing apps to submit images and seamlessly present AI‑generated visual‑based product results.

### **3. Full Support for the Assistant API (Shopping Muse)**

The release introduces full compatibility with the Shopping Muse assistant API, enabling conversational shopping experiences powered by dynamic, personalized guidance.

### **4. Full Support for Rollout (Feature Flags)**

This version adds support for **Rollout** campaigns, enabling controlled, gradual feature releases. The SDK returns a `rolloutFlag` indicating whether a user should receive a new feature, allowing safe experimentation and instant changes without redeploying.

*   `true` → user should see the feature
*   `false` → user is in the control group
*   no flag → user not included in the rollout