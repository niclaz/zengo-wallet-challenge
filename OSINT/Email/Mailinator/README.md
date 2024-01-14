# OSINT content extracted from the mailinator.com public inbox for the challenge

Zengo today released the email associated with the Challenge in [a video on Twitter](https://twitter.com/ZenGo/status/1746555618171797869)

zengowalletchallenge@mailinator.com

In [a different video tutorial](https://twitter.com/ZenGo/status/1746555621325848744) for how to recovery an account with Zengo they described mailinator and showed the process

Mailinator offers Public Inboxes: https://www.mailinator.com/v4/public/inboxes.jsp

Zengo is using it for everyone to have access to the emails sent as part of the account recovery

This is the search link for the inbox: https://www.mailinator.com/v4/public/inboxes.jsp?to=zengowalletchallenge

## Email analysis 

In this section of the repository you will find files and dumps from the email analysis

### Mailinator

#### 'tap to confirm' button (example)

this is the link in the button:

> https://www.mailinator.com/linker?linkid=e4e72e04-1c46-4101-90de-532e4344c687

The 'clean link' of the above:

> https://go.redirectingat.com/?id=19823X771710&xs=1&sref=mailinator.com&url=https%3A%2F%2Fapp.zengo.com%2Fmagiclink%2F%3FuserAuthenticationCode%3Dc93fe665-6d8c-42f0-ba48-de4bf61981e5

once clicked the above leads to the following:

> https://app.zengo.com/magiclink/?userAuthenticationCode=c93fe665-6d8c-42f0-ba48-de4bf61981e5

The 'userAuthenticationCode' carries over from go.rediretingat.com to zengo.com

After looking through 5 of the same type of signup email it is obvious the userAutenticationCode changes with each request, following the **magiclink passwordless standard**


## Important data to consider for future

+ Request flow: redirectingat.com > app.zengo.com > magiclink > something happens in app
+ OSINT of redirectingat.com - now managed by skimlinks.com - which is owned by taboola.com (Ad / Affiliate marketing)
+ redirectingat uses an 'id' is '19823X771710'
+ zengo magiclink includes a 'userAuthenticationCode' which changes with each request
  + Consider attack surface in email request sent from redirectingat.com to zengo.com > injection ? 
+ subdomains of interest for OSINT
  + app.zengo.com
  + app.zengo.com/f/
  + app.zengo.com/f/a/ 
  
