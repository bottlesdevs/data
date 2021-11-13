# Bottles' Data
This repository works as a extra repository for Bottles data.

## Contents
- Release backgrounds
- Concepts
- Notifications

## Publish notifications
Notifications are placed in `notifications.yml` file.

Example:
```yaml
2021-11-14 :
  id : 2
  type : info
  title : "2021.11.14 Release is out!"
  body : Upgrade to get latest features and bugfixes.
  url : https://usebottles.com/blog/release-2021.11.14/
  date : 2021-11-14
  recurrent : true
  before : "2021.11.14-treviso"
```

summary:
- `id`: unique identifier
- `type`: info, special, warning
- `title`: title of the notification
- `body`: body of the notification
- `url`: url of the notification
- `date`: date of when the notification is published
- `recurrent`: if the notification is recurrent (it will be displayed every first installation)
- `before`: the version of Bottles before this notification is published (e.g. in the above example, the notification will be displayed only for version before 2021.11.14-treviso)

Every New release update should overwrite the previous one but change the `id` field to a new one, to avoid Bottles from hide it.
