# Introduction to Routr SIP Server

## Let's get started!

Get up and running with Routr by following this interactive tutorial.

This guide shows how to install and run an instance of Routr server. It'll also walk you through the steps of connecting to the server using the command-line tool and the web UI.

**Time to complete**: About 10 minutes

Click the **Next** button to move to the next step.

## What is Routr?

Before we jump in, let's briefly go over what Routr can do.

Routr is a sip proxy, location server, and registrar that provides a reliable and scalable SIP infrastructure for telephony carriers, communication service providers, and integrators.

This tutorial goes over Routr's major components and can help you familiarize with the steps of deploying a new VoIP network.

Continue to the next step to begin the tutorial.

## Downloading and Installing Routr SIP Server

Routr server is a standalone software and does not require any dependencies to work. Routr runs on all mayor operative system, as well as a microservices environment like [Docker](https://www.docker.com/)

The first step in running an instance of Routr is downloading the server.

To download the server run this command:
```bash
wget https://github.com/fonoster/routr/releases/download/1.0.0-rc5/routr-1.0.0-rc5_linux-x64_bin.tar.gz
```

**Tip**: Click the copy button on the side of the code box and paste the command in the Cloud Shell terminal to run it.

### Then extract the files to the current directory

To extract the files, run this command:
```bash
tar xvfz routr-1.0.0-rc5_linux-x64_bin.tar.gz
```

Next, you'll launch an instance of Routr server.

## Launching the Server

To run the server change into the directory you've just extracted and run the `routr` command.

To start the the server run this command:
```bash
cd routr-1.0.0-rc5_linux-x64_bin && ./routr
```

<walkthrough-footnote>Please wait for the server to launch and be sure to review the output for some relevant information.</walkthrough-footnote>

Next, install the command-line tool.

## Installing the Command-Line Tool

The command-line tool allows you to control and monitor the Routr instance. Please open a new cloud shell and install the command-line.

<walkthrough-open-cloud-shell-button open-cloud-shell/>

### Install the command-line using npm

Installing the npm package [routr-ctl](https://www.npmjs.com/package/routr-ctl) provides you with the globally accessible `rctl` command. To install command-line tool run this command:
```bash
npm install -g routr-ctl
```

Next, log in to the server using the command-line tool.

## Login to the Routr instance using the Command-Line Tool

To issue commands to your Routr instance, you must first login.

To login to your instance, run this command:
```bash
rctl login -u admin -p changeit https://127.0.0.1:4567/api/v1beta1
```

Next, issue some basic commands and launch the web UI.

## Issue basic commands

The command-line tools allow you to issue commands to your Routr instance. Here are some examples:

### Getting a list of carriers

To list the carriers available in your Routr instance run this command:
```bash
rctl get gateways
```

### Getting a list of domains

To see the available domains in your Routr instance, run this command:
```bash
rctl get domains
```
### Launching the web UI (Bonus step)

To launch the web UI run this command
```bash
rctl proxy -p 8080
```

You can now preview the <walkthrough-spotlight-pointer spotlightId="devshell-web-preview-button" text="web UI"></walkthrough-spotlight-pointer>

**Tip**: Check the [cheat sheet](https://routr.io/docs/administration/cli/cheatsheet/) for more command-line examples.

## Congratulations

<walkthrough-conclusion-trophy></walkthrough-conclusion-trophy>

You're all set!

You can now install and run a Routr instance and issue some basic commands.

For more tutorials and information about Routr, refer to the [Routr Offical Website](https://routr.io/docs).

**Don't forget to clean up after yourself**: If you created test projects, be sure to delete them to avoid unnecessary charges. Use `gcloud projects delete <PROJECT-ID>`.
