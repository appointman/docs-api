---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - ruby
  - python
  - javascript

toc_footers:
  - <a href='mailto:developer@appointman.net'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>

includes:
  - api
  - errors

search: true
---

# Introduction

The appointman API is a RESTful interface, providing programmatic access to basic data in the system. It provides predictable URLs for accessing resources, and uses built-in HTTP features to receive commands and return responses. This makes it easy to communicate with from a wide variety of environments, from command-line utilities to gadgets to the browser URL bar itself.

The API accepts JSON or form-encoded content in requests and returns JSON content in all of its responses, including errors. Only the UTF-8 character encoding is supported for both requests and responses.

_The API is still under development. Let us know in case something is missing for your use case.

Let's get started!

# Authentication

We require that applications designed to access the appointman API on behalf of multiple users implement OAuth 2.0.

## OAuth

Most of the time, OAuth is the preferred method of authentication for developers, users, and appointman as a platform. If you’re new to OAuth, take a moment to learn about it here. It’s not as scary as you might think!

In addition to learning about how to use OAuth on the appointman platform here, feel free to take a look at the official <a href="https://tools.ietf.org/html/draft-ietf-oauth-v2-31" target="_blank">OAuth spec</a>!

At its core, OAuth is a mechanism for applications to access the appointman API on behalf of a user without the application having access to the username and password. Instead, apps get a token which they can use with their own application credentials to make API calls.

## What is OAuth?

If you’re using a library to handle this or already understand OAuth and have <a href="#">registered an OAuth application</a>, you may want to skip ahead to the <a href="#">quick reference</a>.

If you have not already, you will need to <a href="#">register an application</a>. Take note of the client ID, an application’s username, and the client secret, an application’s password (protect it like one)!

1) A user will arrive at your application and click a button that says "Connect with appointman".

2) This takes the customer to the User Authorization Endpoint, which displays a page asking the user if they would like to grant access to your third-party application.

3) If the customer clicks "Allow", they are redirected back to the application, bringing along a special code as a query parameter. (We are assuming the <a href="#">Authorization Code Grant flow</a>, which is the most common.)

4) The application can now use the Token Exchange Endpoint to exchange the code, together with the Client Secret, for a Bearer Token (which lasts an hour) and a Refresh Token (which can be used to fetch new Bearer Tokens when the current one expires).

5) The application can make requests of the API using this Bearer Token for the next hour.

6) Once the Bearer Token expires, the application can again use the Token Exchange Endpoint to exchange the Refresh Token for a new Bearer Token. (This can be repeated for as long as the user has authorized the application.)

This is just one example using the Authorization Code Grant - applications that run entirely in the browser would generally use the Implicit Grant flow instead.

We definitely recommend using a library to take care of the nitty-gritty of OAuth, but hopefully this helps demystify the process somewhat.

## Register an Application

You must first register your application with appointman to receive a client ID and client secret. This is a manual process, currently.
Write an email to <a href="mailto:api@appointman.net">api@appointman.net</a> and just give us a short description what you are planning to do.

After an internal review you will receive a Client ID, needed to uniquely identify your app to the appointman API, as well as a Client Secret.

_Note: Your Client Secret is a secret, it should never be shared with anyone or checked into source code that others could gain access to._

## Quick Reference

TBD

https://asana.com/developers/documentation/getting-started/auth?missingtranslation=de#authorization-code-grant