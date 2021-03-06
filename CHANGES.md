CHANGES
=======

2.7 (2017-12-08)
----------------

- Fixed a bug in `RevocationRequestHandler`. When the `action` response
  parameter in a response from `/api/auth/revocation` is `OK`,
  Content-Type of the response returned from the revocation endpoint to
  the client application should be `application/javascript` instead of
  `application/json`.


2.6 (2017-11-20)
----------------

- Added `JaxRsUtils` class.


2.5 (2017-11-16)
----------------

- Updated the version of authlete-java-common to 2.11.

- Implemented new `AuthleteApi` methods added by authlete-java-common-2.11.


2.4 (2017-10-18)
----------------

- Updated the version of authlete-java-common to 2.10.

- Supported `Settings.setReadTimeout(int)` method.


2.3 (2017-10-13)
----------------

- Updated the version of authlete-java-common to 2.9.

- Implemented `AuthleteApi.getSettings()` method.


2.2 (2017-07-21)
----------------

- Updated the version of authlete-java-common to 2.7.

- Implemented `AuthleteApi.standardIntrospection(StandardIntrospectionRequest)` method.

- Added `BaseIntrospectionEndpoint` class and `IntrospectionRequestHandler` class.


2.1 (2017-07-10)
----------------

- Fixed bug where user authentication time was being treated as milliseconds instead of seconds.


2.0 (2017-03-18)
----------------

- Updated the version of authlete-java-common to 2.1.

- Implemented the following new methods of `AuthleteApi` interface.
    * `deleteClientAuthorization(long, String)`
    * `getClientAuthorizationList(ClientAuthorizationGetListRequest)`
    * `updateClientAuthorization(long, ClientAuthorizationUpdateRequest)`


1.8 (2017-02-17)
----------------

- Updated the version of authlete-java-common to 1.40.

- Implemented `deleteGrantedScopes(long, String)` method of `AuthleteApi`
  interface.


1.7 (2017-02-15)
----------------

- Modified `AuthleteApiImpl` to catch `IllegalStateException` which
  `Response.hasEntity()` may throw.


1.6 (2017-02-14)
----------------

- Updated the version of authlete-java-common to 1.39.

- Implemented `getGrantedScopes(long, String)` method of `AuthleteApi`
  interface.


1.5 (2017-02-03)
----------------

- Changed `application/json` to `application/json;UTF-8` in `callPostApi()`
  defined in `AuthleteApiImpl`.


1.4 (2016-07-30)
----------------

- Added `getScopes()` method to `AuthorizationDecisionHandlerSpi` and
  `AuthorizationRequestHandlerSpi` to provide a function to replace scopes.

- Updated `AuthleteApiImpl` for `AuthleteApi` version 1.34.


1.3 (2016-04-25)
----------------

- Added `getProperties()` method to `AuthorizationDecisionHandlerSpi`,
  `AuthorizationRequestHandlerSpi` and `TokenRequestHandlerSpi` to
  support the mechanism to associate extra properties with access tokens.

- Added `getProperties()` method, `setProperties(Property[])` method,
  and other setter methods to `AccessTokenInfo` class.


1.2 (2016-02-08)
----------------

- Added some `Base*Endpoint` classes.

- Added classes to validate an access token.

- Added utility classes to implement a userinfo endpoint.


1.1 (2016-02-06)
----------------

- Added utility classes to implement (a) a JWK Set endpoint,
  (b) a configuration endpoint, and (c) a revocation endpoint.

- Updated `AuthleteApiImpl` for `AuthleteApi` version 1.28.


1.0 (2016-01-11)
----------------

- The first release.
