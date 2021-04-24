# my-logging
Logging : A key element in modern software system

this is abhay shukla from GBSU/ARC/SOL/SGM|Monitoring

i have been using logging system from from starting of my carrer. Used in Apple (hardware), retail(target), Panasonic Kiosk (ClearConnect™ ecosystem ), societe generale (Banking & finance)


Why


----
Observability : why we need IT system to be observable ?
1. We need to discover problems in it system, infra, application
2. Need to be able to fix problem, when they discovered, efficiently
3. would like to understand system, how multile system work together, by seeing logs, metrics, 
4. Audit : who, when , why, 
5. Reporting : what happen last months, stats : daily, monthly, yearly
6. Forecasting : ex.: how many users/infra, we have now, how many user/infra we are expecting in next months
----

https://www.youtube.com/watch?v=va_3khi5pM8

make system observable
collect -> Centralize the data -> monitor/alert/dashboard/report/Drill-down/analysis

Logs  |  Metrics  :- two differents aspect of this spectrum

1. Logs are events - metrics are aggregates of events


Arch :
beats/fluentd/logstash -> Central log management system -> user / alerts


Log shipping : log to file -> ship logs to log management system  or configure log library to ship logs to log management system

Orchestration : backend system (docker/k8s/pods -> central log management system -> user/alerts)



-----
What to log/not to log

Read your logs : if you read the logs, then only you can improve the logs
Logs evolve : Changing logs -> Adjusting logs  (Reading logs -> Improving logs)

Best practise : whenever(local/dev/prod) i run or deploy app/system/software, i read logs


Workflow : Logs from workflow tells story
1. Id's : request, sesstion, background jobs
2. Lifecycle events : start stop crash
3. Progress
4. Statem machine transition 
5. Timing, sizes , counts - event level metrics

Increase the Context of your logging- increase dimensionality : slice and dice your story
1. Id's
2. User information 
3. Source file and line number
4. Caller Id (Session , request, job)
5. Origaniting id (Session , request, job)
6. Host, Service, pod, task, container (name, ID)

Log management from User Prospective :
Filter
Group by and time chart
Follow the tail
Dashboards
Alerts


Tips and Tricks :
1. Log levels : debug, info, error, warning , error
2. Log to file vs send directly to managent system
3. Log format : JSON ? [timestamp] [thread] INFO [Message]
4. Metrics together with logs
5. Git hash(version of system/code) config in startup log
6. Follow the tail during deploy












================================================================================================
purpose : tracking/ Auditing/ Monitoring

Logger : 2 type -> ConsoleAppender(dev) / FileApender(support)

debug  : general info (low prirority mess)
info : general info (low prirority mess)
warn : some action , which are not suppose to be done by user, but still accedently he/she clicked on button.  then warn
error : Any exception, authentication , if 1 user  facing issue  then error
fatal : if many user facing issue then fatal

trace

https://www.youtube.com/watch?v=ifIlljI4FZY


The logging module in application gives you everything you need to report progress and problems in your code. It would be nice if developers and machine were 100% reliable.. but let be honest. Life is messy. You are expecting an Integer, someone hands you a float. You call cloud API - the serveices is down for maintainance. 
A wide range of problem can happen, that are out of your control. With logging you can leave a trail of breadcrumbs, so when something can goes wrong, you can determin the cause. Hope for the best, but plan for the worst - with logging.


Distributed logging : 

https://www.youtube.com/watch?v=WzHgOl3xvu4

1. Centralized logging capability
2. Centralized log tracing
3. Generate Report to get specific type of error
4. Alert Machanism based on error spotted in the log


Monolithic Application : app -> files (tail the logs from files)





