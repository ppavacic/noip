# noip

> [!CAUTION]
> Noip2 has open security issue!
> Before using this image check https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=601229 and https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=653957.

Fixes your problem of having ever-changing IP address.

## Usage

### Standard usage

```bash
sudo docker run \
  --name noip \
  -d \
  -e NOIP_USERNAME=DDNS_USERNAME_FROM_DDNS_KEYS_SLASH_GRPUPS_PAGE \
  -e NOIP_PASSWORD=DDNS_KEY_FROM_DDNS_KEYS_SLASH_GRPUPS_PAGE \
  -e NOIP_HOSTNAMES=DDNS_HOSTNAMES_FROM_DDNS_KEYS_SLASH_GRPUPS_PAGE \ # usually all.ddnskey.com
  ppavacic/noip
```

### Secrets file usage

```bash
sudo docker run \
  --name noip \
  -d \
  -e NOIP_USERNAME_FILE=PATH_TO_FILE \
  -e NOIP_PASSWORD_FILE=PATH_TO_FILE \
  -e NOIP_HOSTNAMES_FILE=PATH_TO_FILE \
  ppavacic/noip
```

Useful in compose files.

## Example

### Standard example

```bash
sudo docker run \
  --name noip \
  -d \
  -e NOIP_USERNAME=hzk6tvm \
  -e NOIP_PASSWORD=coolpassIgot \
  -e NOIP_HOSTNAMES=all.ddnskey.com \
  ppavacic/noip
```

### Secrets file example

```bash
sudo docker run \
  --name noip \
  -d \
  -e NOIP_USERNAME_FILE=/run/secrets/noip_username \
  -e NOIP_PASSWORD_FILE=run/secrets/noip_password \
  -e NOIP_HOSTNAMES_FILE=run/secrets/noip_hostnames \
  ppavacic/noip
```

## Contribute

https://github.com/ppavacic/noip/
