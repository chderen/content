---
title: Intl.Locale
slug: Web/JavaScript/Reference/Global_Objects/Intl/Locale
tags:
  - Class
  - Internationalization
  - Intl
  - JavaScript
  - Locale
  - Reference
browser-compat: javascript.builtins.Intl.Locale
---
{{JSRef}}

The **`Intl.Locale`** object is a standard built-in property of the Intl object
that represents a Unicode locale identifier.

{{EmbedInteractiveExample("pages/js/intl-locale.html")}}

<!-- The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone https://github.com/mdn/interactive-examples and send us a pull request. -->

## Description

The **`Intl.Locale`** object was created to allow for easier manipulation of
Unicode locales. Unicode represents locales with a string, called a *locale
identifier*. The locale identifier consists of a *language identifier* and
*extension tags*. Language identifiers are the core of the locale, consisting of
*language*, *script*, and *region subtags*. Additional information about the
locale is stored in the optional *extension tags*. Extension tags hold
information about locale aspects such as calendar type, clock type, and
numbering system type.

Traditionally, the Intl API used strings to represent locales, just as Unicode
does. This is a simple and lightweight solution that works well. Adding a Locale
class, however, adds ease of parsing and manipulating the language, script, and
region, as well as extension tags.

## Constructor

*   {{jsxref("Intl/Locale/Locale", "Intl.Locale()")}}
    *   : Creates a new `Locale` object.

## Instance properties

*   {{jsxref("Intl/Locale/baseName", "Intl.Locale.prototype.baseName")}}
    *   : Returns basic, core information about the `Locale` in the form of a
        substring of the complete data string.
*   {{jsxref("Intl/Locale/calendar", "Intl.Locale.prototype.calendar")}}
    *   : Returns the part of the `Locale` that indicates the Locale's calendar era.
*   {{jsxref("Intl/Locale/caseFirst", "Intl.Locale.prototype.caseFirst")}}
    *   : Returns whether case is taken into account for the locale's collation
        rules.
*   {{jsxref("Intl/Locale/collation", "Intl.Locale.prototype.collation")}}
    *   : Returns the collation type for the `Locale`, which is used to order
        strings according to the locale's rules.
*   {{jsxref("Intl/Locale/hourCycle", "Intl.Locale.prototype.hourCycle")}}
    *   : Returns the time keeping format convention used by the locale.
*   {{jsxref("Intl/Locale/language", "Intl.Locale.prototype.language")}}
    *   : Returns the language associated with the locale.
*   {{jsxref("Intl/Locale/numberingSystem", "Intl.Locale.prototype.numberingSystem")}}
    *   : Returns the numeral system used by the locale.
*   {{jsxref("Intl/Locale/numeric", "Intl.Locale.prototype.numeric")}}
    *   : Returns whether the locale has special collation handling for numeric
        characters.
*   {{jsxref("Intl/Locale/region", "Intl.Locale.prototype.region")}}
    *   : Returns the region of the world (usually a country) associated with the
        locale.
*   {{jsxref("Intl/Locale/script", "Intl.Locale.prototype.script")}}
    *   : Returns the script used for writing the particular language used in the
        locale.

## Instance methods

*   {{jsxref("Intl/Locale/maximize", "Intl.Locale.prototype.maximize()")}}
    *   : Gets the most likely values for the language, script, and region of the
        locale based on existing values.
*   {{jsxref("Intl/Locale/minimize", "Intl.Locale.prototype.minimize()")}}
    *   : Gets the most likely values for the language, script, and region of the
        locale based on existing values.
*   {{jsxref("Intl/Locale/toString", "Intl.Locale.prototype.toString()")}}
    *   : Returns the Locale's full locale identifier string.

## Examples

### Basic usage

At its very simplest, the
{{jsxref("Intl/Locale/Locale", "Intl.Locale")}} constructor
takes a locale identifier string as its argument:

```js
let us = new Intl.Locale('en-US');
```

### Using the Locale constructor with an options object

The constructor also takes an optional configuration object argument, which can
contain any of several extension types. For example, set the
{{jsxref("Intl/Locale/hourCycle", "hourCycle")}} property of the
configuration object to your desired hour cycle type, and then pass it into the
constructor:

```js
let us12hour = new Intl.Locale("en-US", {hourCycle: "h12"});
console.log(us12hour.hourCycle); // Prints "h12"
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

*   {{jsxref("Intl")}}
*   [The Intl.Locale Polyfill](https://formatjs.io/docs/polyfills/intl-locale)
*   [Unicode locale identifiers spec](https://www.unicode.org/reports/tr35/#Canonical_Unicode_Locale_Identifiers)