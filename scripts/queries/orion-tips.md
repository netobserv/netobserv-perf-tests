# Orion config tips

Below tips may help to generate different comparisons with Orion in certain
scenarios. For full orion documentaion refer
[orion repository.](https://github.com/cloud-bulldozer/orion/)


To exclude specific versions and restrict to specific version, say 4.22,
specified by version=4.22 env var:

```yaml
    metadata:
      wildcard:
        ocpVersion: "{{ version }}"
```

To match runs with specific operator build:

```yaml
  metadata:
      wildcard:
        release: "*d336d6e*"
```

If you're running rehearsals and only want to match runs in that PR:
```yaml
  metadata:
    pullNumber: 79326
```
