> What is exadata bundle patching ? 

# Table of Contents

- [Table of Contents](#table-of-contents)
  - [Scheduling](#scheduling)
  - [Run exachk](#run-exachk)
  - [Fill patching template](#fill-patching-template)
  - [Review patch assessment](#review-patch-assessment)
  - [Review patch plan](#review-patch-plan)
  - [Review prechk logs](#review-prechk-logs)
  - [OS Backup](#os-backup)
  - [Pre-ver](#pre-ver)
  - [Patching](#patching)
  - [Post exachk](#post-exachk)
  - [Post verification](#post-verification)


## Scheduling
---
. Every customer who have the exabox will have a scheduling tool url which will hosted on the gateway server so this link will be given to each customer has to log into the platinum gateway tool and then they need to schedule the patching request so whichever date is available 

Schedule patching through scheduling tool which will gnerate the patching SR# automatically 
Please refer the platinum scheduling tool document 
## Run exachk
Once the patching is scheduled customer need to run and upload exadata check report to the sr once you schedule the patcing there will be an automatic sr created and then to that SR you need to upload exa check report
Run and upload the Exachk report to oracle SR# 4-5 weeks in advance  otherwise your patching will be cancelled by oracle 
## Fill patching template
 once you uploade the report then there's a patching template 
again customer responsibility they have
to fill that patching template and then
upload it to the
sr again and then once these three steps
are done from a customer

Fill the patching template upload to oracle SR# 4-5 weeks in advance so if you missed to upload the template oracle engineer will keep reminding you in the SR if you missed it your patching is going to be cancelled by oracle make sure you need to follow this strict timelines 
## Review patch assessment
customer side you know next patch
engineer oracle engineer will come
and he will read my patching template
and he will read exact report and then
he will prepare a patch assessment
- when you upload the Exa report and patch template then comes to the oracle engineer will review them so, If there are nay issues or if it is not run properly then he/she will reintimate you to run the exadata check report and then upload the proper template and then based upon these two exa check report and template oracle is going to create a patch assessment it's basically tells about what is my current database and what is my current patch level and what is my oracle home and what is my grid home option what is my target home option is there any one-offs or backboards requested all the details will be find out in the patches assessment like a report where it can say that what is my current state , what is my current patch level and what is my target value let's say everythign is in that and is there any critical issues in my system so that I need to fix it oracle will highlight there are critical issues that customer responsiblity to fixed theme or open a new SR if there is no critical issues oracle will give a grow green signal we're good with the patch assessment he will create a patch assessment and upload it back to the SR and again customer has to download and review and then customer has to find out is there any critical issues if there any of them that will be highlighted by oracle engineer and then customer and then oracle together they can fix those issues before the patching    
- Patch Assessment ( PA ) will be provided 4 weeks before the patching if oracle cross this deadline customer can escalate to the oracle why it is not done on the timely manner 
## Review patch plan
and then he will prepare a patch plan
and then he will do the pre-checks
patch assessment is which is the current
version what is the target version
uh you know customer want to go and the
patch plan is the detail
steps uh the detail technical execution
steps
which can be used during the patching so
patch engineer will just refer this
patch there and copy and paste the
commands from this patch plan
he will not deviate apart from this
patch plan
- Patching Plan again oracle engineer will prepare a patch plan excel sheet and where it contains my patching details IB switch patching details and database patching details everything technical steps will be written there and oracle is going to refer that patch plan during the patching oracle just copy the commands from the patch plan and then paste it into my production box or whatever dev box he's not supposed to deviate from thsi patch plan what is why he wil provide this patch plan this plan will be provided <b> 2 weeks in advance </b> if oracle cannot provide it before this timeline customer can escalate to oracle and then get it done it's the customer responsiblity to download the patch plan and review theme and then you know if there is any descrpancy they can always go back to oracle  and then I will show you   how the patch plan template look like 
## Review prechk logs
patch plan so pre-checks is like it will
be done one week prior to the patching
and then
- Patch Pre-check will be <b> one week in advance</b>
## OS Backup 
make sure that you know our system is
good to go ahead with the patching
and then again customer responsities to
take a necessary os backup and then
uh you know make sure that in case of
any failures
we should be able to restore it using
those backups
## Pre-ver
and then there's a pre-verification and
handover system to the patching
so it's again customer responsibility to
capture my current state what all
databases are running what all listeners
are running and then what all services
are running
what is my cluster state and what is my
cluster health state everything has to
be
verified and then you know handed over
to the oracle engineer for the patching
## Patching 
okay so now uh where we are like one you
have to verify our system and then hand
over system to the oracle engineer he
will
start with the patching activity so
coming to the step number nine
where oracle engineer will shut down our
cluster database and all then he will
start with our
patching activity actual patching
activities happens here he will do our
db node patching cell node patching
iv switch patching and you know oracle
home patching and then you know uh
database
data you know data patch or cat funnel
everything will be done by oracle
engineer once foreign do patching
## Post exachk
then he will hand over back the system
to customer
again customer will run uh post exact
report and then that will be reviewed by
again oracle engineer
so this post exit check can be run by
oracle engineer or customer like anybody
can run it and then
upload it back to the sr and then oracle
engineer will review it and then make
sure that
you know when there are no critical
issues noted in that the check report if
there are any critical issues
oracle engineer is going to fix them and
then after that customers will
## Post verification
Again do post verification like you know
making sure all databases listeners and
services
applications everything is able to
communicate and then run the business as
usual