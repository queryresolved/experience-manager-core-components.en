---
title: Form Text Component (v1)
seo-title: Form Text Component (v1)
description: null
seo-description: The Core Component Form Text component allows the entry of form text for submission.
uuid: 30123aba-57a8-4ed4-93cb-6a3d2edff9a7
content-type: reference
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: bd4e9930-4d81-49ae-a3d1-9a8740418dae
disttype: dist5
gnavtheme: light
groupsectionnavitems: no
hidemerchandisingbar: inherit
hidepromocomponent: inherit
modalsize: 426x240
noindex: true
index: y
internal: n
snippet: y
---

# Form Text Component (v1){#form-text-component-v}

The Core Component Form Text component allows the entry of form text for submission.

## Usage {#usage}

The Form Text Component allows for the submission of different types of text and is intended to be used along with the [form container component](form-container.md).

The type of text validation, labels, and help messages can be defined by the content editor in the [configure dialog](form-text-v1.md#main-pars_title).

## Version and Compatibility {#version-and-compatibility}

This document describes v1 of the Form Text Component, originally introduced with release 1.0.0 of the Core Components with AEM 6.3.

The following table lists the compatibility of v1 of the Form Text Component.

<table border="1" cellpadding="1" cellspacing="0" width="100%"> 
 <tbody> 
  <tr> 
   <td><strong>AEM Version</strong></td> 
   <td><strong>Form Text<br /> Component v1</strong><br /> </td> 
  </tr> 
  <tr> 
   <td>6.3</td> 
   <td>Compatible</td> 
  </tr> 
  <tr> 
   <td>6.4</td> 
   <td>Compatible</td> 
  </tr> 
 </tbody> 
</table>

>[!CAUTION]
>
>This document describes v1 of the Form Text Component.
>
>For details of the current version of the Form Text Component, see the [Form Text Component](form-text.md) document.

## Sample Component Output {#sample-component-output}

The following is sample taken from [We.Retail](/content/help/en/experience-manager/6-3/sites/developing/using/we-retail).

### Screenshot {#screenshot}

![](assets/chlimage_1.png) 

### HTML {#html}

```
<div class="cmp cmp-form aem-GridColumn aem-GridColumn--default--12">
 <form method="POST" action="/content/we-retail/us/en/experience.html" id="new_form" name="new_form" enctype="multipart/form-data" class="aem-Grid aem-Grid--12 aem-Grid--default--12 ">
     <input type="hidden" name=":formstart" value="/content/we-retail/us/en/experience/jcr:content/root/responsivegrid/container">
     <div class="cmp cmp-form-field aem-GridColumn aem-GridColumn--default--12">
   <div class="form-group">
       <label for="form-text-978484744">How many pieces of toast would you like?</label>
          <input type="number" id="form-text-978484744" name="pieces">
   </div>
  </div>
 </form>
</div>
```

### JSON {#json}

```
"container": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              "columnCount": 12,
              "gridClassNames": "aem-Grid aem-Grid--12 aem-Grid--default--12",
              ":items": {
                "text": {
                  "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
                  ":type": "weretail/components/form/text",
                  "name": "piecesOfToast",
                  "jcr:title": "How many pieces of toast would you like?",
                  "type": "number",
                  "rows": "2"
                }
              },
              ":itemsOrder": [
                "text"
              ],
              ":type": "weretail/components/form/container"
            }
```

>[!NOTE]
>
>JSON export from the Core Components requires release 1.1.0 of the Core Components. Please see the [compatibility information for Core Components v1](versions.md#main-pars_title_236368006) for more information.

## Configure Dialog {#configure-dialog}

The configure dialog allows the content author to define the type of text to be input as well as default values and labels.

### Main {#main}

![](assets/chlimage_1.png)

* **Constraint** - The type of text to be input and will be validated against

    * **Text**
    * **Text Area**
    * **Email**
    * **Tel**
    * **Date**
    * **Number**
    * **Password**

* **Text lines** - Number of lines to be displayed in the text area (only displayed when **Constraint** is set to **Text Area**)

* **Label** - The label that will be displayed for the field
* **Hide the label from being displayed** - Needed if the label is required only for accessibility purposes and does not impart any additional visual information about the field
* **Element Name** - The name of the field that is submitted with the form data
* **Value** - Default value that is pre-populated in the field

### About {#about}

![](assets/chlimage_1.png)

* **Help Message** - A hint to the user of what can be entered in the field
* **Display help message as placeholder** - To display the help message inside the form input when it is empty and not focused

### Constraints {#constraints}

![](assets/chlimage_1.png)

* **Constraint Message**

    * Message displayed as tooltip when submitting the form if the value does not validate the Type chosen
    * Not displayed for **Text** and **Text Area** constraint types

* **Required** - If selected the user must fill in a value before submitting the form
* **Make read only** - If selected the user cannot modify the value of the field

## Design Dialog {#design-dialog}

There is no design dialog for the Form Text component.

## Technical Details {#technical-details}

The latest technical documentation about the Form Text Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/text/v1/text).

The entire core components project can be downloaded from GitHub.

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md). 