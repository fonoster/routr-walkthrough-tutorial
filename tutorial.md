# Introduction to Routr SIP Server

## Let's get started!

Get up and running with Routr SIP Server by following this interactive tutorial.

This guide will show how to install and run your own instance of Routr server. It'll also walk you through the steps of connecting to the server using the command-line tool and the web UI. 

**Time to complete**: About 10 minutes

Click the **Next** button to move to the next step.

## What is Routr?

Before we jump in, let's briefly go over what Routr can do.

Routr is a sip proxy, location server, and registrar that provides a reliable and scalable SIP infrastructure for telephony carriers, communication service providers, and integrators.

This tutorial will go over two mayor components of the project, Routr server and Routr CTL; helping you familiarize with the steps of deploying a new VoIP network.

Continue on to the next step to begin the tutorial.

## Downloading and Installing Routr SIP Server

Routr server is a standalone software and does not need any dependency to run. Routr runs on all mayor operative system, as well as microservices enviroment like [Docker](https://www.docker.com/)

The first step in running a Routr server instance is downloading the server.

To download the server run this command:
```bash
wget https://github.com/fonoster/routr/releases/download/1.0.0-rc1/routr-1.0.0-rc1_linux-x64_bin.tar.gz
```

**Tip**: Click the copy button on the side of the code box and paste the command in the Cloud Shell terminal to run it.

### Then extract the files

To extract the files run this command:
```bash
tar xvfz routr-1.0.0-rc1_linux-x64_bin.tar.gz
```

Next, you’ll launch Routr server

## Launch the Server

To run the server just `cd` into the directory you've just extracted and run the `routr` command.

To start the the server run this command:
```bash
cd routr-1.0.0-rc1_linux-x64_bin && ./routr
```

<walkthrough-footnote>Please wait for the server to launch and be sure to review output for some relevant information.</walkthrough-footnote>

Next, you will install the command-line tool.

## Installing the Command-Line tool

The command-line tool will allow you to control and monitor a Routr instance. The command-line tool `rctl` ships as a separate component.
Please open an additional cloud shell and install command-line.

<walkthrough-open-cloud-shell-button open-cloud-shell/>

### Install command-line

To install command-line tool run this command:
```bash
npm install -g routr-ctl
```

Next, you will login to the server using the Command-Line tool.

## Login to a Routr instance using the Command-Line tool

To issue commands to a Routr instance you must first login.

To login to your instance run this command:
```bash
rctl login -u admin -p changeit https://172.17.0.2:4567/api/v1beta1
```

Next, you will issue some basic commands and launch the web UI.

## Issue basic commands

The command-line tools allows you to issue commands to a Routr instance. The following are some examples.

### Getting a list of carriers

To list the available carriers run this command:
```bash
rctl get gateways
```

### Getting a list of domains

To see the available domains run this command:
```bash
rctl get domains
```
### Launch the web UI (Bonus step)

To launch the web UI run this command
```bash
rctl proxy -p 8080
```

You can now preview the <walkthrough-spotlight-pointer spotlightId="devshell-web-preview-button" text="web UI"></walkthrough-spotlight-pointer>

**Tip**: Check the [cheat sheet](https://routr.io/docs/administration/cli/cheatsheet/) for more command-line examples.

## Congratulations

<walkthrough-conclusion-trophy></walkthrough-conclusion-trophy>

You’re all set!

You can now install and run a Routr instance and issue some basic commands. 

For more tutorials and information about Routr, refer to the [Routr Offical Website](https://routr.io/docs/overview).

**Don't forget to clean up after yourself**: If you created test projects, be sure to delete them to avoid unnecessary charges. Use `gcloud projects delete <PROJECT-ID>`.
