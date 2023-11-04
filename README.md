![OmenMon Logo](https://omenmon.github.io/assets/images/favicon.png)

# OmenMon Localization

This repository stores OmenMon interface translations into other languages.

## Using

To use a translation, download the XML file, and copy the `<String Key="...">` elements inside the `<Messages>` element of your `OmenMon.xml` configuration file:

````xml
<?xml version="1.0" encoding="utf-8"?> 
<OmenMon>
    <Messages>
        <!-- Paste the translated strings here. Example:
        <String Key="CliTranslated">Translated to [Language] by [Author]</String>
        <String Key="GuiTranslated">Translated by [Author]</String> -->
    </Messages>
</OmenMon>
````

For details, see [the documentation](https://omenmon.github.io/config#messages).

### System Settings

To display console messages with non-ASCII characters, you might additionally need to:
* Switch the code page to UTF-8: `chcp 65001`
* Change the console font

## Contributing

To add a new translation:

* Start with `OmenMon.en_US.xml` as a template
* Install as outlined in the [Using](#using) section above
* Translate the interface messages
  * Edit the XML file only when **OmenMon** is not running
  * You do not have to translate everything, e.g. unit names such as _Hz_ or _°C_
    * Delete any entries you did not change
* Copy your `OmenMon.xml` configuration file to `OmenMon.xx_YY.xml`, where:
  * `xx` is an [ISO 639-1](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) language code, _lower_-case
  * `YY` is an [ISO 3166-1 Alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) country code, _UPPER_-case
  * For example, `en_US` indicates _English (United States)_, the default localization
* You can add your translation credit as `CliTranslated` and `GuiTranslated` if you wish to do so
* Remove your configuration, i.e. anything between `<Config>` and `</Config>` and share the file here

## Resources

* Main **OmenMon** repository is at [https://github.com/OmenMon/OmenMon](https://github.com/OmenMon/OmenMon)
* Documentation is available at [https://omenmon.github.io/](https://omenmon.github.io/)
