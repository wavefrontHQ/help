orElse() | orelse() cannot return a reasonable result, because the wrapped query \"%s\" found more than 10M active
series and cannot be queried without supplying explicit point tags/sources. See [Optimizing 
High Cardinality Data](https://docs.wavefront.com/cardinality.html#optimizing-high-cardinality-data).