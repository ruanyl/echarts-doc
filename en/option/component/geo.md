{{ target: component-geo }}

# geo(Object)

Geographic coorinate system component.

Geographic coorinate system component is used to draw maps, which also supports [scatter series](~series-scatter), and [line series](~series-lines).

**Example of using scatter series in geographic coordinate:**
~[600x400](${galleryViewPath}scatter-map&edit=1&reset=1)


From `3.1.10`, geo component also supports mouse events, whose parameters are:

```js
{
    componentType: 'geo',
    // geo component's index in option
    geoIndex: number,
    // name of clicking area, e.g., Shanghai
    name: string,
    // clicking region object as input, see geo.regions
    region: Object
}
```

**Tip:**
The region color can also be controlled by map series. See [series-map.geoIndex](~series-map.geoIndex).


## show(boolean) = true

Whether to show the geo component.

{{ use: geo-common(
    prefix='#',
    galleryEditorPath=${galleryEditorPath},
    galleryViewPath=${galleryViewPath}
) }}

## regions(Array)
Configure style for specified regions.
For example:
```js
regions: [{
    name: 'Guangdong',
    itemStyle: {
        normal: {
            areaColor: 'red',
            color: 'red'
        }
    }
}]
```

The region color can also be controlled by map series. See [series-map.geoIndex](~series-map.geoIndex).


### name(string)
Name of area in map, like `'Guangdong'`, or `'Zhejiang'`.

### selected(boolean) = false
Whether this area is selected.

### itemStyle(Object)
Item style of this area.
#### normal(Object)
##### areaColor(Color)
Area color in the map.
{{ use: partial-item-style(prefix='####') }}
#### emphasis(Object)
##### areaColor(Color)
Area color in the map.
{{ use: partial-item-style(prefix='####') }}

### label(Object)
Label style of this region.
#### normal(Object)
##### show(boolean) = false
Whether to show label in normal state.
##### textStyle(Object)
Text style of label in normal state.
{{ use: partial-text-style(prefix='#####') }}
#### emphasis(Object)
##### show(boolean) = false
Whether to show label in emphasized state.
##### textStyle(Object)
Text style of label in emphasized state.
{{ use: partial-text-style(prefix='#####') }}



{{ use:partial-silent(
    prefix="#"
) }}
