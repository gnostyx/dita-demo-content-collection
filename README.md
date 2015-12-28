Gnostyx DITA Demonstration Documents
===================================

This project provides a set of DITA documents intended to support DITA demonstrations by providing realistic documents that demonstrate a wide variety of DITA features and use patterns. The base version of the documents were originally developed and contributed by Gnostyx Research (gnostyx.com). Additional variants demonstrating various ways of using keys have been developed Eliot Kimber.

Guide to Scenarios
==================

An introduction to the DITA demonstration collection and a description of the maps and scenarios provided.

Eliot Kimber Updates
--------------------

I have updated this content set to add versions that use keys and key scopes (DITA 1.3)
in ways that reflect various suggested or potential best practices.

- Thunderbird-keys-reuse-only: Puts keys on all references to topics such that there is exactly one URI reference to each topic and each such reference has an associated key. In addition, every navigation topicref has a key. Resource-only keys are defined for all images and for all topics that are used two or more times within the different maps in the information set.

If a topic is used exactly once across all the maps and that use is a navigation topicref (processing-role="normal") then putting a key on the navigation topicref satisfies the requirement to have both exactly one URI reference to the topic and a key associated with every topic. If the topic is used in two or more maps then a resource-only key definition is defined for the topic and put in a separate key definition map. The navigation topicrefs that use the topic refer to the resource-only key, not the the topic's URI.

- Thunderbird-keys-all-resonly: Declares a resource-only key for every topic (and image). All navigation topicrefs have keys and use keyrefs to the topics they place in the publication structure. This version reflects the "resource-only key definitions for every topic" practice, which while useful may be more than many writing teams need or can realistically set up.

In both of these versions of the content, cross references and content references are to always to keys: all references from topics to any kind of resource are key references, including all content references.

For more background on these two key-using versions on the content, see "Reworking the User Guide Map" below.

Introduction
------------

The DITA Demonstration Collection provides a set of sample DITA files that are meant to be used to demonstrate selected capabilities and benefits of DITA . The sample DITA files that have been prepared are intended to provide illustrative DITA content that is both technically valid and functionally realistic. It primary use-case is as a tool for demonstrating the capabilities of DITA to audiences that are interested in the functional benefits that can be achieved by deploying DITA.

The content has been created based on materials produced by various organizations with this content being modified to exclude proprietary details.

The functional objective set for the content itself is that it should be "functionally realistic" without necessarily being a flawless description of an actual system. As a technical objective, the DITA markup is valid and in line with generally accepted DITA markup practices. As a further objective, the DITA markup intentionally includes a range of possible markup and content organization tactics, based on patterns encountered in real-world content sources.

The collection of instances provided as part of this collection is also intended to be broad enough to support the definition and execution of a number of useful demonstration scenarios.

For this initial DITA Demonstration Collection, it was determined that the focus would be placed squarely upon the use and demonstration of core DITA 1.2 features. The DITA Demonstration Collection will be updated and extended over time to reflect newly released DITA features as they become available and as they enter mainstream usage.

Using the Collection
--------------------

The initial DITA Demonstration Collection has been prepared based on a general story that features a software product that facilitates the management of a distributed collection of hardware devices and software components. The fictional system has been called the _StormCluster_ solution which includes a user environment named _MobileView_. This scenario was developed because it makes it possible to illustrate many of the core DITA benefits such as supporting the publication of a range of information products for a variety of user types and across a number of product releases. It also makes it possible to introduce new collections of content that would add new types of content (e.g., hardware documentation, business procedures, and so on).

If there is a governing purpose for the DITA Demonstration Collection, it is to serve as a set of sample files that can be used to demonstrate the capabilities and benefits of different DITA enabled technologies and by extension DITA itself. More generally still, this collection of sample files can be used to introduce stakeholders to the merits of applying carefully designed markup structures to their content assets. It is this purpose that makes the functional realism of the "story" so important. Even where it is not a match to what a given group of stakeholders is interested in directly, it should nonetheless look realistic and credible. In seeking to be this, it is hoped that the story surrounding for _StormCluster_, and its various subcomponents, will support a wide range of demonstration, training, and evaluation scenarios that will be broadly accessible.

