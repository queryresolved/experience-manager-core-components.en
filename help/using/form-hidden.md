---
title: Form Hidden Component
seo-title: Form Hidden Component
description: null
seo-description: The Core Component Form Hidden component allows for the display of a hidden field.
uuid: 63a1b381-f45c-4241-b743-dea8abd45e11
contentOwner: User
content-type: reference
topic-tags: authoring
topic-tags: core-components
discoiquuid: 36e49035-7641-4bad-8a61-723060032903
disttype: dist5
gnavtheme: light
groupsectionnavitems: no
hidemerchandisingbar: inherit
hidepromocomponent: inherit
modalsize: 426x240
index: y
internal: n
snippet: y
---

# Form Hidden Component{#form-hidden-component}

The Core Component Form Hidden component allows for the display of a hidden field.

## Usage {#usage}

The Core Component Form Hidden Component allows for the creation of hidden fields to pass information about the current page back to AEM and is intended to be used along with the [form container component](form-container.md).

The field properties can be defined by the content editor in the [configure dialog](form-hidden.md#main-pars_title).

## Version and Compatibility {#version-and-compatibility}

The current version of the Form Hidden Component is v2, which was introduced with release 2.0.0 of the Core Components in January 2018, and is described in this document.

The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

<table border="1" cellpadding="1" cellspacing="0" width="100%"> 
 <tbody> 
  <tr> 
   <td>Component Version<br /> </td> 
   <td>AEM 6.3</td> 
   <td>AEM 6.4</td> 
  </tr> 
  <tr> 
   <td>v2<br /> </td> 
   <td>Compatible</td> 
   <td>Compatible</td> 
  </tr> 
  <tr> 
   <td><a href="../using/form-hidden-v1.md">v1</a></td> 
   <td>Compatible</td> 
   <td>Compatible</td> 
  </tr> 
 </tbody> 
</table>

For more information about Core Component versions and releases, see the document [Core Components Versions](versions.md).

## Sample Component Output {#sample-component-output}

The following is sample taken from [We.Retail](/content/help/en/experience-manager/6-3/sites/developing/using/we-retail).

### HTML {#html}

```
<div class="cmp cmp-form aem-GridColumn aem-GridColumn--default--12">
 <form method="POST" action="/content/we-retail/us/en/experience.html" id="new_form" name="new_form" enctype="multipart/form-data" class="aem-Grid aem-Grid--12 aem-Grid--default--12 ">
  <input type="hidden" name=":formstart" value="/content/we-retail/us/en/experience/jcr:content/root/responsivegrid/container">
   <div class="visible aem-GridColumn aem-GridColumn--default--12">
    <input type="hidden" id="ghostToast" name="Invisible Toast" value="ghostToast">
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
                "hidden": {
                  "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
                  ":type": "weretail/components/form/hidden",
                  "name": "Invisible Toast",
                  "id": "ghostToast",
                  "value": "ghostToast"
                }
              },
              ":itemsOrder": [
                "hidden"
              ],
              ":type": "weretail/components/form/container"
            }
```

## Configure Dialog {#configure-dialog}

The configure dialog allows the content author to define the parameters of the hidden field.

![](assets/chlimage_1-26.png)

* **Name** - The name of the field, which is submitted with the form data
* **Value** - The value of the field, which is submitted with the form data
* **Identifier** - The identifier should be unique on the page and can be used to bind scripts to this form field

Because the Form Hidden component normally has no visible attributes, the component's placeholder in the editor displays the **Name** and **Value** field values if they are assigned in order to help the author identify the appropriate Form Hidden component.

![](assets/screenshot_2018-10-19at094927.png) 

## Design Dialog {#design-dialog}

There is no design dialog for the Form Hidden component.

## Technical Details {#technical-details}

The latest technical documentation about the Form Hidden Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/form/hidden/v2/hidden).

The entire core components project can be downloaded from GitHub.

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md). 