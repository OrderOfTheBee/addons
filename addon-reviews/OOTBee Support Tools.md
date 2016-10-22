# OOTBee Support Tools

<table width="100%">
    <tr>
        <td width="120">Developer:</td>
        <td>Axel Faust, Markus Joos</td>
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
        <td><a href="https://github.com/AFaust/ootbee-support-tools">GitHub AFaust/ootbee-support-tools</a></td>
        <td width="120">Source license:</td>
        <td><a href="http://www.gnu.org/licenses/lgpl-3.0.html">LGPL v3.0</a></td>
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
Non-technical | 10 | [Documentation](https://github.com/OrderOfTheBee/addons/wiki/Non-technical-inclusion-criteria#documentation) | must | no documentation on installation, configuration or general usage
Technical | 7 | [Artifacts](https://github.com/OrderOfTheBee/addons/wiki/Technical-inclusion-criteria#packaging--artifacts) | must not | requires build from source due to lack of release
Technical | 20 | API | should | very limited, deliberate access to Java API not part of the Public API (acceptable due to nature of addon)
Technical | 21 | API | should | very limited use of private Alfresco service beans (acceptable due to nature of addon)
Technical | 28 | Misc / Java | must not | very limited direct manipulation of threads (acceptable in context: hot-threads.lib.js)

## Compatibility

This segments lists all notes regarding compatibility of the addon with Alfresco, 3rd-party addons or client environments.

Compatible with | Version | Notes
--- | --- | ---
Alfresco | Community 5.1.g | 
Alfresco | Community 5.0.d | 
Firefox | 48 | 
Edge | 38 | 
Chrome | 54 | 

## Mandatory tasks

1. Provide official beta / stable release
2. Provide documentation about usage
3. List on addons.alfresco.com