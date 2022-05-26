# GSD TODO list

This list covers the TODO list across the entire GSD project. This isn't
the right place for it right now, but it has to go somewhere.

Please tag yourself with @githubname if you want to take a piece of work.

There are three places to start when thinking about GSD

Policy
Data
Tools

## Policy

Policy mostly doesn't exist today. We need to write down a lot of what's
happening in the project as well as future goals. This TODO list should
probably exist there too. You can find the closest thing to a policy repo
here
https://github.com/cloudsecurityalliance/gsd-project-plans

It's very disorganized and needs organization.

GSD needs a logo

We have a lot of kernel IDs, we need to explain why this is

## Data

The database can be found here
https://github.com/cloudsecurityalliance/gsd-database

How the data is currently structured needs to be documented (for example we
mirror CVE data in a namespace).

The GSD format needs to be documented (see the tools to understand this
format, it only exists in code today)

The OSV format needs to be better documented as well as a plae we can start
to capture some of the missing pieces GSD needs.

We need a json schema file to validate the data (for example we should
validate all pull requests before they can be merged)

We need to better doument expectations around the data being captured. For
example some data is more informational than a vulnerability. We need to
explain that and have a way to tag it as such

There are lots of other vulnerabilty databases out there. We need to decide
what to do about them. Should we mirror them like we do with CVE? We mostly
did this with CVE because CVE cannot be easily updated, GSD can be.

We have a concept of an "overlay" that isn't documented in any useful way.
What should this do and how shoudl the data be handled

We have a concpet of a namespace. What does that mean? What should it mean?

## Tools

The tools repo can be found here
https://github.com/cloudsecurityalliance/gsd-tools

Please see the CONTRIBUTING and DEVELOP files. They both probably need some
clarity. If someone could try to stand up some of these tools and see what
instructions are missing.

The webform is EXTREMLY ugly. Please make it pretty.

The webform can only request simple IDs. It would be nice if there were
more "dropdown" type elements to avoid having to type everything in (like
vulnerability type for example)

The webform could probably stand an API to interact with GSD

The only way to update an ID today is via a github PR. We should have a
nice form to allow editing data.

The webform only captures URLs for references. We should be capturing other
types of references (git commit IDs for example)

The tools run via docker-compose today. We should build some helm charts
for this probably

The securitylist tool is how we mirror NVD and CVE data. There is ZERO
error checking in these scripts. It's also sort of hacked together. Some
cleanup and documentation are needed

The gsd-bot directory holds the bot. This bot looks are issues in github
and creates files in the database. It has minimal error checking.

The bot only outputs OSV data for kernel entries, it should output OSV
format for everything (this will probably require some webform changes
also)

The bot has a special kernel mode and a special kernel helper script. The
scripts are bad, not documented, and the process is a mystery to everyone
except Josh and Oliver

The bot has some tests, it needs more. A bunch of the tests probably fail

What even is the cloudflare-workers directory?

We have some codeql workflows. We could probably use more.

The tools README is very sad