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
        **TODO**
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
Non-technical | 5 | [State](https://github.com/OrderOfTheBee/addons/wiki/Non-technical-inclusion-criteria#state) | must | Current release has been marked as a "Release Candidate" for 15+ months - effectively a public "production"
Non-technical | 8 | [Publication](https://github.com/OrderOfTheBee/addons/wiki/Non-technical-inclusion-criteria#public-listing) | must | Details on addons.alfresco.com listing very limited and outdated (minimal supported versions, project link)
Technical | 11 | Build | must | Build from source of tag 0.6.0-rc1 succeeds (criteria fulfilled), but current master fails due to [issue#30](https://github.com/share-extras/js-console/issues/30) |
Technical | 13 | Configuration | must | Repository module should use "module" instead of "extension" path for Spring context and model configuration
Technical | 32 | Configuration | should | Repository module should not use "extension" path for web scripts (which prevents overrides by end user / customer)
Technical | 17 | Configuration | should | Repository module might want to allow configuration of pre-/post-roll scripts via Addon properties (or inline into Java source)
Technical | 21 | API | should | Repository module uses non-public bean variant for TransactionService (non-critical due to simple alias of TransactionService=transactionService)
Compatibility | 2 | Alfresco | must not | Module itself does not use EoL'ed features, but provides console templates to use Lucene

## Compatibility

This segments lists all notes regarding compatibility of the addon with Alfresco, 3rd-party addons or client environments.

Compatible with | Version | Notes
--- | --- | ---
Alfresco | Enterprise 5.0.0 | tested by reviewer
Alfresco | Community 5.0.c | tested by douglascrp (discussed via #alfresco on IRC)
Alfresco | Enterprise 4.2.x | tested by reviewer
Alfresco | Community 4.2.f | tested by reviewer
Alfresco | Community / Enterprise 4.0 | | API and configuration compatible (document list actions)
Firefox | 34.0.5 | tested by reviewer
Internet Explorer | 10 | tested by reviewer
Internet Explorer | 11 | tested by reviewer (Alfresco Enterprise 4.2.1 / Community 5 or later)

Note: IE 8 is not compatible / supported in any combination with Alfresco, unless [issue#24](https://github.com/share-extras/js-console/issues/24) is addressed.

## Suggested tasks

1. Update addons.alfresco.com listing - potentially de-activate [old project site](https://code.google.com/p/share-extras/wiki/JavascriptConsole)
2. Correct license application within project
3. Minor re-organisation of configuration
4. Remove reference to EoL'ed components
5. Remove reliance on running SOLR - [issue#21](https://github.com/share-extras/js-console/issues/21)
