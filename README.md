# noip

Fixes your problem of having ever-changing IP address.
Uses noip-duc.

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
  -e NOIP_PASSWORD_FILE=/run/secrets/noip_password \
  -e NOIP_HOSTNAMES_FILE=/run/secrets/noip_hostnames \
  ppavacic/noip
```

Where `/run/secrets/` is a volume with secrets.

## Contribute

https://github.com/ppavacic/noip/
