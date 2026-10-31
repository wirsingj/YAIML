<!-- yaiml-revision: 0.51.76d4cca6ae474b9c -->
# Draw.io Authoring Notes

Create uncompressed XML for reviewable edits. The native structure is `mxfile / diagram / mxGraphModel / root`; use a unique page ID, root cell `0` and layer `1`. Give shapes explicit positive bounds and connectors real endpoint IDs. Start with simple shapes and a single reading direction.

```xml
<mxfile>
  <diagram id="overview" name="Overview">
    <mxGraphModel page="1" pageWidth="900" pageHeight="600">
      <root>
        <mxCell id="0"/>
        <mxCell id="1" parent="0"/>
        <mxCell id="subject" value="Subject" vertex="1" parent="1"
          style="rounded=0;whiteSpace=wrap;html=0;">
          <mxGeometry x="40" y="40" width="180" height="70" as="geometry"/>
        </mxCell>
      </root>
    </mxGraphModel>
  </diagram>
</mxfile>
```

Use an XML serializer or correctly escape attribute values, including ampersands and quotes. Prefer plain labels (`html=0`); avoid embedding source text as HTML. Connectors use `edge="1"`, `source` and `target`, with `<mxGeometry relative="1" as="geometry"/>`. Leave space for wrapped labels and edge labels.

An `object` wrapper can carry `id`, `label`, and descriptive data such as `evidence`, `source` and `sourceRevision`; its child `mxCell` then omits `id` and `value`. These fields are optional provenance, not a YAIML schema. Keep source paths relative and exclude private values.

Existing files may contain compressed pages, nested groups, custom data or multiple layers. Use a capable local reader or preserve them untouched; never replace unreadable content with a new blank graph. Do not flatten an existing file into this minimal example.

Before opening an existing file, inspect for external media/fonts or action links. A local editor can still fetch referenced assets. Do not activate links or fetch those dependencies without authorization; preserve the content and report a rendering limit when necessary. Parse XML without resolving external entities.

Check each page, reference integrity, parent cycles and geometry appropriate to each element. Bounded shapes need usable dimensions; relative edge-label vertices may legitimately omit width/height. Preserve intentional point geometry rather than rejecting or resizing it. Check referenced endpoints when present; an existing free connector may instead use explicit source/target points. These are not missing-cell references.

An XML parse alone establishes neither draw.io compatibility nor accurate project meaning. Opening/rendering with an existing local draw.io installation can check compatibility and layout; disclose when it was not available. Do not require that installation for adoption.

Format reference: [draw.io file structure](https://github.com/jgraph/drawio/wiki/File-Format). The format details above are included for offline authoring; reading the external page is optional. For existing local export tooling, consult its own help rather than assuming a particular executable path.