One of the key target demonstration scenarios set for the _StormCluster_ collection is to showcase how quickly important details, such as product names or widely used resources (i.e., icons), can be changed and immediately propagated across the entire collection and across all resulting information products. This capability can be used to quickly modify the _StormCluster_ collection to use different company and product names, and to invoke different icons and images, so that in very short order the collection could look more like information produced or used by a given audience.

Licensing Terms
---------------

Copyright 2015 Gnostyx Research Inc.

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.

In line with this license, people are encouraged to use, adapt, extend, and distribute the collection in whatever ways that they see fit. This includes providing this content as part of a commercial offering, for example as reference files within a product tutorial. They are further encouraged, but not obligated, to make their adaptations and extensions available to the public on similar terms.


Acknowledgements
----------------

The initial release of the DITA Demonstration Collection has been sponsored by [Gnostyx Research Inc.](http://www.gnostyx.com) and has been the result of contributions from the following people:

-   Joe Gollner
-   Kelsey Nelson
-   Ian Skeaff
-   Shirin Ahmadzadeh-Shad
-   Kathleen Gollner
-   Tenny Webster
-   James Gollner
-   Jacquie Samuels

The effort to produce this initial release of the DITA Demonstration Collection highlighted a number of important considerations. A key one is that the development of good quality content is very hard work and that this is made even harder when the task of constructing a fictional, but still functionally realistic, story is tossed into the mix. It should be expected that the coherence of the story, and the consistency with which it is realized, will continue to be improved although this claim will need to be measured against the fact that this represents the most challenging aspect of such an undertaking.

Anyone using or reviewing this collection who identifies any issues or who has comments that would point towards the improvement of the collection can forward their observations to Gnostyx Research Inc. ([info@gnostyx.com](mailto:info@gnostyx.com)). These improvement observations can, naturally, include contributions of additional sample instances. This collection will also be deployed on a publically accessible source control service (GitHub) thereby facilitating its collaborative evolution.

Organization of content
-----------------------

All topics, maps, graphics, and ditaval files (to control conditions) are available in one folder.

If it is desireable to test a different situations where files are located in various sibling folders or subfolders, implementers can copy a map, as well as all its topics and graphics, into sibling or sub-folders, then rename the copied map and adding it to the master map.

Note:

Implementers may need to troubleshoot filenames and duplicate reference files for content that has content references.

Variables
---------

Company, product, and features names are controlled through a central file: r\_productname\_variables.dita.

When a company, product, or feature name is included in the content, it is placed in the target file as a conref or conkeyref from the central file (source). This permits the values to be modified, or extended, whenever needed (if the company name changes, product name changes, or feature name changes). Maintaining variables centrally is particularly useful in the case of a collection of test and demonstration instances because it should make it easy to change key names in order, for example, to reflect a particular organizations product names. Implementers making use of the collection, or the team maintaining the collection, may wish to:

-   Modify the names used for the product, company or features in order to tailor the demonstrations to reflect the needs of a given organization.

-   Extend the content collection to include new products or features.

-   Extend the content collection to support scenarios where two or more companies are contributing content to a combined product.

In a similar fashion, an image warehouse topic (r\_image\_warehouse.dita) has been used to hold references to the images being used by the collection.

Guide to the Maps
-----------------


##### The roles of the different Maps provided as part of the DITA Demonstration Collection

|Map|Scenario|
|--------|---------|
|Master Control Map|This map provides a single view of all topics within the collection. It also includes references to background materials that describe the DITA Demonstration Collection and its intended use.|
|_MobileView_ User Map|This map assembles content into a published information product that would be used by customer local administrators accessing and using information services provided by _StormCluster_.|
|Integrator Bookmap|This BookMap includes publication information, such as a list of figures and an index as back matter. This map topics that would be used by an administrator working within an integrator organization instead of a local administrator working within an end-customer organization.|
|Customer Proposal Template Map|A map incorporates content into a template proposal that can be used to demonstrate the sharing of content between documentation sources and business documents.|

_Source: Thunderbird/c_guide_to_scenarios.dita_


How the Key-Based Samples Were Created
--------------------------------------

The key-based samples were created from the original non-key-based (except for the conrefs to the warehouse topics) Thunderbird source. 
The keys were added by using regular expression search and replace with oXygenXML. This was possible because the images and topics
had filenames that were both globally unique within the information set and reflected patterns that worked well for keys. In particular,
the topic files all follow the naming pattern "{c|r|t}_{descriptive name}.dita". This allowed use of the descriptive name part of 
the topic filename as the navigation key for each topic and the full filename (minus the extension) as the resource-only key.

The process followed was roughly:

1. Create a new oXygenXML project and add the dita-demo-content-collection to the project. The project makes it easy to apply
global search and replace to sets of files.

2. Copy the original Thunderbird directory to create the starting point for the new sample files.

3. Create key definition maps for the image files in each of the two image directories (Images/ and Images2/).

4. Rework the conditional topicgroups in the User Guide map to include the new image keydef maps.

5. Add @keys attributes to all the navigation topicrefs in all the navigation maps. 

4. Use global search and replace to change all hrefs to keyrefs in all the topics.

### Creating Key Definition Maps for the Images

The basic technique is:

**Step 1.** Capture the list of files in the image directory to a file. On a unix-type
operating system you can do this with "ls > files.txt". There must be a Windows
equivalent (or you can install the git Windows client and include the git command
window, which provides a basic bash shell environment).

**Step 2.** Edit the files.txt file in oXygen and apply this regular expression 
search and replace:

~~~~
Find:

^(([^\.]+)\.(.+))$

Replace with:

<keydef keys="$2" href="$1" format="$3">
 <topicmeta>
  <navtitle>$1</navtitle>
 </topicmeta>
</keydef>
~~~~
 
The regular expression matches each line of the file, capturing the whole line as group 1, the base
filename as group 2, and the extension as group 3.

The navigation title is necessary because the key is bound to a non-DITA resource and thus
needs an explicit navigation title.

**Step 3.** Add the map DOCTYPE declaration and map start and end elements to make a complete map
document. You can copy the markup from the master_control.ditamap 

~~~~
<!DOCTYPE map PUBLIC "-//OASIS//DTD DITA Map//EN" "map.dtd">
<map>
  <title>Keydefs for Images/ directory</title>
  <topicgroup>
    <topicmeta>
      <navtitle>Images/ directory</navtitle>
    </topicmeta>
~~~~

**Step 4.** Save the file as "keydefs-images.ditamap" in the Images/ directory

**Step 5.** Repeat for the Images2/ directory, calling the file keydefs-images2.ditamap.

### Reworking the User Guide Map

The User Guide map uses warehouse topics to manage conditional references to 
the images, with one version of the warehouse for each product version (STA 
and STB).

The Images/ and Images2/ directories provide product-specific variants of the
graphics, so the two image keydef maps need to be included within the conditional
topicgroups used to define keys for the variables and warehouse topics:

~~~~
<topicgroup product="STA" processing-role="resource-only">
  <mapref href="Images/keydefs-images.ditamap"/>
  <mapref href="Images2/keydefs-images2.ditamap"/>
  <keydef keys="r_productname_variables" href="topics/r_productname_variables.dita" type="topic"
    format="dita"/>    
  <keydef keys="r_image_warehouse" href="topics/r_image_warehouse.dita" type="topic"
    format="dita"/>   
</topicgroup>
<topicgroup product="STB" processing-role="resource-only">
  <mapref href="Images2/keydefs-images2.ditamap"/>
  <mapref href="Images/keydefs-images.ditamap"/>
  <keydef keys="r_productname_variables" href="topics/r_productname_variables_2.dita" type="topic"
    format="dita"/>    
  <keydef keys="r_image_warehouse" href="topics/r_image_warehouse_2.dita" type="topic"
    format="dita"/>   
</topicgroup>
~~~~

Note that both topic groups include both image keydef maps but in opposite orders. This ensures that 
the product-specific key bindings take precedence while still ensuring that any keys defined in
one of the maps but not the other will have definitions regardless of which product is filtered
out.

If all they contained were image elements used by conref, the image warehouse topics could be replaced with a single warehouse as all the key definitionsare now conditional. 
But the image warehouse
also contains figures that then contain images and those figures could be product specific beyond
just the image referenced. Likewise, the image elements could have product-specific alternative text,
so it can still make sense to use a warehouse for the image elements and use them via conref.

The other thing to do for the User Guide map is to add @keys attributes to all the navigation
topicrefs. The navigation topicref keys enable cross references (and ultimately, cross-deliverable
links) to specific uses of topics within the publication. This is essential for reliable cross
referencing. Navigation topicref keys can also be used to control the anchors used in deliverables
(e.g., the filenames of HTML files generated from the referenced topics, as though @copy-to had
been specified on each topicref such that the effective filename reflects the key name).

This can be done with another regular expression search and replace applied to
the navigation topicrefs in the map:

~~~~
Find:

(href="topics/[ctr]_([^\.]+))

Replace with:

keys="$2" $1

XPath:

topichead//topicref
~~~~

The resulting topicrefs should look like this:

~~~~
<topicref keys="mv_managing_messages" href="topics/c_mv_managing_messages.dita"/>
~~~~

The XPath limits the change to only topicrefs under topichead ancestors, which
prevents it from changing topicrefs in the relationship table, which we don't 
want to do.

There is one topic whose filename does not follow the pattern: FAQ.dita.
I solved this problem by changing it's filename to "c_FAQ.dita" (even though
the topic is a generic topic, it functions more or less as a concept) and just
manually changed the topicref to add the @keys attribute with the value "FAQ".

For the relationship tables, we want to replace the @href attributes with the
equivalent @keyref. We don't need @keys on these topicrefs because they
only serve to establish links between topics, they don't put those topics
into any navigation structure, so there would never be a reason to link to
these particular topicrefs.

To change the reltable topicrefs use this regular expression search and replace:

~~~~
Find:

href="topics/[ctr]_([^\.]+).+?"

Replace with:

keyref="$1"

XPath: 

reltable//topicref
~~~~

If you've done this correctly, oXygen should not report any unresolvable key references in the map if the current map is 
selected in the "Root map" field in the oXygen Map Manager view.

### Replacing @href With @keyref on Images

With the keys set up in the User Guide map, I then updated all the topics to use @keyref in place of @href.
The original topics did not have any topic-to-topic cross references, so the only direct URI references
were to images.

This is essentially the same regular expression search and replace used to update to the navigation topicrefs
in the map, but applied to all the topic files using the oXygen project view.

**Step 1.** Select the Project view in oXygen. You should have already added the dita-demo-content-collection directory
to it. If you haven't, so so now.

**Step 2.** In the Project view, navigate to the topics/ directory under the directory that contains the files you're 
modifying. 

**Step 3.** Right click on the topics/ directory and select "Find/Replace in files..."

**Step 4.** For the "Text to find" field enter this regular expression:

~~~~
href="\.\./Image[s]?/([^\.]+)\.[^"]+"
~~~~

