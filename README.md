# Highlights

## [Database Middleware and Setup](https://github.com/ChicoState/PantryNode/pull/57)

Researched database communication middleware, setup demo implementation, and, along with Brian Wells (who redesigned the database) worked on the initial database conversion code. My original idea was to work out a drop-in replacement for Mongoose, which meant finding a way to operate PostgreSQL as a NoSQL database. In simple terms, Sequlize would have allowed us to convert from Mongo to Postgres with little work to the existing code, but there was debate about the propriety of using Postgres in this way. In the end, the decision was made to rework the database rather than it keeping as-is. Sequelize was still used and turned out to be a helpful in communicating with the database. 

See also [issue #23: Migrate to PostgreSQL](https://github.com/ChicoState/PantryNode/issues/23) and [commit c036278ed82e115717d01811beb792979eb2ddb6](https://github.com/ChicoState/PantryNode/pull/57/commits/c036278ed82e115717d01811beb792979eb2ddb6)

## [Frontend to Backend Communication](https://github.com/ChicoState/PantryNode/tree/register_backend_connect)

In the last sprint, solved the backend to frontend communication issue (up to that point, the frontend had not been talking to the backend at all). Also, hooked up the registration form to the backend so new users were being created. Without the ability for the user inerface to communicate with the database, the UI would never truly function. And, if the sign-up form doesn't work, no one can use the app. 

See also [issue #120: Redirect issue on successful validation - Login Formik](https://github.com/ChicoState/PantryNode/issues/120).

# Timeline

## Sprint 1
* Researched a library to replace Mongoose (Sequelize). The idea was to find a near drop-in replacement - Sequelize is an ORM that would have mimicked the Mongoose/Mongo implementation. 
* Developed demo implementation ([Issue #23: Migrate to PostgreSQL](https://github.com/ChicoState/PantryNode/issues/23), [Pull Request #57: Merging migrate-to-postgres, updating #23](https://github.com/ChicoState/PantryNode/pull/57)).

## Sprint 2
* Committed code for /donor route to pull donor data from database ([issue #61: Migrate Routes from mongodb to PostgreSQL](https://github.com/ChicoState/PantryNode/issues/61)).

## Sprint 3
* Created [issue #141: Scaffold back-end interface file/route structure](https://github.com/ChicoState/PantryNode/issues/141)
* Opened [Pull request #148: Added structure and example for backend API](https://github.com/ChicoState/PantryNode/pull/148) which adds the structure for API-style interaction from frontend to backend.

## Sprint 4
* Reviewed [pull request #203: Removed outdated file structure](https://github.com/ChicoState/PantryNode/pull/203)
* [Pull request #148: Added structure and example for backend API](https://github.com/ChicoState/PantryNode/pull/148) approved and merged to into main. Issue #141 closed.

## Sprint 5
* Got frontend talking to backend and registration form properly creating new users in the database ([branch: register_backend_connect](https://github.com/ChicoState/PantryNode/tree/register_backend_connect)), related to [issue #120: Redirect issue on successful validation - Login Formik](https://github.com/ChicoState/PantryNode/issues/120).
