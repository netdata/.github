<!--
title: "Contributing"
custom_edit_url: https://github.com/netdata/netdata/edit/master/CONTRIBUTING.md
sidebar_label: "Contributing handbook"
-->

# Contributing

Thank you for considering contributing to Netdata.

We love to receive contributions. Maintaining a platform for monitoring everything imaginable requires a broad understanding of a plethora of technologies, systems and applications. We rely on community contributions and user feedback to continue providing the best monitoring solution out there.

There are many ways to contribute, with varying requirements of skills, explained in detail in the following sections.
Specific GitHub issues we need help with can be seen [here](https://github.com/netdata/netdata/issues?q=is%3Aissue+is%3Aopen+sort%3Aupdated-desc+label%3A%22help+wanted%22). Some of them are also labeled as "good first issue".

# All Netdata Users

## Give Netdata a GitHub star

This is the minimum open-source users should contribute back to the projects they use. Github stars help the project gain visibility, stand out. So, if you use Netdata, consider pressing that button. **It really matters**.

## Join the Netdata Community

We have launched a [discussion board](https://community.netdata.cloud) where you can find many of us.

## Spread the word

Community growth allows the project to attract new talent willing to contribute. This talent is then developing new features and improves the project. These new features and improvements attract more users and so on. It is a feedback loop. 

 **The more people involved, the faster the project evolves**.

 We have a growing community at our [forums](https://community.netdata.cloud) which can help you spread the word. If you want to talk about Netdata in a local meetup, just create a topic in the "Community" category and we will help you prepare!

 We also have a vibrant [Twitter account]([https://](https://twitter.com/linuxnetdata)) and a [reddit channel](https://www.reddit.com/r/netdata).

## Provide feedback

We love feedback. It's what makes us better as developers, professionals and open-source maintainers. It's what makes Netdata better as a product, for everyone, for free!

If you have any comment about the product, a positive or negative comment, a request, please let us know by making a post at [at Netdata Community](https://community.netdata.cloud/) to discuss it. 

**We can't commit** that we will address the issue right away, but we will acknowledge your issue, and take notes of it! Although we use an internal Product Roadmap, we take your feedback and feature requests very seriously, so you can rest assured that if a particular feature requests gathers a lot of community votes, it will be prioritized accordingly.

# Become a Netdata Supporter

Netdata is a complex system, with many integrations for the various  collectors, export destinations and notification endpoints. As a result, we rely on help from "Supporters", users who are willing to **provide feedback** while we implement certain parts of the Netdata Agent. 

Netdata follows a highly opinionated approach to monitoring, offering a zero-configuration experience to users, as we take all the responsibility to organize the metrics into meaningful charts and create sane default alarms for them. This add an additional layer of complexity in the implementation of each integration, since we need 2 things:
1) Domain expertise to organize the metrics into meaningful charts and define sane alarms for them.
2) Production systems to test the integration on real-life systems before releasing it for the rest of the users.

To cover the **hundreds** of systems that we do, we have relied on kind users who were willing to discuss with us their use-cases while we develop the integrations and then test them on production systems to verify that they are valuable. 

> To become a "supporter", simply create a topic in the [Netdata Agent Development & Integrations](https://community.netdata.cloud/c/agent-development/9) category of our community forums.

Let's see the categories for which we are looking for supporters:

## Support a collector

Netdata is all about simplicity and meaningful presentation. A "supporter" for a collector assists with the following:

-   Provides feedback to the Netdata engineers about:
    - The organization of metrics into meaningful charts
    - The alarms that are sensible to be defined for each chart, as well as, their sane defaults.
-   When the implementation passes QA, tests the implementation in production.
-   Uses the charts and alarms in their day to day work and provides additional feedback.
-   Requests additional improvements as things change (e.g. new versions of an API are available).

## Support an exporting connector

 A "supporter" for a connector:

-   Suggests ways in which the information in Netdata could best be exposed to the particular endpoint, to facilitate meaningful presentation.
-   When the implementation passes QA, tests the implementation in production.
-   Uses the exporter in their day to day work and provides additional feedback, after the backend is delivered.
-   Requests additional improvements as things change (e.g. new versions of the exporter API are available).

## Support a notification method

A "supporter" for a notification method:

-   Points the Netdata engineers to the documentation for the API and identifies any platform-specific features of interest (e.g. the ability in Slack to send a notification either to a channel or to a user).
-   Uses the notification method in production and provides feedback.
-   Requests additional improvements as things change (e.g. new versions of the API are available).


## Become an active community member

As the project grows, an increasing share of our time is spent on supporting this community of users on how to use and extend Netdata. Participating actively on our community forums, providing feedback and helping other users out is crucial.

A community is a complex system, a network of people. The only way forward is the decentralization of the community over various community members who lead a particular cluster of a community. Quite simply, the Netdata team can not stay connected and engage over a certain number of people, not only because of time and intrinsic constraints (e.g [Dunbar's Number](https://en.wikipedia.org/wiki/Dunbar%27s_number)).

Every active member is a connection point of a new user with the community. The more active users we have, the more new users we can attract to the community and create a lively community that pushes the project forwards, innovates and helps each other in an peer-to-peer manner.


## Improve documentation

As Netdata's features grow, we need to clearly explain how each feature works and document all the possible configurations. And as Netdata's community grows, we need to improve existing documentation to make it more accessible to people of all skill levels.

We also need to produce beginner-level tutorials on using Netdata to monitor production-level systems, from databases to web-servers and Kubernetes clusters. Whatever you use for production, it's a perfect case-study for Netdata!

Start with the [guide for contributing to documentation](/docs/contributing/contributing-documentation.md), and then review the [documentation style guide](/docs/contributing/style-guide.md) for specifics on how we write our documentation.

You can submit your guide on our [Community Guides](https://community.netdata.cloud/c/community-guides/17) category and get initial feedback from the community and the Netdata team. Afterwards, we can work together to incorporate the guide into the main corpus of the documentation. Again, we can't commit to do that, since every piece of documentation(such as a guide) increases the cost of maintenance.

For that reason, we prefer to start with the Community Forums, where people can create any guide that they feel like sharing with the rest of the Netdata Community. If we believe that the use-case has value for the broader Netdata Community (e.g it's not about an edge-case), then it is possible that we may ask you to work with us and publish it in [Netdata Learn](Https://learn.netdata.cloud), our education portal.


# Developers

Since the initial release of Netdata back in 2016, hundreds of contributors have come together to improve the agent in any way possible. 

## Why contribute to Netdata

You might be interested to join our growing community of contributors if:

1) You find a bug and want to fix it
2) You need a feature that is not yet implemented and you want to do it yourself
3) You want to use Netdata to monitor a system or application that we don't currently support
4) You want to export metrics from Netdata to a platform that we don't currently support
5) You have created a new alarm for an existing data source
6) You have created a new alarm notification method
7) You want to contribute a useful custom dashboard that you have created
8) You have created an awesome integration of Netdata with another system

## What you can expect of us

1) We give our outmost attention to our contributors. We are committed to engage and evaluate every single contribution to our projects
2) We will acknowledge the value that you are providing and we will clearly state the reasons behind accepting or not accepting a contribution. 
3) We won't accept all contributions, as every contribution adds to the maintenance cost of the codebase. We have to carefully evaluate that cost over the benefit that the particular contribution will bring to users.
4) We will invite you to the user group on our [Community Forums](https://community.netdata.cloud), reserved only for Netdata Contributors.
5) If you are a first-time contributor, we will send you a thank you swag package!