If you do "Find all" now you can test the regular expression without worrying about
making any changes. Also, oXygen will remember the expression so the next time
you open the Find/Replace dialog it will be there for you.

**Step 5.** For the "Replace with" field, enter:

~~~~
keyref="$1"
~~~~

**Step 6.** Make sure the "Regular expression" box is checked and the "Make backup files with extension"
box is **unchecked**. Because you're using a git repository you shouldn't need to worry about backups.
Rather, you can commit your current changes before making the global search and replace, making it
easy to revert back to a good state or, if you want to be really disciplined about it, 
create a new temporary ("feature") branch just for this search and replace. With git in use,
the backup files just cause annoyance. (However, I've added .bak to the .gitignore file in 
this project so backup files will not be added to the repository if you do create them).

**Step 7.** In the "XPath" field enter:

~~~~
image
~~~~

**Step 8.** Click "Replace All..."

This will bring up the Replace All dialog. Here you can use the "Preview"
button to see what will be selected and what the change will be if you're
not 100% sure that your setup is correct. Once you've done the preview
you can then click the "Replace All" button to perform the change.

At this point the files should be almost completely keyified. You can
test this by using oXygen's map validator against the User Guide map.
If the map is reported as valid, try generating HTML or an EPUB from the map.
It should work and all the images should show up.

