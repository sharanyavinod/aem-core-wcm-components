<!--
Copyright 2017 Adobe Systems Incorporated

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
-->
Form Options (v3)
====
Options form field written in HTL.

## Features
* Checkboxes
* Radio buttons
* Drop down
* Multi select drop down

### Use Object
The Form Options component uses the `com.adobe.cq.wcm.core.components.models.form.Options` Sling Model for its Use-object.

### Edit Dialog Properties
The following properties are written to JCR for this Form Options component and are expected to be available as `Resource` properties:

1. `./id` - defines the id for the option
2. `./type` - defines the type of options form; possible values: `checkbox`, `radio`, `drop-down`, `multi-drop-down`
3. `./title` - defines the title of the form, which is used to describe its role
4. `./name` - defines the name of the field, which will be submitted with the form data
5. `./source` - defines the source of the options; possible values: `local`, `list`, `datasource`
6. `./listPath` - defines the path of a static list for the options, if the `source` property is set to `list`
7. `./datasourceRT` - defines the resource type of the datasource, if the `source` property is set to `datasource`
8. `./items` - defines the option items, if the `source` property is set to `local`
9. `./helpMessage` - defines a help message that can be rendered in the field as a hint for the user

## Client Libraries
The component provides a `core.wcm.components.form.options.v3.editor` editor client library category that includes
JavaScript handling for dialog interaction. It is already included by its edit dialog.

## BEM Description
```
BLOCK cmp-form-options
    ELEMENT cmp-form-options__legend
    ELEMENT cmp-form-options__field-label
    ELEMENT cmp-form-options__field
        MOD cmp-form-options__field--checkbox
        MOD cmp-form-options__field--radio
    ELEMENT cmp-form-options__field-description
    ELEMENT cmp-form-options__label
    ELEMENT cmp-form-options__drop-down-field
    ELEMENT cmp-form-options__multi-drop-down-field
    ELEMENT cmp-form-options__help-message
```

## Information
* **Vendor**: Adobe
* **Version**: v3
* **Compatibility**: AEM 6.3
* **Status**: production-ready
* **Documentation**: [https://www.adobe.com/go/aem\_cmp\_form\_options\_v3](https://www.adobe.com/go/aem_cmp_form_options_v3)
