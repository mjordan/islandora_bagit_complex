# Islandora BagIt Complex

Extends [Islandora BagIt](https://github.com/Islandora/islandora_bagit) to produce Bags for descendents of complex Islandora objects: compound object children, book pages, newspaper issues, and newspaper issue pages.

Use with caution, since creating a Bag for a newspaper, for example, will also create a Bag for each of its issues, and each page of each issue.


## Requirements

* [Islandora BagIt](https://github.com/Islandora/islandora_bagit)

## Installation

Install as usual, see [this](https://drupal.org/documentation/install/modules-themes/modules-7) for further information.

## Configuration

When enabled, this module adds a set of checkboxes labeled "Complex objects" to Islandora BagIt's admin settings form. Select the content models for which you want descendent objects created.

## Usage

This module has no user interface; instead, it changes the default behavior of the Islandora BagIt module. If enabled, when a user creates a Bag for a complex object (compound, book, or newspaper, or newspaper issue), this module will automaticall generate Bags for the object's descendents using the configuration parameters defined for the Islandora BagIt module.

Please note the following important points:

* This module does not apply to collections, since the Islandora BagIt module already handles them.
* Because this module can result in very long execution times when creating Bags, you should avoid creating Bags from within Drupal's user interface. Creating a Bag for a newspaper, for example, will almost certainly time out if initiated from within the newspaper object's Manage tab. If you enable this module, only create Bags using the Drush command.
* You should enable the "plugin_object_ds_basic" plugin so that each object's RELS-EXT datastream is included in its Bag. This datastream contains child-parent relationship data that will be necessary to associate an object with its parent, book, newspaper, or newspaper issue.

## Maintainer

* [Mark Jordan](https://github.com/mjordan)


## Feedback and Contrubuting

Feedback, bug reports, use cases, and pull requests are welcome. See CONTRIBUTING.md for details. Also feel free to post to the [Islandora Group](https://groups.google.com/forum/?hl=en&fromgroups#!forum/islandora) before opening an issue.