## Contribution Quickstart

The workflow for contribution is the same no matter the component to which you contribute (with the exception of the ebpf collector, we will address it separately).

To enable you, we have created a Docker container that has everything you need to start developing for Netdata right away. By working from inside the container:

- You don't need to install any dependencies
- You isolate your developer environment from your work/personal machine

### Contribution Workflow 

1) Fork the repository that you are interested in
2) Make sure that Docker is installed and started
3) Download Visual Studio Code
4) Clone your forked repository on your local machine
5) Open the directory using [Visual Studio Code](https://code.visualstudio.com/download)
6) Click on the popup box that will appear and says "reopen directory inside developer container"
7) A VS Code window will appear that will have opened the current directory from inside the container. The filesystem that it shows as also the terminal that you can open is from inside that container. 
   1) You can start developing without installing any libraries or dependencies. 
   2) You can use the pre-installed tools (e.g apt, pip, git) to download additional software that you may need. Everything will be installed inside that particular container.
   3) We have installed a number of VS Code Extensions that we believe are useful to you. You can install any additional number of extensions. Note that these extensions will be installed inside the container and have nothing to do with those extensions that you may have installed locally if you are a VS Code user.

![visual studio code example](https://github.com/netdata/community/raw/main/devenv/remote-containers-readme.gif)

## Additional Resources

### Contribute a new feature (or improve an existing one) for the Netdata Agent

If you want to develop or improve a feature for the Netdata Agent core functionality (e.g `dbengine`, `daemon`, `alarms`), you will need to be knowledgeable in C, since the Agent is almost completely developed in C. This is a matter for efficiency of course, since monitoring thousands of metrics with a per-second granularity is no easy task!

To contribute a new or improved feature:
1) Fork the [netdata/netdata](https://github.com/netdata/netdata) repository
2) Download the forked repository locally
3) Open the directory using VS Code
4) Develop ⛏
   1) Authenticate with GitHub from inside the container
   2) Create a new branch and name it after the feature you are developing (e.g "apache-collector"). Switch to that branch.
   3) After you are done developing, you can easily build Netdata from source using the command: `netdata-install`. This alias loads the `netdata-installer.sh` script with a few additional debugging flags to facilitate you in the your work.
   4) After running `netdata-install` once, you can instead using `netdata-build`. The first commands downloads some additional dependencies from the Internet. Once you have done it once, you don't need to repeat it. `netdata-build` is much faster than `netdata-install`. 
   5) In case your contribution is in the `netdata-installer.sh` script itself, you will need to use exclusively `netdata-install` to verify that it works as expected.
