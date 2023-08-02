# Workflows

There are several dimensions to this project, and one is logistical: the
workflows that guide production from title selection through ingestion.

**Scenario:** a curator has a newspaper or periodical title and wants it
\"digitized\" and made available to patrons.

## Assessment

-   Is there a Catalog record?
-   Have rights been determined?
-   Is the run complete or incomplete?
-   Paper originals or microfilm?
-   Dimensions?
-   Is there in-house language expertise to handle it?
-   How large is the run, in terms of volumes, issues, and pages?

## Options

Outsource everything.

:   Send paper copies or microfilm to an established vendor for imaging,
    and send the digital images to DDD for processing into METS/ALTO
    data. This is how *The Daily Princetonian* was digitized.
    Establishing open-ended contracts with vendors and carefully
    formulated workflows would make it much simpler than it has been.

Outsource metadata creation.

:   Scan the pages in-house and send them to DDD for processing into
    METS/ALTO data at NDNP standards (see
    <https://www.loc.gov/ndnp/guidelines/>).

Do everything in-house.
:   Scan the pages in-house and generate bare-bones METS/ALTO metadata
    through fully automated processes, akin to those now used to ingest
    objects into Figgy from the Digital Studio.

Which option to choose depends on several factors including importance
of the material and cost.

## Metadata

Blue Mountain set a very high standard, making extensive use of the MODS
schema to express field values (titles, creators, publishers,
identifiers, etc.) and relationships (constituent-whole relationships),
and the METS Structmap to knit together segments of text and image
produced through zoning and high-accuracy OCR correction. The newspapers
in the Papers of Princeton collection are of similar quality, although
the constituent-level metadata is extracted automatically from zoned
headlines.

Blue Mountain was a research project, however, and its level of detail
cannot be sustained in ordinary library practice. Stakeholders should
expect no metadata that cannot be derived from existing catalog records,
which for newspapers and periodicals are notoriously poor, and which are
unlikely to be improved or enhanced for digitization. A \"first do no
harm\" approach will be best.

# Scenario 3: Do Everything In-House

The assessment phase remains the same.

## Title Level

### Descriptive

### Structural

## Issue Level

### Descriptive

### Structural

# From METS/ALTO to Manifest

The IIIF Presentation API is framework derived from the [Shared Canvas
data model](https://iiif.io/api/model/shared-canvas/1.0/) which was, in
turn, developed to describe digital facsimiles using a linked-data
approach. The Shared Canvas data model has been absorbed into the IIIF
Presentation API and, it seems, abandoned for its set of Resources,
which are focused on presentation, not description. The IIIF Manifest is
not a substitute for descriptive or structural metadata. Rather, it is a
*transmission standard* for conveying information about digital files
(image files, primarily) to programs that can present those files to a
user (on a screen, for example, in the case of image files).

Generating IIIF Manifests from METS/ALTO data is relatively
straightfoward; see Blue Mountain Springs.