### Setting Up Keys for The External Web Sites

The only remaining direct URI references are to external Web sites. There's
only a few of these and there's no easy way to translate arbitrary URLs into
appropriate keys.

I created a new empty map called "keydefs-external-web-sites.ditamap" to
hold the new keydefs and added a reference to that map from the User Guide
map.

I then did this search across all the topics:

~~~~
href="
~~~~

With an XPath of "xref" to find all the xrefs in all the topics. 

From the search results I then just opened each topic to the xref,
copied the @href attribute to a new keydef in the keydefs map,
made up a key name, set the @scope attribute to "external"
and the @format attribute "html", added an appropriate navigation title
to the keydef for that Web site.

On the original xref I replaced the @href attribute
with @keyref pointing to the key I just defined.

With that task complete, the only URI references should be in map files,
either on dedicated keydef elements or on navigation topicrefs to topics
that are not reused. You can check that by doing a search on "href=" across
all the .dita and .ditamap files in the project. You should only get hits
on .ditamap files.

A more complete check would be to ensure that a given URI is only referenced
once it an given map (or, more dogmatically, in exactly one map), which could
be done with an XQuery the operates on all the files in the project.

With these changes made and validated against the User Guide map, it's then
simply a matter of making the same updates to the other root maps (integrator_admin.ditamap,
master_control.ditamap, and proposal_template.ditamap).

