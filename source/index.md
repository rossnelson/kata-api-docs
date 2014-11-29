---
title: Kata API Reference

language_tabs:
  - shell

toc_footers:
  - <a href='http://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the Kata API! You can use our API to access User and Organization API
endpoints, which can get information on various users, organizations and thier
access levels in our database.

We have Shell examples using curl. You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.

This API documentation page was created with [Slate](http://github.com/tripit/slate).

# Organizations

## Get All Organizations

```shell
curl -i \
  -H "Content-Type: application/json" \
  "http://kata.simian.us/orgs"
```

> The above command returns JSON structured like this:

```json
{
  "orgs":
  [
    {
      "id":2,
      "name":"Schumm-Bahringer",
      "created_at":"2014-11-29T03:02:41.734Z",
      "updated_at":"2014-11-29T03:02:41.734Z",
      "parent_id":null
    },
    {
      "id":3,
      "name":"Moen-Padberg",
      "created_at":"2014-11-29T03:02:41.735Z",
      "updated_at":"2014-11-29T03:02:41.735Z",
      "parent_id":2
    }
  ]
}
```

This endpoint retrieves all organizations.

### HTTP Request

`GET http://kata.simian.us/orgs`

# Users

## Get All Users

```shell
curl -i \
  -H "Content-Type: application/json" \
  "http://kata.simian.us/users"
```

> The above command returns JSON structured like this:

```json
{
  "users":
  [
    {
      "id":1,
      "email":"axcess1@me.com",
      "created_at":"2014-11-27T20:21:43.663Z",
      "updated_at":"2014-11-27T20:21:43.663Z"
    },
    {
      "id":2,
      "email":"camille.heel@vonrueden.info",
      "created_at":"2014-11-29T04:14:25.838Z",
      "updated_at":"2014-11-29T04:14:25.838Z"
    }

  ]
}
```

This endpoint retrieves all users.

### HTTP Request

`GET http://kata.simian.us/users`

## Get a Specific User

```shell
curl -i \
  -H "Content-Type: application/json" \
  "http://kata.simian.us/users/3"
```

> The above command returns JSON structured like this:

```json
{
"user": 
  {
    "id":1, 
    "email":"elwin.gerhold@leannonkling.name"
  }
}
```

This endpoint retrieves a specific user.

### HTTP Request

`GET http://kata.simian.us/users/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the user to retrieve

