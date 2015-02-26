
The Academia Entity Catagory
=======================

1. Overview
----------------

Research and Education Federations are encouraged to use the REFEDS Academia Entity Category to annotate such member identity providers that represents academic institutions in order to distinguish them from identity providers that are not able to claim any affiliation with the international research and education community.

The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED", "MAY", and "OPTIONAL" in this document are to be interpreted as described in RFC 2119 [RFC2119]. This definition is written in compliance with the Entity Category SAML Entity Metadata Attribute Types specification [EntityCatTypes].

2. Definition
----------------

An identity provider MUST NOT be annotated with the academia entity category unless it is being operated by, or on behalf of and by contract with, at least one organisation represented by a legal entity in good standing in the community of other academic institutions and fulfills at least one of the criteria below:

1. the organization is dedicated to education and research and which grants academic degrees at level 6 (or higher) according to ISCED 2011 [ISCED] or equivalent internationally recognized academic degree levels.
2. the organization is a research library or archive
3. the organzation is primarily dedicated to conducting research
4. the organization is a teaching hospital
5. any organization explicitly denoted as an acedemic institution by a goverment entity in the jurisdiction where the claim of being an academic institution is made

Note that the funding mechanism (private, public or mixed) is not a factor in the definition of an academic institution. For instance, privately funded research institutions are eligible for the entity category if they fulfill at least one of the criteria above.

3. Syntax
---------

The following URI is used as the attribute value for the Entity Category and Entity Category Support attribute: http://refeds.org/category/academia

4. Semantics
------------

By asserting an Identity Provider to be a member of the academia entity category a registrar claims that the Identity Provider fulfils the criteria described above in the jurisdiction of the registrar. The intended use for the Entity Category is twofold:

- To allow metadata consumers (eg in a discovery service) to filter on identity providers representing one or more to academic institution
- To allow relying parties an way to decide what value to assign to a claim of the eduPersonScopedAffiliation and eduPersonAffiliation attributes.

Specifically a relying party SHOULD NOT assume that an attribute assertion received from an identity provider with the academia entity category represents a Subject (as defined in [TBD]) with any particular affiliation to the organization on behalf of which the identity provider is operated. Conversely, the absense of the academia category does not mean that the identity provider does not in fact represent one or more academic institution.

5. References
-------------

[ISCED] ISCED 2011, http://www.uis.unesco.org/ISCED

[AcademicInstitutionWikipedia] http://en.wikipedia.org/wiki/Academic_institution

[EntityCatTypes] Young, I, Johansson, L, and Cantor, S Ed., "The Entity Category SAML Attribute Types", July 2014.

[RFC2119] Bradner, S., "Key words for use in RFCs to Indicate Requirement Levels", BCP 14, RFC 2119, March 1997.

[TBD] insert saml reference here for Subject
