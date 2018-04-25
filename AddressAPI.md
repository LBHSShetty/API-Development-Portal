---
layout: swagger
title: Address API
data: AddressAPI
---

Address API which covers all our address searches for Local and National property address.


**Scope of the API**

This API provides a limited interface to the Local Land and Property Gazetteer (LLPG) and the National Land and Property Gazetteer (NLPG). Its main purpose is to facilitate address searching. It allows for retrieval of resources, not creation or updating.

**A single API for local and national addresses**

We currently have a web service with a local gazetteer endpoint and a national gazetteer endpoint. There are two more web services which use these endpoints to offer a combined service, the default behaviour of which searches the LLPG first, and if nothing is returned then the NLPG is searched.

The API will replace the LLPG endpoint, the NLPG endpoint, and the combined LLPG/NLPG web services using them. It will offer the LLPG by default.

There is an optional parameter called gazetteer, which can be used to override the default behaviour. This parameter specifies if the returned addresses should be from the Hackney gazetteer (LLPG), the national gazetteer (NLPG), or combined, as detailed above.

Every returned address has a gazetteer property showing which gazetteer it was extracted from.

To ensure the API returns up to date results for local addresses, it will not return Hackney addresses from the national gazetteer.
