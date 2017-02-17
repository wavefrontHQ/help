Optionally specify metric name, source name, and point tag value filters as Javascript regular expressions that the series must match.
<dl>
<dt>Metric Filter Regex</dt>
<dd>A regular expression that metric names must match. E.g.: jvm\.memory\.heap\w+</dd>
<dt>Source Filter Regex</dt>
<dd>A regular expression that source names must match. E.g.: co-2a-app[0-9]+-i-\d+</dd>
<dt>Point Tag Filter Regexes</dt>
<dd>A point tag key and a regular expression that point tag values must match.</dd>
<dt><strong>Tag Key</strong> env<br/><strong>Filter Regex</strong> prod\w+</dt>
</dl>
Specify the external link URL template. The template employs [Mustache syntax](https://mustache.github.io/). The properties supported by the template are:
<dl>
<dt>source</dt>
<dd>The source of the series.</dd>
<dt>startEpochMillis</dt>
<dd>Starting time of the chart window, in milliseconds from the UNIX epoch.</dd>
</tr>
<tr>
<dt>endEpochMillis</dt>
<dd>Ending time of the chart window, in milliseconds from the UNIX epoch.</dd>
</tr>
<tr>
<dt>&lt;pointTagName1&gt;, &lt;pointTagName2&gt;,...</dt>
<dd>One or more point tag names associated with the series.</dd>
</dl>

For further information, see:
- [External Links](https://community.wavefront.com/docs/DOC-1242)
