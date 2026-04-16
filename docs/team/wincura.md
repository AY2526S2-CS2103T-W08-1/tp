---
layout: page
title: William Scott Win's Project Portfolio Page
---

### Project: Bivago

**Bivago is a desktop application that helps tour guides streamline the process involved in planning and executing new
group tours.**
It helps them quickly look up contacts for attractions, hotels, restaurants and drivers before, during and after different types
of tours that the tour guides offer.

The user interacts with it using a CLI, and it has a GUI created with JavaFX. It is written in Java.

Given below are my contributions to the project.

* **New Entities**: Added support for multiple contact types.
  * What it does: allows the user to manage multiple types of contacts beyond `Person` from the original AB3. This involves having type-specific fields for each type.
  * Justification: This feature improves the product significantly because our target user can manage their contacts differently and does not have to rely on tags on a `Person` alone to differentiate hotels, restaurants and amusement parks, for example.
  * Highlights: This enhancement required an in-depth understanding of the underlying architecture as the `Model`, `Storage` and `Logic` components of the original AB3 project had to be significantly updated to support the new types of contacts. This involved updates to the features `add` and `edit`, including their commands, their syntax, their usage messages, their parsers, and the serialization/deserialization process involving the `.json` data file.
  * Credits: Usage of AI Tools (Open AI) to assist in extending tests to support different contact types, subsequently verified and tweaked accordingly. Namely in:
    `FavouriteStatusTest.java`, `HalalStatusTest.java`,
    `OpeningHourTest.java`, `ClosingHourTest.java`,
    `AccommodationStarsTest.java`, `EditContactDescriptorTest.java`,
    `FnbTest.java`, `AttractionTest.java`, `AccommodationTest.java`,
    `EditCommandTest.java`, `AddCommandParserTest.java`
* **New Feature**: Added the ability to manage favourite contacts.
  * What it does: allows the user to undo all previous commands one at a time. Preceding undo commands can be reversed by using the redo command.
  * Justification: This feature improves the product significantly because a user can make mistakes in commands and the app should provide a convenient way to rectify them.
  * Highlights: This enhancement affects existing commands and commands to be added in future. It required an in-depth analysis of design alternatives. The implementation too was challenging as it required changes to existing commands.
  * Credits: Usage of AI Tools (Open AI) to assist in extending tests to support different contact types and favourite contacts,
    subsequently verified and tweaked accordingly. Namely in:
    `FavouriteStatusTest.java`, `HalalStatusTest.java`,
    `OpeningHourTest.java`, `ClosingHourTest.java`,
    `AccommodationStarsTest.java`, `EditContactDescriptorTest.java`,
    `FnbTest.java`, `AttractionTest.java`, `AccommodationTest.java`,
    `ContactIsFavouritePredicateTest.java`, `FavouriteAddCommandTest.java`,
    `FavouriteRemoveCommandTest.java`, `FavouriteViewCommandTest.java`,
    `FavouriteAddCommandParserTest.java`, `FavouriteRemoveCommandParserTest.java`,
    `EditCommandTest.java`, `AddCommandParserTest.java`
* **Code contributed**: [RepoSense link]("https://nus-cs2103-ay2526-s2.github.io/tp-dashboard/?search=wincura&breakdown=true")

* **Enhancements to existing features**:
  * Designed the icon of the application

* **Documentation**:
  * User Guide:
    * Updated the Summary and the `Quick Start` section
    * Added the `How it serves you` section describing the value provided by our solutions for target users
    * Updated the documentation for the features `add` and `edit`
    * Added documentation for the features `favourite-add`, `favourite-remove` and `favourite-view`
    * Did cosmetic tweaks to existing documentation of all features including drop-down lists for example commands
  * Developer Guide:
    * Added implementation details of the added contact types
    * Added implementation details of the features `favourite-add`, `favourite-remove` and `favourite-view`
    * Added use cases for the features `list`, `favourite-add`, `favourite-remove` and `favourite-view`
    * Added manual testing instructions for the features `add`, `list`, `edit`, `favourite-add`, `favourite-remove` and `favourite-view`
    * Updated manual testing instructions for the `delete` feature
