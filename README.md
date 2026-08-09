# luci-theme-limcore

A clean, modern dark/light theme for OpenWrt LuCI.

Forked from [luci-theme](https://github.com/tickcount/luci-theme) by [tickcount](https://github.com/tickcount), which is itself based on [luci-theme-aurora](https://github.com/eamonxg/luci-theme-aurora) by eamonxg. This fork carries a reworked visual layer on top of their work.

## Preview

| Desktop | Tablet | Phone |
|---------|--------|-------|
| ![Desktop](preview/pc.png) | ![Tablet](preview/tablet.png) | ![Phone](preview/phone.png) |

https://github.com/user-attachments/assets/d3701be2-686f-48ec-b569-c7113755dba5

## Installation

OpenWrt 25.12+ and snapshots use `apk`; earlier versions use `opkg`.

**opkg** (OpenWrt < 25.12):

```sh
cd /tmp && uclient-fetch -O luci-theme-limcore.ipk \
  https://github.com/l-limon-l/luci-theme-limcore/releases/latest/download/luci-theme-limcore_1.0.0-r20260810_all.ipk \
  && opkg install luci-theme-limcore.ipk
```

**apk** (OpenWrt 25.12+):

```sh
cd /tmp && uclient-fetch -O luci-theme-limcore.apk \
  https://github.com/l-limon-l/luci-theme-limcore/releases/latest/download/luci-theme-limcore-1.0.0-r20260810.apk \
  && apk add --allow-untrusted luci-theme-limcore.apk
```

## Compatibility

- **OpenWrt** 23.05+
- **Chrome/Edge** 111+
- **Safari** 16.4+
- **Firefox** 128+

## Features

- Warm neutral palette with proper light/dark mode
- Three-column docs-style layout: sidebar, content, table of contents
- Frosted glass header with scroll-aware opacity
- Floating toast notifications
- Toggle-style boolean checkboxes
- Smooth page transitions via View Transitions API
- Redesigned login page
- Responsive — works on mobile

## Development

Built with **Vite 7**, **Tailwind CSS v4**, and **pnpm**. See [Development docs](.dev/docs/DEVELOPMENT.md).

## License

Apache License 2.0.

Credit where it is due: this theme is a fork of [luci-theme](https://github.com/tickcount/luci-theme) by [tickcount](https://github.com/tickcount), which in turn builds on [luci-theme-aurora](https://github.com/eamonxg/luci-theme-aurora) by eamonxg.
