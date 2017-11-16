
The Academic Institution Entity Category
=======================

1. Overview
----------------

Research and Education Federations are encouraged to use the REFEDS Academic Institution Entity Category to annotate those member Identity Providers that are trusted to assert academically-orientated data about their users, in order to distinguish them from Identity Providers that are not able to claim any affiliation with the international research and education community.

The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED", "MAY", and "OPTIONAL" in this document are to be interpreted as described in RFC 2119 [RFC2119]. This definition is written in compliance with the Entity Category SAML Entity Metadata Attribute Types specification [EntityCatTypes].

2. Definition
----------------

In order to be annotated with the Academic Institution Entity Category, an Identity Provider MUST be managed by (or on behalf of and by contract or other written agreement with) at least one academic institution. 

Such an academic organisation MUST be represented by a legal entity in good standing in the community of other academic institutions, fulfilling at least one of the criteria below:

1. the institution is dedicated to education and research and which grants academic degrees at level 5 (or higher) according to ISCED 2011 [ISCED] or equivalent internationally recognised academic degree levels.
2. the institution is a teaching hospital working with health professionals studying at level 5 (or higher) according to ISCED 2011 [ISCED] or equivalent internationally recognised academic degree levels.
3. the institution is a research library or archive.
4. the institution is primarily dedicated to conducting research.
5. the institution is explicitly denoted as an academic institution by a government entity government entity or recognised accrediting body in the jurisdiction where the claim of being an academic institution is made.

Note that the funding mechanism (private, public or mixed) is not a factor in the definition of an academic institution. For instance, privately funded research institutions are eligible for this entity category if they fulfil at least one of the criteria above.

3. Syntax
---------

The following URI is used as the attribute value for the Entity Category and Entity Category Support attribute: http://refeds.org/category/academic_institution


4. Semantics
------------

By asserting that an Identity Provider is a member of the Academic Institution Entity Category a registrar claims that the Identity Provider fulfils the criteria described above in the jurisdiction of the registrar. 

Specifically a relying party SHOULD NOT assume that an attribute assertion received from an Identity Provider with the Academic Institution Entity Category represents a Subject (as defined in [SAMLCore]) with any particular affiliation to the institution on behalf of which the Identity Provider is operated.  eduPersonScopedAffiliation MUST be used to determine the affiliation status of users. 

Conversely, the absence of the Academic Institution Entity Category does not mean that the Identity Provider does not in fact represent one or more academic institutions.

5.  Registration Criteria
-------------

When an Identity Provider’s registrar (normally the Identity Provider’s home federation) registers the Identity Provider in the Academic Institution Entity Category, the registrar MUST perform at least the following checks:

5.1 The Identity Provider meets the definition outlined in section 2 above.

5.2 Identity Provider metadata has been submitted to the registrar for publication.

5.3 The Identity Provider meets the following technical criteria: 

5.3.1 The Identity Provider provides a unique mdui:DisplayName in metadata (an english language version xml:lang=”en” is RECOMMENDED).

5.3.2 The mdui:DisplayName accurately reflects the organisation in question.

5.3.3 The Identity Provider releases the eduPersonScopedAffiliation attribute.

Academia Identity Providers MUST resolve issues of non-compliance within a reasonable period of time from when they become aware of the issue. Failure to do so MUST result in revocation of the entity’s membership in the category.


6. References
-------------

[ISCED] ISCED 2011, http://uis.unesco.org/en/topic/international-standard-classification-education-isced.

[AcademicInstitutionWikipedia] http://en.wikipedia.org/wiki/Academic_institution.

[eduPerson] Internet2 MACE Directory Working Group, “eduPerson Object Class Specification (201602)”, February 2016.

[EntityCatTypes] Young, I, Johansson, L, and Cantor, S Ed., "The Entity Category SAML Attribute Types", July 2014.

[RFC2119] Bradner, S., "Key words for use in RFCs to Indicate Requirement Levels", BCP 14, RFC 2119, March 1997.

[SAMLCore] S. Cantor et al., "Assertions and Protocols for the OASIS Security Assertion Markup Language (SAML) V2.0", OASIS SSTC, March 2005, Document ID samlcore-2.0-os. See http://www.oasis-open.org/committees/security/.
