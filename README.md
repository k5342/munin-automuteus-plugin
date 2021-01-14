# munin-automuteus-plugin
A logging plugin for [AutoMuteUs](https://github.com/denverquane/automuteus).

This is not intended to collect data from Prometheus endpoint (port 2112) including discord API call counts.

## Requirements
- Perl
- LWP
- JSON

## Installation
1. Clone this repository
1. Put `automuteus` file into /etc/munin/plugins/ directory
1. Set environment variables in /etc/munin/plugin-conf.d/munin-node as needed (see below)
1. Reload munin-node to complete installation

## Configuration
Set `GALACTUS_ENDPOINT` environment variable to point your AutoMuteUs (Galactus) instance. You can customize this based on your settings; `GALACTUS_HOST` and `GALACTUS_EXTERNAL_PORT` environment variables in [sample.env](https://github.com/denverquane/automuteus/blob/master/sample.env).
```ini
...
[automuteus]
env.GALACTUS_ENDPOINT http://192.168.1.2:8102/
...
```

## LICENSE
The MIT License (MIT) Copyright (c) 2021 k5342

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
