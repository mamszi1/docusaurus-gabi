---
id: api-integration-guide
title: My API Integration
sidebar_label: My API Integration
sidebar_position: 3
description: Learn how to seamlessly connect your application with our platform using our RESTful API.
---

# API Integration Guide

Welcome to the developer guide for integrating with the **Acme Platform API**.

Our API is built on RESTful principles. It returns JSON data, uses standard HTTP response codes, and requires bearer token authentication. This guide will walk you through the essentials of making your first request and handling data.

:::tip Prerequisite
Before getting started, ensure you have generated an **API Key** from your developer dashboard. Never share your keys in client-side code.
:::

## Authentication

All API requests must be authenticated by passing your API Key in the `Authorization` header.

The format is: `Authorization: Bearer YOUR_API_KEY`

## Base URL

All endpoints in this guide are relative to the following base URL for the production environment: