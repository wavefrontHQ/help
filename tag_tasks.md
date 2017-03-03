## Using Tags

### Adding Tags

1. Choose which entities to tag:
    - Check the checkboxes next to the entities and click the **+ Tag** button.
    - Click **+tag** below an entity.
1. In the Add Tag dialog:
    - Optionally start typing a tag name to filter the list of tags. Click the tag.
    - Click the **Create Tag** button at the bottom:
        1. Type a tag name. Tag names are case sensitive. For example, the tags **MyApp** and **myapp** are stored as distinct tags.
        1. Click **Add**.

### Searching for Tags
When there are enough tags you can type in the Search box below the Tags heading in the filter bar to filter the list of tags.
The search process is case insensitive; searching for **myapp** will return **MyApp** and **myapp**.

### Filtering by Tags
Click a tag icon ![agents tag](images/agents_tag.png#inline) in the filter bar or below an entity.

### Tag Paths
All tag types support the ability to organize tags in a hierarchy. The hierarchy is defined by separating tag components
with a dot **'.'**. For example, **MyService.MyApp**.

### Searching Tag Paths
You can type trailing wildcards ".\*" when searching tag paths. To match all tags starting with
**alertTagPath.**, enter **alertTagPath.\***.