5) **Optional:** Valgrind to verify that there are no memory leaks in Netdata after your changes. If you are not familiar with the software, no worries. It's optional!
6) Build Netdata one last time using `netdata-install` to verify that everything works as expected.
7) Commit your changes to the branch (e.g "apache-collector") and push to GitHub
8) Make a **draft PR** from that branch to the master branch of the `netdata/netdata` repository.

### Contribute a new collector

The Netdata Agent has a modular approach to collecting data from data sources, meaning that we have a number of collector plugins that send data to the Netdata Agent. For each collector plugin, you can create a new module which collects data from a data source, currently you can create plugins in 4 frameworks:

1) Python
2) Golang
3) Node.d (deprecated)
4) C (internal plugins)
5) Shell

When deciding which framework to use, please consider our approach:
1) Golang is used for all production-grade collectors and *most* of the python collectors will be migrated to Golang. We actively support, maintain and improve the Golang collectors. We are migrating to Golang for 2 reasons:
   1) Slightly more performing
   2) Considerably easier to maintain and use, since they don't require any dependency on the machine which runs the Netdata Agent (e.g python collectors require python).
2) Python is used for quick PoC, because it's a more widely-known language. Although there are vastly more python collectors that in golang, we can't ensure that each and every one works, since a large number of them was contributed by the community. 
3) C is used for internal plugins and some external. It is the language we prefer for implementation of collectors, since it's efficient. If you are not familiar with C, no worries, we will be excited to receive contributions in either Golang (preferably) or Python.
Although we understand that you will want to contribute with the framework that you feel more comfortable in, we would **prefer** if the new collector was in Golang.

To contribute a new collector (or improve an existing one):
1) Fork the [netdata/netdata](https://github.com/netdata/netdata) repository
   1) If it's a Golang repository, fork the [netdata/go.d](https://github.com/netdata/go.d) repository
