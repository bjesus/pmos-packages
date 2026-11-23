# pmos-packages

Signed [postmarketOS / Nura](https://nura.eco) package repositories for my
out-of-tree device ports, served by GitHub Pages. Packages are built by the
CI of each port's repository and pushed here.

| Device | Repository URL (for `/etc/apk/repositories` or `pmbootstrap config mirrors.pmaports_custom`) | Source |
|---|---|---|
| Huawei MediaPad M3 Lite 8 (`qcom-msm89x7` + `huawei-cpn-config`) | `https://bjesus.github.io/pmos-packages/huawei-cpn/` | https://github.com/bjesus/mediapad-m3-lite-8-linux |

All packages and indexes are signed with `bjesus-pmos.rsa.pub` (in this
repository's `keys/` directory). Install it to `/etc/apk/keys/` on the device,
or into pmbootstrap's `config_apk_keys/` when building images.

Layout: `<device>/edge/<arch>/APKINDEX.tar.gz` — i.e. a mirror root per
device that pmbootstrap can use directly as `mirrors.pmaports_custom`
(it appends `edge`), and `https://bjesus.github.io/pmos-packages/<device>/edge`
as an apk repository line on the device.
