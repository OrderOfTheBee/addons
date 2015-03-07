# Uploader Plus

<table width="100%">
    <tr>
        <td width="120">Developer:</td>
        <td>Paolo Predonzani (SoftwareLoop), Douglas C. R. Paes and contributors</td>
        <td colspan="2"></td>
    </tr>
    <tr>
        <td width="120">Release:</td>
        <td><a href="https://github.com/softwareloop/uploader-plus/releases/tag/v1.2">1.2</a></td>
        <td width="120">Release date:</td>
        <td>2015-02-12</td>
    </tr>
    <tr>
        <td width="120">Type:</td>
        <td>Extension for Repository / Share</td>
        <td width="120">Packaging:</td>
        <td>AMP</td>
    </tr>
    <tr>
        <td width="120">Public listing:</td>
        <td colspan="3"><a href="https://addons.alfresco.com/addons/uploader-plus">addons.alfresco.com/uploader-plus</a></td>
    </tr>
    <tr>
        <td width="120">Source hosting:</td>
        <td><a href="https://github.com/softwareloop/uploader-plus">GitHub softwareloop/uploader-plus</a></td>
        <td width="120">Source license:</td>
        <td>LGPL 3</td>
    </tr>
    <tr>
        <td width="120">Reviewer:</td>
        <td>Axel Faust (Angel Borroy informal review)</td>
        <td width="120">Review date:</td>
        <td>2015-03-07 (2014-11-16)</td>
    </tr>
    <tr>
        <td>Criteria catalog:</td>
        <td colspan="3"><a href="https://github.com/OrderOfTheBee/addons/wiki/Inclusion-criteria-overview">Critieria overview</a> (state of 2015-01-06)</td>
    </tr>
</table>

<p><span style="font-size:150%;">Review result: </span><span class="label labelstyle-159818 linked-labelstyle-159818 lightertooltipped" style="background-color: #159818; color: #fff;">RESULT PENDING</span> (single significant issue)</p>

## General notes

No | Note | Reference
--: | ---- | ---------
 1 | Available on Maven Central as of version 1.2 | [uploader-plus on search.maven.org](http://search.maven.org#search|ga|1|uploader-plus)
 2 | Good coverage of documentation via blog posts - Introduction, Installation, Configuration and even working with custom types and compatibility tests |
 3 | Custom code is (apart from "(web-)extension" overrides) contained in custom packages but lacks identifiable namespacing in some cases, specifically in web script package and client resource paths. Namespacing is not yet part of criteria catalog but may be added in the future. |  

## Criteria notes

This segment lists all notes / issues / violations of inclusion criteria found during the review. Any item of the [criteria catalog](https://github.com/OrderOfTheBee/addons/wiki/Inclusion-criteria-overview) not mentioned in this section is presumed to be matched sufficiently for inclusion in the OOTB addon listing.

Class | No | Category | [Type](https://github.com/OrderOfTheBee/addons/wiki/General-guidelines#requirement-relevance-types) | Note | 
----- | --: | -------- | :----- | ----
Technical | 32 | Configuration | should | Repository and Share modules override upload backend web script and *.get.html.ftl of DnD, Flash and HTML upload component, and also provide custom web scripts and default web-client-config-custom.xml via "(web-)extension". This prevents customization/configuration by end user / customer via shared/classes and may conflict with other addons. It could also introduce regression issues for end users / customers when the web script provided by the addon does not include the fixes of the end users / customers actual Alfresco version, e.g. for Enterprise releases / service packs.

## Compatibility

This segments lists all notes regarding compatibility of the addon with Alfresco, 3rd-party addons or client environments.

Compatible with | Version | Notes
--- | --- | ---
Alfresco | Enterprise 5.0.0 | tested by reviewer - upload.post.js of addon effectively reverts Alfresco bug fixes
Alfresco | Enterprise 4.2.x | tested by reviewer - upload.post.js of addon effectively reverts Alfresco bug fixes (e.g. MNT-12565)
Alfresco | Community 4.2.f | tested by reviewer
Firefox | 36.0.1 | tested by reviewer
Internet Explorer | 11 | tested by reviewer (Alfresco Enterprise 4.2.1 / Community 5 or later)

## Suggested tasks

1. Convert Share uploader overrides to distinct custom uploaders (e.g. "SoftwareLoop.DNDUpload").
1.1. Extend from Alfresco uploaders instead of hitching them
1.2. Use extension module to add custom uploader components to document library via sub-component or customization mechanism (advantage of customization mechanism: less duplication and i18n reuse - sub-component has better isolation from Alfresco changes though)
1.3. Use a customization or sub-component in extension module to set custom uploaders via setOptions()-operation on Alfresco.getFileUploadInstance() singleton
2. Use an upload backend web script distinct from the Alfresco one and call this from custom Share uploader
3. Allow for selective (de-)activation of Uploader Plus during runtime (modules management) or on a per-site basis by Site Manager
4. Move all custom web scripts from "(web-)extension" into regular folders, so end users / customers are able to override
5. Provide custom web client configuration in file that does not conflict with default name web-client-config-custom.xml (custom file may be loaded via a custom ConfigBootstrap bean)
6. Move all module specific Repository-tier configuration and model files into a path based on module, e.g. alfresco/module/uploader-plus-repo/