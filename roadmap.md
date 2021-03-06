# Roadmap

This document contains planned features. It is not sorted by priority, releavance or anything else.
Things will be done when somebody implements them. If you have a feature request that is not already
on the roadmap file an issue [here](https://github.com/letsmeet-click/letsmeet.click/issues)


## WP - testing

- [✓] add pytest setup
- [✓] setup wercker
- setup travis

## [✓] WP - notifications / slack integration

- [✓] on push -> slack
- [✓] on deploy -> slack (in update.sh on server)
- [✓] test results from wercker -> slack

## [✓] WP - bootstrap

- [✓] add bootstrap 3
- [✓] for the start, no compressor/..., but link to hosted bootstrap (maxcdn)
- [✓] do not check in downloaded files like bootstrap css, etc

## WP - oauth

- [✓] add python-social-auth
- option to change username
- option to set password
- register oauth with
  - [✓] github
  - [✓] twitter
  - google
  - [✓] facebook
- [✓] add login page
- [✓] add login status to navbar
- [✓] link / unlink social accounts

## [✓] WP - postgis

- [✓] use postgis in postgres docker container
- [✓] https://hub.docker.com/r/mdillon/postgis/
- [✓] write instructions for (dev) setup / change docker-compose.yml

## [✓] WP - communities

- [✓] create app: communities
  - [✓] add/ [X] modify community
  - [✓] subscribe (membership in community) in m2m table
  - [✓] creator is (default) owner - owner is subscribed with additional info in m2m through model (choice, not bool)
  - [✓] view to community using /c/<slug> (don't forget the slug-field for name!)
  - [✓] no delete option for communities! (until later)

## [✓] WP - locations
https://github.com/letsmeet-click/letsmeet.click/issues/27
- create app: locations
  - [✓] locations can have special requirements (notes textfield)
  - add fields for meta information:
    - [✓] name
    - [✓] link to location
    - [✓] lat/lon using geo-fields (for km calculations later)
    - [✓] slug field for usage as url later. generated using the name of the location.

## [✓] WP - events

- [✓] create app: events
  - [✓] m2m to users with through. coming/not-coming
  - [✓] fk to community

## [✓] WP - hosting on ovh-vpc

- [✓] setup dev.letsmeet.click
- [✓] setup docker containers on server
- [✓] add update.sh for deployment
- [✓] add letsencrypt / ssl

## [✓] WP - nginx

- [✓] CNAME support

## [✓] WP - communities 2

- [✓] every subscriber can be promoted to owner by original owner
- [✓] community has links to
  - [✓] twitter profile of group
  - [✓] github org
  - [✓] homepage
  - [✓] irc channel
  - [✓] slack org
  - [✓] only one per type possible
  - [✓] enhance community view with
    - [✓] event list
    - [✓] owners
    - [✓] subscribers
    - [✓] links (see above)
- [✓] validator for CNAME field (no /, no http[s] at the beginning)

## [@asmaps] WP - users 2
 https://github.com/letsmeet-click/letsmeet.click/issues/21 
- profile page
  - [✓] my profile
  - /u/<username>
  - option to add bio
  - option to add profile picture
  - show list of communities the user is member
  - show list of events the user is going / was going
  - option to optout of being listed for events/communities (later by community/event ?)

## WP - locations 2
 https://github.com/letsmeet-click/letsmeet.click/issues/22
- osm integration
  - get locations from openstreetmap
  - i.e. http://nominatim.openstreetmap.org/search/?q=shackspace
  - evaluate other methods
  - add to community creation process
  - osm/leaflet map on location site
- landing page for locations:
  - /l/<slug>

## WP - events 2
https://github.com/letsmeet-click/letsmeet.click/issues/23
- rsvp of anonymous users? only count them? verify with email / token-link?
- allow to hide participiants and only show count. (show all participiants only to owners)
- comments on event
- table with comments, no threads (1 event = 1 thread)
- add social media share buttons

## WP - KPIs
https://github.com/letsmeet-click/letsmeet.click/issues/24
- summary page with KPIs
  - registered users by day
  - created communities by day
  - created events by day/community
  - rsvps by day/community
- only for staff but not as part of the admin.

## WP - FAQ/Help
https://github.com/letsmeet-click/letsmeet.click/issues/25
- add a general FAQ/Help page
- add instructions for CNAME support in communities

## WP - hosting 2

- [✓] opbeat
- [✓] dump postgresql
- [✓] backup to another server

## WP - mailing
https://github.com/letsmeet-click/letsmeet.click/issues/26

- mail to organizer on new community subscription
- mail to organizer on new event yes/no

- mail to every attendee one day before event
- mail to every local_organizer two days before event
- mail to every subscriber on event creation
- mail using i.e. https://www.mailgun.com/
