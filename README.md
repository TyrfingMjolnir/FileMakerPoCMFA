# FileMakerPoCMFA
Proof of Concept for [MFA](https://en.wikipedia.org/wiki/Multi-factor_authentication) in a Filemaker solution.

This file is here for discussion, this file may or may not contain a valid concept for MFA in FileMaker.

1) Username for now is an email address; this should be swopped out and generated on the request.
2) Password is only communicated to email by the system, no users have to see this; will have to remove the password convenience field to achieve 2FA.
3) Login to FileMaker is still 1FA, but then again Filemaker is 1 unit and does not have the potential of becoming an MFA on its own. FileMaker is 1 factor. The primary purpose of 2FA is to not disclose username and password in the same channel.
4) User accounts are deactivated 24 hrs after initial login as pr this example; this could be 4 or 10 weeks depending on [SOP](https://en.wikipedia.org/wiki/Standard_operating_procedure)
