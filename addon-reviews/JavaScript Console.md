# JavaScript Console

<table width="100%">
    <tr>
        <td width="120">Developer:</td>
        <td>Florian Maul, Jens Goldhammer + contributors</td>
        <td colspan="2"></td>
    </tr>
    <tr>
        <td width="120">Release:</td>
        <td><a href="https://github.com/share-extras/js-console/releases/tag/v0.6.0-rc1">0.6.1-rc1</a></td>
        <td width="120">Release date:</td>
        <td>2013-10-22</td>
    </tr>
    <tr>
        <td width="120">Type:</td>
        <td>Repository / Share extension</td>
        <td width="120">Packaging:</td>
        <td>AMP</td>
    </tr>
    <tr>
        <td width="120">Public listing:</td>
        <td colspan="3"><a href="https://addons.alfresco.com/addons/javascript-console">addons.alfresco.com/javascript-console</a></td>
    </tr>
    <tr>
        <td width="120">Source hosting:</td>
        <td><a href="https://github.com/share-extras/js-console">GitHub share-extras/js-console</a></td>
        <td width="120">Source license:</td>
        <td>Apache License</td>
    </tr>
    <tr>
        <td width="120">Reviewer:</td>
        <td>Axel Faust</td>
        <td width="120">Review date:</td>
        <td>2015-01-06</td>
    </tr>
    <tr>
        <td>Criteria catalog:</td>
        <td colspan="3"><a href="https://github.com/OrderOfTheBee/addons/wiki/Inclusion-criteria-overview">Critieria overview</a> (state of 2015-01-06)</td>
    </tr>
</table>

<p><span style="font-size:150%;">Review result:</span><span style="color:green;font-size:150%;">PASS</span> (only trivial issues)</p>

## General notes

No | Note | Reference
--: | ---- | ---------
 1 | Apache License is not applied correctly - license is only stated in the addons.alfresco.com listing and included in only a single source file | [Apache License 2.0](http://www.apache.org/licenses/LICENSE-2.0)

## Criteria notes

This segment lists all notes / issues / violations of inclusion criteria found during the review. Any item of the [criteria catalog](https://github.com/OrderOfTheBee/addons/wiki/Inclusion-criteria-overview) not mentioned in this section is presumed to be matched sufficiently for inclusion in the OOTB addon listing.

Class | No | Category | [Type](https://github.com/OrderOfTheBee/addons/wiki/General-guidelines#requirement-relevance-types) | Note | 
----- | --: | -------- | :----- | ----
Non-technical | 5 | [State](https://github.com/OrderOfTheBee/addons/wiki/Non-technical-inclusion-criteria#state) | must | Current release has been marked as a "Release Candidate" for 15+ months - effectively a public "production"
Non-technical | 8 | [Publication](https://github.com/OrderOfTheBee/addons/wiki/Non-technical-inclusion-criteria#public-listing) | must | Details on addons.alfresco.com listing very limited and outdated (minimal supported versions, project link)
Technical | 13 | Configuration | must | Repository module should use "module" instead of "extension" path for Spring context and model configuration
Technical | 32 | Configuration | should | Repository module should not use "extension" path for web scripts (which prevents overrides by end user / customer)
Technical | 17 | Configuration | should | Repository moudule might want to allow configuration of pre-/post-roll scripts via Addon properties (or inline into Java source)
Technical | 21 | API | should | Repository module uses non-public bean variant for TransactionService (non-critical due to simple alias of TransactionService=transactionService)
Compatibility | 2 | Alfresco | must not | Module itself does not use EoL'ed features, but provides console templates to use Lucene

## Suggested tasks

1. Update addons.alfresco.com listing - potentially de-activate [old project site](https://code.google.com/p/share-extras/wiki/JavascriptConsole)
2. Correct license application within project
3. Minor re-organisation of configuration
4. Remove reference to EoL'ed components