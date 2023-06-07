# GeoIP

A splite tunnel solution for v2rey cliens like Clash-Meta and Clash-Premium.

### Update Interval

This update every day from lastes ip list.


### How to use in Clash-Meta and Clash-Premium

1) Add the rule provider like this:

```yaml
rule-providers:
  ...
  iran-ip-rules:
    type: http
    behavior: ipcidr
    url: https://raw.githubusercontent.com/MiSaturo/GeoIP/main/iran-ip-rules.yaml
    path: ./clash-iran-ip-roles.yaml
    interval: 86400
  ...
```

2) Use defined rule-provider as rul-set in your ruls:

```yaml
rules:
  ...
  - RULE-SET,iran-ip-rules,DIRECT
  ...
```
