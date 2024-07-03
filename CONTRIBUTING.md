# Contributing

Thank you for considering contributing to Netdata.

Maintaining a platform for monitoring everything imaginable requires a broad understanding of a plethora of technologies, systems, and applications. We rely on community contributions and user feedback to continue providing the best monitoring solution out there.

There are many ways to contribute, with varying requirements of skills, explained in detail in the following sections.
One good way to start is searching through [specific GitHub issues](https://github.com/netdata/netdata/issues?q=is%3Aissue+is%3Aopen+sort%3Aupdated-desc+label%3A%22help+wanted%22) we need help with. Some of them are also labeled as "good first issue".

## Give Netdata a GitHub star

GitHub Stars are more important that you may think. It helps us gain visibility as a project and attract awesome contributors. We thank each and every star gazer, since we consider them, in a sense, contributors. If you enjoy the project, please do consider giving as a 🌟.

## Join the Netdata Community

You can engage with the Netdata community through our repo's [Github Discussions](https://github.com/netdata/netdata/discussions), our [Discord server](https://discord.com/invite/2mEmfW735j) and our [Community Forum](https://community.netdata.cloud)!

### Contribute a new collector

The Netdata Agent has a modular approach to collecting data from data sources, meaning that we have a number of collector plugins that send data to the Netdata Agent. For each collector plugin, you can create a new module which collects data from a data source.

Before you  continue, take a look at our [documentation  about collectors](https://github.com/netdata/netdata/blob/master/src/collectors/README.md) and how they work. It will greatly help you if you have a good understanding of the general architecture, the different collectors that we have, how they are divided into different *plugins* and finally what it means that a collector is *internal* or *external*.

All of our collectors are located on our main repository, [netdata/netdata](https://github.com/netdata/netdata). To contribute a new collector (or improve an existing one):

- **For Go collectors:**
  - Follow the Guide we have released: [How to write a Netdata collector in Go](https://github.com/netdata/netdata/blob/master/src/go/plugin/go.d/docs/how-to-write-a-module.md).
- **For Python collectors:**
  - Follow the Guide we have released: [How to contribute a Python collector](https://github.com/netdata/netdata/blob/master/docs/developer-and-contributor-corner/python-collector.md).
- **For Shell/Bash**
  - Read the [charts.d](https://github.com/netdata/netdata/blob/master/src/collectors/charts.d.plugin/README.md) documentation.
- **For StatsD:**
  - If you are not familiar with StatD, we have written an [introduction](https://www.netdata.cloud/blog/introduction-to-statsd/) to the protocol.
  - Take a look at the [reference documentation](https://github.com/netdata/netdata/blob/master/src/collectors/statsd.plugin/README.md) for the StatsD plugin.

### Contribute a new alarm definition

Netdata has an opinionated approach to monitoring, enabling the user to quickly get up to speed and running, without having to spend any time in creating charts and alarms. As such, it comes with sane defaults that have been curated by both industry experts, our team, and everyday users.

There are 2 reasons why you may want to contribute to our alarms:

1. You want to improve the sane defaults by modifying an existing alarm or adding a new one
2. You want to contribute a new collector. Every new collector should come with some basic alarms out-of-the-box

To do both, you will need to create (or modify) alarm configuration files. Our [documentation](https://github.com/netdata/netdata/blob/master/src/health/REFERENCE.md) details the process. To develop and test the alarm, you will only need an active installation of the Netdata Agent, so the developer container described above is not required.

### Contribute a new alarm notification

The Netdata Agent supports a large variety of alarm notifications. In essence, the Netdata Agent uses the alarm definitions to understand whether it should fire an alarm notification and then proceeds by executing a script called `alarm-notify.sh`.

In order to modify existing ones or create new notification alarms you will need to code in `bash`.

To create a new alarm, we can look to:

- Already implemented alarms inside `alarm-notify.sh` and copy their structure
- Use the [custom endpoint](https://github.com/netdata/netdata/blob/master/src/health/notifications/custom/README.md) notification as boilerplate.
