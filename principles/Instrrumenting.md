# Architecture Principle: Instrumentation over Logging

Logging can be time consuming and difficult to coordinate across mutiple services. Instrumentation is the act of defining a healthy state for an application and then monitoring metrics, events, logs, and traces (MELT) to determine holistically the deviation from healthystate in realtime. Logging is a part of instrumentation but instrumentation and health states are the prefered approach.


** -- MOVE TO PATTERN -- **

## Log Formats

```
{DATE} {TIMESTAMP} {family} {origin}:{level}-{message}
```

```
YYYYMMDD HH:MM:SS+TZ application coredns:I~This is a logging attempt
```

- https://docs.python.org/3/howto/logging.html
- https://www.mend.io/resources/blog/how-to-instrument-application-logging/
- https://www.loggly.com/blog/log-log-proven-best-practices-instrumentation/
- https://newrelic.com/blog/best-practices/logging-vs-instrumentation
