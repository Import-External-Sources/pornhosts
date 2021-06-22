[![Codacy Badge](https://api.codacy.com/project/badge/Grade/84b46b76e27740bb9eb3770dc6b004a2)](https://app.codacy.com/gh/Import-External-Sources/pornhosts?utm_source=github.com&utm_medium=referral&utm_content=Import-External-Sources/pornhosts&utm_campaign=Badge_Grade_Dashboard)


# Update 11. October 2020
You should all be aware of this repository is to become replaced by
[Porn Records](https://mypdns.org/my-privacy-dns/porn-records).

Porn-Records is a mix of the previously records from Porn-hosts repo and the
[matrix](https://mypdns.org/my-privacy-dns/matrix)

This mean that records will slowly but steady be removed from this repo
as the new repo. To keep having all our records, please visit the
[Porn Records](https://mypdns.org/my-privacy-dns/porn-records) repo.

### hosts file Location
You can see the full matrix here
<https://archive.mypdns.org/w/dnshosts/#location-in-the-file-system>

### Unix based systems
macOS X, iOS, Android, Linux: `/etc/hosts`.

### DNS zones
If you are so lucky that you have updated your system to use a DNS resolver
rather than abusing your disk-IO with the `hosts` file, we also generate a few
zone files for Unbound, dnsmasq and regular RPZ supported resolvers.

*Note*: If you'll read more about why you should switch to a local DNS resolver,
Please read this [thread](https://github.com/StevenBlack/hosts/issues/1057) at
[@StevenBlacks](https://github.com/StevenBlack)
[hosts](https://github.com/StevenBlack/hosts) project

### RPZ
You'll find the RPZ formatted file in the [dns_zones/](dns_zones/) folder as
`pornhosts.mypdns.cloud.rpz`

The syntax used for is to provide a `NXDOMAIN` response

Ex.

```python
femjoynude.com		CNAME	.
*.femjoynude.com	CNAME	.
```

### Unbound
The Unbound formatted file is generated with the `always_nxdomain` syntax.

Ex.

```python
local-zone: "yspmedia.gitlab.io" always_nxdomain
```

The file is found under the [dns_zones/](dns_zones/) as
`pornhosts.mypdns.cloud.zone`

Any helpful [contributions](CONTRIBUTING.md) are appreciated
