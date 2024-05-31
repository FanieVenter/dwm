

# dwm - Dynamic Window Manager

[![Build Status](https://github.com/FanieVenter/dwm/workflows/CI/badge.svg)](https://github.com/FanieVenter/dwm/actions)
[![GitHub License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

`dwm` is an extremely fast, small, and dynamic window manager for X. This repository contains my customized build of `dwm`, featuring several patches and configurations tailored to improve productivity and aesthetics.

## Features

- **Dynamic Tiling**: Efficiently manage windows with dynamic tiling layouts.
- **Customizable**: Easily modify the source code to suit your preferences.
- **Minimalistic**: Lightweight and minimal resource usage.
- **Keyboard-driven**: Navigate and manage windows primarily through keyboard shortcuts.

### Enhanced with Metrics

Incorporating appropriate features from the `metrics` project, this repository includes:

- **Activity Metrics**: Display your GitHub activity, including commits, pull requests, and issues.
- **Community Metrics**: Show your community contributions, such as discussions and repositories starred.
- **Repository Metrics**: Highlight key statistics about your repositories, like stars, forks, and license usage.

## Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/FanieVenter/dwm.git
   cd dwm
   ```
2. Build and install `dwm`:
   ```sh
   sudo make clean install
   ```

## Configuration

Configuration is done by editing the `config.h` file and recompiling. Refer to the example configuration for details on setting up keybindings, layouts, and other preferences.

## Metrics Integration

To integrate GitHub metrics into your profile or repository, you can use the following features from `lowlighter/metrics`:

- **GitHub Activity**: Display recent contributions and activity, providing insight into your coding habits and project involvement.
- **Community Contributions**: Showcase your participation in the GitHub community, including issues, pull requests, and repository stars.
- **Repository Statistics**: Present detailed statistics for your repositories, including star counts, forks, and primary license information.

### Example Metrics Configuration

```yaml
name: Metrics
on:
  schedule: 
    - cron: '0 * * * *'
  workflow_dispatch:
jobs:
  github-metrics:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: GitHub Metrics
        uses: lowlighter/metrics@latest
        with:
          token: ${{ secrets.METRICS_TOKEN }}
          plugin_activity: yes
          plugin_repositories: yes
          plugin_community: yes
```

For detailed documentation and more configuration options, visit the [metrics repository](https://github.com/lowlighter/metrics).

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

This README provides a clear overview of your `dwm` repository while integrating appropriate features from the `metrics` project, enhancing its appeal and functionality [[❞]](https://github.com/lowlighter/metrics/releases) [[❞]](https://github.com/lowlighter/metrics/blob/master/README.md) [[❞]](https://dev.to/lowlighter/discover-your-github-ranking-with-metrics-insights-dpe) [[❞]](https://dev.to/lowlighter/embellish-your-github-readme-profile-with-20-metrics-pagespeed-stats-music-you-ve-listened-to-and-more-2kda).