2) Download the forked repository locally
3) Open the directory using VS Code
4) Develop ⛏
   1) Authenticate with GitHub from inside the container
   2) Create a new branch and name it after the feature you are developing (e.g "apache-collector"). Switch to that branch.
   3) For Python collectors:
      1) Follow the contribution guidelines on the [python.d](https://learn.netdata.cloud/docs/agent/collectors/python.d.plugin) documentation.
      2) Follow the Guide we have released: [How to contribute a Python collector]
   4) For Golang collectors:
      1) Follow the contribution guidelines on the [go.d](https://learn.netdata.cloud/docs/agent/collectors/go.d.plugin) documentation.
      2) Follow the Guide we have released: [How to develop a go.d collector](https://learn.netdata.cloud/docs/agent/collectors/go.d.plugin/docs/how-to-write-a-module).
   5) For Shell/Bash
      1) Follow the guidelines on the [charts.d](https://learn.netdata.cloud/docs/agent/collectors/charts.d.plugin).


### Contribute a new exporting engine destination 

The exporting engine is written in C and such the contribution process is the same in [Contributing a new feature](#contribute-a-new-feature-or-improve-an-existing-one-for-the-netdata-agent)

### Contribute a new alarm definition

Netdata has an opinionated approach to monitoring, enabling the user to quickly get up to speed and running, without having to spend any time in creating charts and alarms. As such, it comes with sane defaults that have been curated by both industry experts, our team, and everyday users. 

There are 2 reasons why you may want to contribute to our alarms:
1. You want to improve the sane defaults by modifying an existing alarm or adding a new one
2. You want to contribute a new collector. Every new collector should come with some basic alarms out-of-the-box

To do both, you will need to create (or modify) alarm configuration files. Our [documentation](https://learn.netdata.cloud/docs/monitor/configure-alarms) details the process. To develop and test the alarm, you will only need an active installation of the Netdata Agent, so the developer container described above is not required.

### Contribute a new alarm notification

The Netdata Agent supports a large variety of alarm notifications. In essence, the Netdata Agent uses the alarm definitions to understand whether it should fire an alarm notification and then proceeds by executing a script called `alarm-notify.sh`.

In order to modify existing ones or create new notification alarms you will need to code in `bash`.

To create a new alarm, we can look to:
- Already implemented alarms inside `alarm-notify.sh` and copy their structure
- Use the [custom endpoint](https://learn.netdata.cloud/docs/agent/health/notifications/custom) notification as boilerplate.


#### Code of Conduct and CLA

We expect all contributors to abide by the [Contributor Covenant Code of Conduct](https://netdata/.github/CODE_OF_CONDUCT.md). For a pull request to be accepted, you will also need to accept the [Netdata contributors license agreement](CONTRIBUTORS.md), as part of the PR process.

#### Performance and efficiency

Everything on Netdata is about efficiency. We need Netdata to always be the most lightweight monitoring solution available. We may reject to merge PRs that are not optimal in resource utilization and efficiency.

Of course there are cases that such technical excellence is either not reasonable or not feasible. In these cases, we may require the feature or code submitted to be by disabled by default.

Don't worry, our engineers will guide you through the process in measuring the performance of the contributed feature.

#### Meaningful metrics

Unlike other monitoring solutions, Netdata requires all metrics collected to have some structure attached to them. So, Netdata metrics have a name, units, belong to a chart that has a title, a family, a context, belong to an application, etc.

This structure is what makes Netdata different. Most other monitoring solution collect bulk metrics in terms of name-value pairs and then expect their users to give meaning to these metrics during visualization. This does not work. It is neither practical nor reasonable to give to someone 2000 metrics and let him/her visualize them in a meaningful way.

So, Netdata requires all metrics to have a meaning at the time they are collected.  We will reject to merge PRs that loosely collect just a "bunch of metrics", but we are very keen to help you fix this.

#### Netdata is a distributed application

Netdata is a distributed monitoring application. A few basic features can become quite complicated for such applications. We may reject features that alter or influence the nature of Netdata, though we usually discuss the requirements with contributors and help them adapt their code to be better suited for Netdata.

#### Operating systems supported

Netdata should be running everywhere, on every production system out there.

Although we focus on **supported operating systems**, we still want Netdata to run even on non-supported systems. This, of course, may require some more manual work from the users (to prepare their environment, or enable certain flags, etc).

If your contributions limit the number of operating systems supported we will request from you to improve it.

#### Documentation

Your contributions should be bundled with related documentation to help users understand how to use the features you introduce.

#### Maintenance

When you contribute code to Netdata, you are automatically accepting that you will be responsible for maintaining that code in the future. So, if users need help, or report bugs, we will invite you to the related github issues to help them or fix the issues or bugs of your contributions.

#### Code Style

The single most important rule when writing code is this: *check the surrounding code and try to imitate it*. [Reference](https://developer.gnome.org/programming-guidelines/stable/c-coding-style.html.en)

We use several different languages and have had contributions from several people with different styles. When in doubt, you can check similar existing code.

For C contributions in particular, we try to respect the [Linux kernel style](https://www.kernel.org/doc/html/v4.10/process/coding-style.html), with the following exceptions:

-   Use 4 space indentation instead of 8
-   We occasionally have multiple statements on a single line (e.g. `if (a) b;`)
-   Allow max line length of 120 chars
-   Allow opening brace at the end of a function declaration: `function() {`.
-   Allow trailing comments

### Your first pull request

There are several guides for pull requests, such as the following:

-   <https://thenewstack.io/getting-legit-with-git-and-github-your-first-pull-request/>
-   <https://github.com/firstcontributions/first-contributions#first-contributions>

However, it's not always that simple. Our [PR approval process](#pr-approval-process) and the several merges we do every day may cause your fork to get behind the Netdata master. If you worked on something that has changed in the meantime, you will be required to do a git rebase, to bring your fork to the correct state. A very easy to follow guide on how to do it without learning all the intricacies of GitHub can be found [here](https://medium.com/@ruthmpardee/git-fork-workflow-using-rebase-587a144be470)

One thing you will need to do only for your first pull request in Netdata is to accept the CLA. Until you do, the automated check for the CLA acceptance will be showing as failed.

#### PR Guidelines

PR Titles:

- Must follow the [Imperative Mood](https://en.wikipedia.org/wiki/Imperative_mood)
- Must be no more than ~50 characters (_longer description in the PR_)

PR Descriptions:

- Must clearly contain sufficient information regarding the content of the PR, including area/component, test plan, etc.
- Must reference an existing issue.

Some PR title examples:

- Fix bug in Netdata installer for FreeBSD 11.2
- Update docs for other installation methods
- Add new collector for Prometheus endpoints
- Add 4.19 Kernel variant for eBPF
- Fix typo in README
- Refactor code for better maintainability
- etc

The key idea here is to start with a "verb" of what you are doing in the PR.

For good examples have a look at other projects like:

- https://github.com/facebook/react/commits/master
- https://github.com/tensorflow/tensorflow/commits/master
- https://github.com/vuejs/vue/commits/dev
- https://github.com/microsoft/vscode/commits/master
- Also see the Linux Kernel and Git projects as well as good examples.

#### Commit messages when PRs are merged

When a PR gets squashed and merged into master, the title of the commit message (first line) must be the PR title
followed by the PR number.

The body of the commit message should be a short description of the work, preferably taken from the connected issue.

### PR approval process

Each PR automatically [requires a review](https://help.github.com/articles/about-required-reviews-for-pull-requests/) from the code owners specified in `.github/CODEOWNERS`. Depending on the files contained in your PR, several people may be needed to approve it.

We also have a series of automated checks running, such as linters to check code quality and QA tests. If you get an error or warning in any of those checks, you will need to click on the link included in the check to identify the root cause, so you can fix it.

If you wish to open a PR but are not quite ready for the code to be reviewed, you can open it as a Draft PR (click the dropdown on the **Create PR** button and select **Draft PR**). This will prevent reviewers from being notified initially so that you can keep working on the PR. Once you're ready, you can click the **Ready for Review** button near the bottom of the PR to mark it ready and notify the relevant reviewers.
