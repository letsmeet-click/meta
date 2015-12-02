# letsmeet.click - plan

## About

Platform to manage events.
Audience are usergroups that used G+, Meetup or Facebook Events before.

## Features

- Users
  - Login with G+, Facebook, Github
  - usernames like twitter/slack/...
  - profile pages per user: i.e. /u/mfa
- Groups
  - group home
  - different namespace than users: i.e. /g/stupig
  - two kinds of members (owners and normal members)
  - all members get invitations for new events
  - location with lat/lon
  - future: search with km radius
  - links to
    - twitter profile of group
    - github org
    - homepage
    - irc channel
    - slack org
    - ...
  - CNAME support? (howto?)
- Events
  - belongs to a Group
  - RSVP (going, not going) [no maybe]
  - discussions below. aka comments. moderated by owners.
  - allow RSVP of anonymous users
  - allow to hide participiants and only show count. (show all participiants only to owners)
- maybe / later
  - voting for date of next event (aka doodle)
  - mail to all members of group (only owners)
  - restapi for groups / events -- all read public? / or only for group-members/owners?
- technology
  - Django 1.8+
  - DRF (if api is a go)
  - allauth / social-auth ?
  - template based webpage with Django or api-based with angular? 
    - rw: No. Just Real Django.
