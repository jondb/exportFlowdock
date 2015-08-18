# FLOWDOCK

This script exports flowdock conversations to .html.

For example, get a list of users:

    ./export users

Gives you something like this:

    u'name': u'bob Woo', u'email': u'bob@org.com', u'nick': u'Bob', u'id': 122112}
    {u'name': u'Carly Barly', u'email': u'charly@org.com', u'nick': u'Charly', u'id': 93955}
    ...

To get the first 10 private conversations with bob, do this:
  
    ./export private 122112 bob.html 10

Open bob.html, and see this:

    2015-01-09 21:38:30Ram/Bob Woo:i like coffee8833252524
    2015-01-09 21:38:34Ram/Bob Woo:a lot8833252571

Bob likes coffee.

To get an entire flow, do this:

    ./export flows

And see this:

    CMD: flows
    {'url': u'https://api.flowdock.com/flows/org/harp', 'parameterized_name': u'harp', 'organization_parameterized_name': u'org'}
    {'url': u'https://api.flowdock.com/flows/org/main', 'parameterized_name': u'main', 'organization_parameterized_name': u'org'}

For the first 50 messages, do this

    ./export flow link link.html 50

Which puts the following into linke.html

    2015-01-12 06:21:10Barly/Barly charly:@Joe, Curt and I saw this bug - can we call down payment 2 words? 20
    2015-01-12 06:21:Joe/Joe Bryon:what bug? 26
    ...

Type ./export for usage.