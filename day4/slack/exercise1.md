# Slack Exercise 1

Your Linux environment should have the following environment variable set:

SLACK_TOKEN

You can access this environment variable using the following code:

    import os
    os.environ["SLACK_TOKEN"]

That environment variable will contain the Slack token to use for authenticating
to the demo Slack Workspace.

1. Using the Python requests libary, retrieve the list of channels from the following URL:

```
url = "https://slack.com/api/channels.list"
```

As this endpoint requires authentication, you will need to pass the Slack token with your request. Gather the list of channels using each of the following methods:

    1. Setting the token in the HTTP header:

```
http_headers = {
    "authorization": token,
}
```

    2. Include the token encoded in the URL:

```
url = f"https://slack.com/api/channels.list?token={token}"
```

    3. Including the token in the payload (if there is a payload, it probably isn't a GET operation anymore!):

```
data = {"token": token}
```
