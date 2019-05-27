# Islandora BagIt Complex

Extends [Islandora BagIt](https://github.com/Islandora/islandora_bagit) to produce child-level Bags for compound object children, book pages, and newspaper issues and issue pages.

This module does not apply to collections, since the Islandora BagIt module already handles them.

## Requirements

* [Islandora BagIt](https://github.com/Islandora/islandora_bagit)

## Installation

Install as usual, see [this](https://drupal.org/documentation/install/modules-themes/modules-7) for further information.

## Usage

This module has no user interface. If enabled, when a user creates a Bag for a complex object (compound, book, or newspaper), this module will automaticall generate Bags for the object's descendents using the configuration parameters defined for the Islandora BagIt module.

> Note: Because this module can result in very long execution times when creating Bags, you should avoid creating Bags from within Drupal's user interface. Creating a Bag for a newspaper, for example, will almost certainly time out if initiated from within the newspaper object's Manage tab. If you enable this module, only create Bags using the Drush command.

## Maintainer

* [Mark Jordan](https://github.com/mjordan)


## Feedback and Contrubuting

Feedback, but reports, use cases, and pull requests are welcome. See CONTRIBUTING.md for details. Also feel free to post to the [Islandora Group](https://groups.google.com/forum/?hl=en&fromgroups#!forum/islandora) before opening an issue.
