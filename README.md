# Tekton scripts and examples

## GitHub authentication
See [this manifest](github-secret.yaml). To apply export environment variales `GITHUB_USER` and `GITHUB_PASSWORD` then run:

```bash
cat github-secret.yaml | envsubst | kubectl apply -f -
```

## Create service account
See [this manifest](serviceaccount.yaml). Not that the secret needs to be created first.

## Optional: Proxy settings
See [this manifest](proxy-presets.yaml) for the Tekton namespace and [this manifest](proxy-presets-ci.yaml) for the ci namespace. If `http_proxy` variables are present run:

```bash
cat proxy-presets.yaml | envsubst | kubectl apply -f -
cat proxy-presets-ci.yaml | envsubst | kubectl apply -f -
```