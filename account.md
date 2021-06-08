# How to manage user accounts for an online tool?

## Requirements

* Users should be able to evaluate the tool easily without having an account
* User accounts are needed to save user specific data and to bill the user
* Implementing password storage and recovery and second factor authentication etc. are uninteresting and probably labour some work for the developer so it should be minimized or eliminated.

## Solution

* All functionality is provided without an account but any data can not be saved without it.
* Federated identity over Google and Facebook etc. is provided at first and local user accounts are implemented only when there is enough demand for it.
* With federation the user may not have to log in at all when using the tool if he is already logged in for Gmail for example.
