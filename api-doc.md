## About API

This documentation explains the various endpoints that are exposed for zappier application integration.

## Production API Base URL

`https://dashboard.digital-agency.tech`

## Endpoints

- Authorize App (`/oauth/authorize`) (`GET`)
- Get Token (`/oauth/token`) (`POST`)
- Refresh Token (`/oauth/token`) (`POST`) 
- Get Profile (`/api/me`) (`GET`)
- Get Bookings (`/api/bookings`)(`GET`)
- Get Food Orders (`/api/food_orders`)(`GET`)
- Get Reviews (`/api/reputation_reviews`)(`GET`) 

## Basic Information

This api works on a OAuth 2.0 Protocol and requires user to authorize integration in order to generate successful bearer token.

## Authorize App

This would be the starting point of the application and requires user to be already logged in to work properly. Otherwise user will be sent back to the login back.

Fields Supported/Required

- client_id
- redirect_uri
- response_type
- scope
- state

## Get Token

To get token a user sends `POST` request to the `/oauth/token` route.

Fields Supported/Required

- grant_type
- client_id
- client_secret
- redirect_uri
- code 

## Refresh Token

To refresh an expired token a user sends `POST` request to the `/oauth/token` route.

Fields Supported/Required

- grant_type
- refresh_token
- client_id
- client_secret
- scope

## Get Profile

To get a user's profile a user sends `GET` request to the `/api/me` route. This is protected and requires a valid token to be sent in header.

## Get Bookings

To get a user's bookings a user sends `GET` request to the `/api/bookings` route. This is protected and requires a valid token to be sent in header.

## Get Food Orders

To get a user's food orders a user sends `GET` request to the `/api/food_orders` route. This is protected and requires a valid token to be sent in header.

## Get Reviews

To get a user's reviews a user sends `GET` request to the `/api/reputation_reviews` route. This is protected and requires a valid token to be sent in header.
