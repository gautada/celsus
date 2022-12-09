# Architecture Principle: Instrumentation over Logging

A good logging format

```
{DATE} {TIMESTAMP} {family} {origin}:{level}-{message}
```

```
YYYYMMDD HH:MM:SS+TZ application coredns:I~This is a logging attempt
```

https://docs.python.org/3/howto/logging.html
https://www.mend.io/resources/blog/how-to-instrument-application-logging/
https://www.loggly.com/blog/log-log-proven-best-practices-instrumentation/
https://newrelic.com/blog/best-practices/logging-vs-instrumentation
