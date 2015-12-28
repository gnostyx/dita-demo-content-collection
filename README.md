Guide to Scenarios
==================

An introduction to the DITA demonstration collection and a description of the maps and scenarios provided.

Eliot Kimber Updates
--------------------

I have updated this content set to add versions that use keys and key scopes (DITA 1.3)
in ways that reflect various suggested or potential best practices.

- Thunderbird-keys-reuse-only: Puts keys on all references to topics such that there is exactly one URI reference to each topic and each such reference has an associated keys. In addition, every navigation topicref has a key. Resource-only keys are defined for all images and for all topics that are used two or more times within the different maps in the information set.

- Thunderbird-keys-all-resonly: Declares a resource-only key for every topic (and image). All navigation topicrefs have keys and use keyrefs to the topics they place in the publication structure.


Introduction
------------

The DITA Demonstration Collection provides a set of sample DITA files that are meant to be used to demonstrate selected capabilities and benefits of DITA . The sample DITA files that have been prepared are intended to provide illustrative DITA content that is both technically valid and functionally realistic. It primary use-case is as a tool for demonstrating the capabilities of DITA to audiences that are interested in the functional benefits that can be achieved by deploying DITA.

The content has been created based on materials produced by various organizations with this content being modified to exclude proprietary details.

The functional objective set for the content itself is that it should be "functionally realistic" without necessarily being a flawless description of an actual system. As a technical objective, the DITA markup is valid and inline with generally accepted DITA markup practices. As a further objective, the DITA markup intentionally includes a range of possible markup and content organization tactics, based on patterns encountered in real-world content sources.

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

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

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
