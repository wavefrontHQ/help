## What is an External Link? 

External links provide integration between Wavefront and external systems. If you use logging systems such as ELK and
Splunk, you can easily construct a meaningful URL to navigate from Wavefront to a log entry.

For example, suppose while analyzing metrics data, you find an anomaly such as an unexpected drop in transaction rate,
and you want to navigate to logs to look for entries that could shed light on why the transaction rate drop occurred.
The external links feature allows you to click through from a Wavefront series directly to a related entry in your
logging system. While this example focuses on a log scenario, the feature is general purpose: you can link through to
any type of system.

An external link consists of a templated URL that contains information about metric names, source names, point tag
values, and time window of the originating series.
