# Profile for DefinedTerm

The two SchemaOrg types DefinedTerm and DefinedTermSet
are allowed in many places as property values.

In e.g. the life-sciences, there are a number of controlled vocabularies
and ontologies, which are often used as source of the DefinedTerms.
Many of the, can be browsed and accessed through terminology and lookup services or portals.

For linked data applications it is sufficient for an entity
with `@type="DefinedTerm"` to link to an `@id` pointing to the IRI
of the referenced concept.

In other cases, more information is needed to search and view defined term information
without having to lookup external resources. E.g., a domain-specific search engine
can create faceted search based on the `name` property, like e.g. done in TeSS.
Aforementioned terminology services also offer linking and query interfaces
beyond IRIs as parameters.

Another possible use of a conformant `DefinedTerm`
is to enable creating hyperlinks to other web ressources, e.g.
https://bio.tools/t?inputDataFormatID=%22format_3244%22
or provide tool-tips if the `description` is provided.

Some typical OBO ontologies can be taken as inspiration of properties that should be
required or recommended in a Bioschema DefinedTerm profile. We also provide
some mapping information between properties of `DefinedTerm`
and those from OBO, OWL and SKOS, following work in https://doi.org/10.1186/2041-1480-2-S1-S3.

It is not intended to duplicate the content and expressivity
of powerful ontology representations and serialisations like OWL or RDF.

# Profile for DefinedTermSet

Properties of controlled vocabulary available through terminology and lookup services
or portals can be de captured in the `DefinedTermSet` profile.

There are also cases where controlled vocabulary are not available through
terminology and lookup services or portals and which are not formalized
into an ontology. In such cases, there may not be a suitable IRI and additional
information would be needed. Eg- The ClinicalTrials.gov's
Protocol Registration and Results System (PRS) Schema
has controlled vocabulary used as values for many properties but these terms
are not necessarily in a formal ontology. In this case, it is important
to leverage the `DefinedTermSet` profile to ensure sufficient information
is included for provenance.
