# Simple Content Stores

<table width="100%">
    <tr>
        <td width="120">Developer:</td>
        <td>Axel Faust</td>
        <td colspan="2"></td>
    </tr>
    <tr>
        <td width="120">Release:</td>
        <td>No release yet</td>
        <td width="120">Release date:</td>
        <td></td>
    </tr>
    <tr>
        <td width="120">Type:</td>
        <td>Extension for Repository</td>
        <td width="120">Packaging:</td>
        <td>AMP</td>
    </tr>
    <tr>
        <td width="120">Public listing:</td>
        <td colspan="3">No listing yet</td>
    </tr>
    <tr>
        <td width="120">Source hosting:</td>
        <td><a href="https://github.com/AFaust/simple-content-stores">GitHub AFaust/simple-content-stores</a></td>
        <td width="120">Source license:</td>
        <td><a href="https://www.eclipse.org/legal/epl-v10.html">Eclipse Public License 1.0</a></td>
    </tr>
    <tr>
        <td width="120">Reviewer:</td>
        <td>Axel Faust</td>
        <td width="120">Review date:</td>
        <td>2016-10-22</td>
    </tr>
    <tr>
        <td>Criteria catalog:</td>
        <td colspan="3"><a href="https://github.com/OrderOfTheBee/addons/wiki/Inclusion-criteria-overview">Criteria overview</a> (state of 2015-01-06)</td>
    </tr>
</table>

Review result: FAIL - mandatory prerequisites not met

## General notes

No | Note | Reference
--: | ---- | ---------
 |  | 

## Criteria notes

This segment lists all notes / issues / violations of inclusion criteria found during the review. Any item of the [criteria catalog](https://github.com/OrderOfTheBee/addons/wiki/Inclusion-criteria-overview) not mentioned in this section is presumed to be matched sufficiently for inclusion in the OOTB addon listing.

Class | No | Category | [Type](https://github.com/OrderOfTheBee/addons/wiki/General-guidelines#requirement-relevance-types) | Note
----- | --: | -------- | :----- | ----
Non-technical | 5 | [State](https://github.com/OrderOfTheBee/addons/wiki/Non-technical-inclusion-criteria#state) | must | no public release yet
Non-technical | 6 | [State](https://github.com/OrderOfTheBee/addons/wiki/Non-technical-inclusion-criteria#state) | must | undertermined due to "no public release yet"
Non-technical | 7 | [Publication](https://github.com/OrderOfTheBee/addons/wiki/Non-technical-inclusion-criteria#publication) | must | not listed yet but committed to list
Non-technical | 8 | [Publication](https://github.com/OrderOfTheBee/addons/wiki/Non-technical-inclusion-criteria#publication) | must | no information about nature of addon, release state and minimal compatible version
Non-technical | 10 | [Documentation](https://github.com/OrderOfTheBee/addons/wiki/Non-technical-inclusion-criteria#documentation) | must | documentation on general usage exists - might be improved in terms of structuring / use case examples
Technical | 7 | [Artifacts](https://github.com/OrderOfTheBee/addons/wiki/Technical-inclusion-criteria#packaging--artifacts) | must not | requires build from source due to lack of release
Technical | 15 | Configuration | must not | addon overrides Spring config of contentService - must be explicitly enabled by system administrator (acceptable way to override)
Technical | 17 | Configuration | should | extensive addon-specific properties provided for configuration
Technical | 20 | API | should | deliberate use of Java API not part of the Public API (unavoidable due to low-level nature)

## Compatibility

This segments lists all notes regarding compatibility of the addon with Alfresco, 3rd-party addons or client environments.

Compatible with | Version | Notes
--- | --- | ---
Alfresco | Community 5.1.g | 

## Mandatory tasks

1. Provide official beta / stable release
2. List on addons.alfresco.com

## Suggested tasks

1. Improve documentation structure