Wildcard: [[queryFunctionName type=header text="'*' to match strings"]]

**Tips to improve performance**
- Do not start a query with a wildcard
- Use delimiters around wildcards if possible, for example,e.g. ts(‘abc.*.xyz') is more efficient than ts(‘abc*xyz’) 