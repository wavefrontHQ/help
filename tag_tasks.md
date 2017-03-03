### Adding Tags
1. Choose which {{include.entities}} to tag:
    - Check the checkboxes next to the {{include.entities}} and click the **+ Tag** button.
    - Click **+tag** below {{include.entity}}.
1. In the **Add Tag** dialog:
    - Optionally start typing a tag name to filter the list of tags and click a tag.
    - Click **Create Tag**:
        1. Type a tag name. Tag names are case sensitive; the tags **MyApp** and **myapp** are distinct tags.
        1. Click **Add**.

### Searching for Tags
When there are enough tags, type a tag name in the Search box below **Tags** in the filter bar.
The search process is case insensitive; searching for **myapp** returns **MyApp** and **myapp**.

### Filtering by Tags
Click a tag icon ![agents tag](images/agents_tag.png#inline) in the filter bar or below an entity.

### Tag Paths
Tags are organized in a hierarchy by separating tag components with a dot **'.'**: **MyService.MyApp**.

### Searching Tag Paths
Trailing wildcards ".\*" are supported when searching tag paths. To match all tags starting with
**tagPath.**, type **tagPath.\***.
