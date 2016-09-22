# Site Logo Customization for Alfresco Share

<table width="100%">
    <tr>
        <td width="120">Developer:</td>
        <td>Alex Yu-Kuang Lu, Douglas C. R. Paes and Bhagya Silva</td>
        <td colspan="2"></td>
    </tr>
    <tr>
        <td width="120">Release:</td>
        <td><a href="https://github.com/douglascrp/alfresco-share-site-logo-customization/releases/tag/3.0">3.0</a></td>
        <td width="120">Release date:</td>
        <td>2016-08-19</td>
    </tr>
    <tr>
        <td width="120">Type:</td>
        <td>Extension for Repository / Share</td>
        <td width="120">Packaging:</td>
        <td>AMP</td>
    </tr>
    <tr>
        <td width="120">Public listing:</td>
        <td colspan="3"><a href="https://addons.alfresco.com/addons/share-site-logo-customisation">addons.alfresco.com/addons/share-site-logo-customisation</a></td>
    </tr>
    <tr>
        <td width="120">Source hosting:</td>
        <td><a href="https://github.com/douglascrp/alfresco-share-site-logo-customization">GitHub douglascrp/alfresco-share-site-logo-customization</a></td>
        <td width="120">Source license:</td>
        <td>Apache License 2.0</td>
    </tr>
    <tr>
        <td width="120">Reviewer:</td>
        <td>Douglas C. R. Paes</td>
        <td width="120">Review date:</td>
        <td>2016-09-12</td>
    </tr>
    <tr>
        <td>Criteria catalog:</td>
        <td colspan="3"><a href="https://github.com/OrderOfTheBee/addons/wiki/Inclusion-criteria-overview">Criteria overview</a> (state of 2015-01-06)</td>
    </tr>
</table>

<p><span style="font-size:150%;">Review result: </span><span class="label labelstyle-159818 linked-labelstyle-159818 lightertooltipped" style="background-color: #159818; color: #fff;">PASS</span> (only trivial issues)</p>

## General notes

No | Note | Reference
--: | ---- | ---------
 1 | Apache License is not applied correctly | [Apache License 2.0](http://www.apache.org/licenses/LICENSE-2.0)

## Criteria notes

This segment lists all notes / issues / violations of inclusion criteria found during the review. Any item of the [criteria catalog](https://github.com/OrderOfTheBee/addons/wiki/Inclusion-criteria-overview) not mentioned in this section is presumed to be matched sufficiently for inclusion in the OOTB addon listing.

Class | No | Category | [Type](https://github.com/OrderOfTheBee/addons/wiki/General-guidelines#requirement-relevance-types) | Note | 
----- | --: | -------- | :----- | ----
Non-technical | 8 | [Publication](https://github.com/OrderOfTheBee/addons/wiki/Non-technical-inclusion-criteria#public-listing) | must | Details on addons.alfresco.com listing very limited and outdated (minimal supported versions, project link)
Non-technical | 10 | [Documentation](https://github.com/OrderOfTheBee/addons/wiki/Non-technical-inclusion-criteria#documentation) | must | Insufficient documentation on general usage
Technical | 32 | Configuration | should | Repository module should not use "extension" path for web scripts (which prevents overrides by end user / customer)
Technical | 22 | API |  must | Repository extension	use runAs() instead of unsecured private service beans to execute code with elevated privileges or as substitute for other users (implemented as javascript and webscript runas configure as admin)
Technical | 23 | API | must not | Extension	require existence of super user called "admin" (e.g. runAs(work, "admin"))

## Compatibility

This segments lists all notes regarding compatibility of the addon with Alfresco, 3rd-party addons or client environments.

Compatible with | Version | Notes
--- | --- | ---
Alfresco | Community 5.1.x | tested by reviewer
Alfresco | Community 5.0.x | tested by reviewer
Alfresco | Community 4.2.f | tested by reviewer
Firefox | 48 | tested by reviewer
Chromium | 52.0.2743.116 | tested by reviewer
Internet Explorer | 10 | tested by reviewer
Internet Explorer | 11 | tested by reviewer

## Suggested tasks

1. Update addons.alfresco.com listing to add most recent Alfresco versions
2. Correct license application within project
3. Minor re-organisation of configuration