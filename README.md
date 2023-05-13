# Planka Helm Chart

Shoutout to [this issue](https://github.com/plankanban/planka/issues/192)

## Issues

By using the Bitnami chart for PostgreSQL, there is an issue where once deployed, if trying to change the password then it will be ignored as the PVC will already exist with the previous password. I have some ideas for a workaround, I just haven't implemented them yet. See warning from Bitnami below:

> **Warning!** Setting a password will be ignored on new installation in case when previous Posgresql release was deleted through the helm command. In that case, old PVC will have an old password, and setting it through helm won't take effect. Deleting persistent volumes (PVs) will solve the issue. Refer to [issue 2061](https://github.com/bitnami/charts/issues/2061) for more details

