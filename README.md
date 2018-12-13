# FileMakerPoCMFA
Proof of Concept for [MFA](https://en.wikipedia.org/wiki/Multi-factor_authentication) in a Filemaker solution.

This file is here for discussion, this file may or may not contain a valid concept for MFA in FileMaker.

1. Username is separate from email address; as the email address is the mode of transport for the FA 1
2. Password is only communicated to email by the system, no users have to see this; will have to remove the password convenience field to achieve this.
3. Login to FileMaker is still 1FA, but then again Filemaker is 1 factor and does not have the potential of becoming an MFA on its own. FileMaker is 1 factor. The primary purpose of 2FA is to not disclose username and password in the same channel.
4. User accounts are deactivated 24 hrs after initial login as pr this example; this could be 4 or 10 weeks depending on [SOP](https://en.wikipedia.org/wiki/Standard_operating_procedure)


```
1.0 Ways to generate account
  1.1 Let admin create the entry
  1.2 Send a request to generate account for username and mailaddress via:
      email, SMS, CWP, DATA API do NOT mention the username in this piece of communication.
```

```
2.0 Ways to communicate password
  2.1 Issue SMS or email preferably my a mode of transport not used
      to generating the account as that would lower the factor. 
```


# Hypothesis
It's possible to build 2FA login procedure with FileMaker and an external mode of transport for this PoC; however it will be desirable to verify the MFA throughout the login process; to do so will take 2 steps in amendment of FileMaker. And for FMI to implement
```
1) A [x] checkbox for making login script uninterruptable
2) Give each account an expiry field that will automatically delete or disable the account
   at a given point in time, as pr timestamp as an example. To avoid wasting resource the best trigger for
   this validation may be: each login attempt.
```

# Conclusion
No single application can truly be MFA; as it's 1FA no matter how one turns the "rubik's cube"; time can add a factor however.
