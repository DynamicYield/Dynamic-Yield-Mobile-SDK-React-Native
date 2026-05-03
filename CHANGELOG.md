<!-- markdownlint-disable MD001 MD004 MD012 MD024 -->

# Changelog

## [1.5.0] (2026-05-03)

## Overview

Version 1.5.0 adds **Active Consent Handling** to the React Native SDK and enhances **Semantic Search** with **spellcheck support**. 
This release improves compliance control and delivers more forgiving search behavior for end users. 

***

## 🌟 New Features

### **1. Active Consent Handling**

The SDK now allows applications to explicitly control consent state during initialization and runtime. 

**Key behavior** 
- Consent is passed during SDK initialization 
- Consent can be updated during the same session using async APIs 
- Consent is **not stored** across app launches 
- When consent is denied, consented tracking is disabled while still allowing non‑personalized campaigns 

**Modes** 
- Active Consent enabled 
   → SDK respects the provided consent value 
- Active Consent disabled
   → SDK always behaves as if consent is granted 

### **2. Semantic Search — Spellcheck Support**

Semantic Search requests can now enable **spellcheck** on a per‑request basis. 

When enabled: 
- The original query is never modified 
- Corrected and normalized queries are returned in the response payload 
- Works with both .success and .warning result states 

**Response fields** 
- searchQuery 
- spellCheckedQuery 
- normalizedQuery 

## ⚠️ Important Notes 

- Consent must be re‑provided on every app launch 
- Runtime consent changes apply only to the current session 
- Spellcheck is opt‑in per Semantic Search request

***

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