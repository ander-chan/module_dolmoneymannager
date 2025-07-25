# Dolibarr Money Manager Module

This module provides a REST API for managing bank accounts in Dolibarr.

## Download

You can download the packaged module from the [releases page](https://github.com/ander-chan/module_dolmoneymannager/releases/tag/v1.0.0).

## Compatibility

This module has only been tested with Dolibarr version 17.

## API Endpoints

The API is exposed through the `class/api_moneymannager.class.php` file and provides the following endpoints:

### Bank Accounts

*   `GET /` : List all bank accounts.
*   `GET /{id}` : Get a specific bank account by its ID.
*   `POST /` : Create a new bank account.
*   `PUT /{id}` : Update a bank account.
*   `DELETE /{id}` : Delete a bank account.
*   `POST /transfer`: Create an internal wire transfer between two accounts.

### Account Lines

*   `GET /{id}/lines` : Get the lines of an account.
*   `POST /{id}/lines` : Add a line to an account.
*   `GET /{id}/lines/{line_id}/links`: Get the links for an account line.
*   `POST /{id}/lines/{line_id}/links`: Add a link to an account line.

### Payments

*   `POST /{id}/payments`: Create a new "payment various".
