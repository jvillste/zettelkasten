# How should people authenticate in online services?

## Requirements

* The user should have different identity for each service
* It should be enought to remember only one password
* It should be easy to change the shared secret automatically for each service
* It should be hard to steal the identities by key loggers or other malware

## Solution

* A different Time-based One-time Password Algorithm (TOTP) secret key is held by each service and stored by the user into an encrypted file that the user can open by a password. 
* The file can be stored in the user's computer or to a cloud service
* The services provide an API that can be used to change the secret automatically
* A login happens by a software that decrypts the file and sends the one time password to the service that the user wants to authenticate.

## Pros

* The secrets are not sent through the wire during authentication
* Channging the secrets for all services can be a one click operation for the user