I also changed the filename of the User Guide map to be different from the original
just so that things generated from it would, by default, have a different filename.
This is just to make it easier to compare the results from processing the different
versions of the Thunderbird source files.

### Managing Publications

In anticipation of the DITA 1.3 cross-deliverable linking feature and as an 
experiment in publication management, I also created a new map to serve as
a catalog or declaration of the maps that act as the roots of publications
in this content set.

In the general case, there is no way to know if a given map is intended to be
a root map or a submap. For some maps it's obvious to a human (e.g., a map
containing only keydefs for example) but for other maps it's not: if the map
has a title and has references to topics or other maps, it might be intended
to be a root map or it might not.

One solution to this is to create another map that references the maps you
intend to be root maps as "peer" maps. This map then serves as an explicit
declaration of "root map ness" and could be used, for example, as configuration
for a CCMS or publication management system.

In this example, I created the map "publication-set.ditamap":

~~~~
<!DOCTYPE map PUBLIC "-//OASIS//DTD DITA Map//EN" "map.dtd">
<map>
 <title>Catalog of Publications</title>
  <topicmeta>   
    <shortdesc>This map serves as a list of all the top-level
    publication maps in the content set. Each map is referenced
    using a peer-scope map ref. Per the DITA 1.3 rules, a peer-scope
    map reference means "this map acts as a separate root map",
    in this context, meaning "The root of a publication". This
    map reflects DITA 1.2 and thus does not use the DITA 1.3 @keyscope
    attribute. For DITA 1.3 it would make sense to also put a key scope
    name on each publication, at least to establish the convention
    for the scope name for that publication when used from other maps.
    That would also allow this map to be used from any publication map
    that wanted to enable links to any of the other publications.
    </shortdesc>    
  </topicmeta>
  <topicgroup>
    <mapref href="Integrator_admin.ditamap" scope="peer"/>
    <mapref href="User_Guide-resonly-all-topics.ditamap" scope="peer"/>
    <mapref href="master_control.ditamap" scope="peer"/>
    <mapref href="proposal_template.ditamap" scope="peer"/>
  </topicgroup>
</map>
~~~~

Note that the mapref elements all specify a @scope of "peer". In DITA 1.3,
setting the scope attribute to "peer" for a reference to a DITA map
explicitly means "the referenced map is a root map from the point of view of
this map". That's intended primarily to enable cross-deliverable linking 
(by putting a key scope on the mapref) but it also serves to simply
establish that a given map is considered to be a root map by at least
one other map.

Here I'm establishing the convention that this "publication set" map 
defines the exclusive set of maps I want to treat as root maps in 
this particular information set.

This publiation set map could be used in any number of ways: as a
way for somebody coming to this set of files to know what the 
publication maps are, as a convenience for authors by simply making
it easy to get to the publication root maps. As a convenience for
authoring tools to know which maps they need to construct key 
spaces from for key space resolution. As configuration for a publication
management system to know what maps it needs to maintain cross-deliverable
linking details for, etc.
 



















