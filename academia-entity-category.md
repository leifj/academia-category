
The Academia Entity Category
=======================

1. Overview
----------------

Research and Education Federations are encouraged to use the REFEDS Academia Entity Category to annotate those member Identity Providers that represent academic institutions, in order to distinguish them from Identity Providers that are not able to claim any affiliation with the international research and education community.

The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED", "MAY", and "OPTIONAL" in this document are to be interpreted as described in RFC 2119 [RFC2119]. This definition is written in compliance with the Entity Category SAML Entity Metadata Attribute Types specification [EntityCatTypes].

2. Definition
----------------

In order to be annotated with the Academia Entity Category, an Identity Provider MUST be managed by (or on behalf of and by contract or other written agreement with) at least one academic institution. 

Such an academic organisation MUST be represented by a legal entity in good standing in the community of other academic institutions, fulfilling at least one of the criteria below:

1. the institution is dedicated to education and research and which grants academic degrees at level 6 (or higher) according to ISCED 2011 [ISCED] or equivalent internationally recognised academic degree levels.
2. the institution is a teaching hospital working with health professionals studying at level 6 (or higher) according to ISCED 2011 [ISCED] or equivalent internationally recognised academic degree levels.
3. the institution is a research library or archive.
4. the institution is primarily dedicated to conducting research.
5. the institution is explicitly denoted as an academic institution by a government entity government entity or recognised accrediting body in the jurisdiction where the claim of being an academic institution is made.

Note that the funding mechanism (private, public or mixed) is not a factor in the definition of an academic institution. For instance, privately funded research institutions are eligible for this entity category if they fulfil at least one of the criteria above.

3. Syntax
---------

The following URI is used as the attribute value for the Entity Category and Entity Category Support attribute: http://refeds.org/category/academia

4. Semantics
------------

By asserting that an Identity Provider is a member of the academia entity category a registrar claims that the Identity Provider fulfils the criteria described above in the jurisdiction of the registrar. The intended use for the entity category is twofold:

- To allow metadata consumers (e.g. a discovery service) to filter on Identity Providers representing one or more academic institutions.
- To allow relying parties a way to decide how to interpret the values of the eduPersonScopedAffiliation and eduPersonAffiliation attributes.

Specifically a relying party SHOULD NOT assume that an attribute assertion received from an Identity Provider with the academia entity category represents a Subject (as defined in [SAMLCore]) with any particular affiliation to the institution on behalf of which the Identity Provider is operated. 

Conversely, the absence of the academia category does not mean that the Identity Provider does not in fact represent one or more academic institutions.

5. References
-------------

[ISCED] ISCED 2011, http://uis.unesco.org/en/topic/international-standard-classification-education-isced

[AcademicInstitutionWikipedia] http://en.wikipedia.org/wiki/Academic_institution

[EntityCatTypes] Young, I, Johansson, L, and Cantor, S Ed., "The Entity Category SAML Attribute Types", July 2014.

[RFC2119] Bradner, S., "Key words for use in RFCs to Indicate Requirement Levels", BCP 14, RFC 2119, March 1997.

[SAMLCore] S. Cantor et al., "Assertions and Protocols for the OASIS Security Assertion Markup Language (SAML) V2.0", OASIS SSTC, March 2005, Document ID samlcore-2.0-os. See http://www.oasis-open.org/committees/security/.
