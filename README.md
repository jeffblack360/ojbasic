# Oracle JET on OpenShift

This git repository helps you get up and running quickly with Oracle JET on OpenShift. This repo combines the Oracle JET v2.1.0 Basic Quickstart template with [https://hub.openshift.com/quickstarts/92-do-it-yourself-0-1](OpenShift's Do-It-Yourself 0.1 Cartridge).

Oracle JET provides developers a modular JavaScript toolkit for building modern HTML5 applications coupled with a powerful PaaS running on OpenShift. OpenShift's Do-It-Yourself application template is a blank slate to build out your own applications and integrate the server technology of your choosing with a state-of-the-art JavaScript toolkit. The DIY server is a barebones Ruby server without any backend services.  Oracle JET is pre-configured and ready to go out-of-the-box. Introduce your own backend services via OpenShift's array of cartridges. Visit the [Oracle JET website](http://oraclejet.org) and the [OpenShift website](http://openshift.com) for all the details.

## Running on OpenShift

Create an account at [https://www.openshift.com/](https://www.openshift.com/)

Create a DIY application 

```
rhc app create ojbasicdiy diy-0.1
```

Add this upstream Oracle JET Basic Quickstart repo

```
cd ojbasic
git remote add upstream -m master git://github.com/jeffblack360/ojbasicdiy.git
git pull -s recursive -X their upstream master
```

Then push the repo to OpenShift

```
git push
```

That's it, you can now checkout your application:

http://ojbasicdiy-$yournamespace.rhcloud.com

See the [Oracle JET Developer Guide](http://docs.oracle.com/middleware/jet210/jet/) for complete installation details, including prerequisites.

## [Documentation](http://docs.oracle.com/middleware/jet210/jet/)
Oracle JET comes with a full [Developers Guide](http://docs.oracle.com/middleware/jet210/jet/) to help with Getting Started and many common issues.
