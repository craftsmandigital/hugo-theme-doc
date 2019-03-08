---
title: "Bulma Columns Shortcode"
date: 2019-03-08T09:43:22+01:00
featured: true
draft: true
toc: true
---

The shortcodes `{{</* columns */>}}` and `{{%/* column */%}}` is a way to build a subset of the [Bulma columns](https://bulma.io/documentation/columns/) feature in shortcodes



shortcode | bulma feature | Bulma doc
---------|----------------|-----
columns | `<div class="columns">` | [link](https://bulma.io/documentation/columns/basics/)
column | `<div class="column">` | [link](https://bulma.io/documentation/columns/options/) 
***

## columns 
  ```text
{{</* columns */>}}
  ```

### columns shortcode setup
This is the minimum shortcode with no parameter. Default it vil output two equal sized collumns.

Here is an exsample how you chould do the setup

`{{%/* column */%}}` could always live inside `{{</* columns */>}}`



  ```tekst
{{</* columns */>}}

  {{%/* column */%}}
    field 1
  {{%/* /column */%}}

  {{%/* column */%}}
    field 2 
  {{%/* /column */%}}

  {{%/* column */%}}
    field 3 
  {{%/* /column */%}}

  {{%/* column */%}}
    field 4 
  {{%/* /column */%}}

{{</* /columns */>}}
```
### Rendered output of the colums setup 

Rendered output of the exsample above

{{< columns >}}

  {{% column %}}
    field 1
  {{% /column %}}

  {{% column %}}
    field 2 
  {{% /column %}}

  {{% column %}}
    field 3 
  {{% /column %}}

  {{% column %}}
    field 4 
  {{% /column %}}

{{< /columns >}}






***
## class and _class

```text
{{</* columns  class="<bulma columns options>" _class="<bulma column options>" */>}}
```
shortcode | option belongs to | Sample options
---------|----------------|-----
columns | class | [is-mobile is-sentered is-gapless](https://bulma.io/documentation/columns/basics/)
column | _class | [box is-narrow](https://bulma.io/documentation/columns/options/) 


{{% notification is-danger %}}
Do not touc options that has something with column sizes, [like the options described on this link](https://bulma.io/documentation/columns/sizes/)

is-three-quarters, is-two-thirds, is-half, is-one-third, is-one-quarter, is-full, is-four-fifths, is-three-fifths, is-two-fifths, is-one-fifth
{{% /notification %}}

options that handles sizes are described [later on](#colsizes-option)

### here are some sample cases
```text
{{</* columns  class="is-mobile" _class="box" */>}}
{{</* columns  _class="box" */>}}
{{</* columns  class="is-mobile" */>}}
```

### columns  class="is-mobile" _class="box"
The exsample below render output of this statement
```text
{{</* columns  class="is-mobile" _class="box" */>}}
```
- `is-mobile` makes the columns to not colapse to one column on a mobile. You can try it and size the browser so narrow as you can. ([The previous exsample vil colapse](#rendered-output-of-the-colums-setup))
- `box` vil render a frame on eatch item

{{< columns  class="is-mobile" _class="box" >}}
  {{% column %}}
    field 1
  {{% /column %}}

  {{% column %}}
    field 2 
  {{% /column %}}

  {{% column %}}
    field 3 
  {{% /column %}}

  {{% column %}}
    field 4 
  {{% /column %}}

{{< /columns >}}







***
## colsizes option
- This option describe how many colums there could be
- Describe how the columns could be sized
- Description and examples on how it works can be found in the [Bulma docs](https://bulma.io/documentation/columns/sizes/#12-columns-system) 

```text
{{</* columns  colsizes="<list of numbers separated by space>" */>}}

{{</* columns  colsizes="2 2 2 2 2 2" */>}}
{{</* columns  colsizes="3 3 3 3" */>}}
{{</* columns  colsizes="2 4 6" */>}}
```

Colsizes option | Number of collumns | Evaluation
---------|----------|---------
 "2 4 6" | 3 | third collumn is as vide as first and second collumn.
 "4 8" | 2 | Second collumn is duble as wide as first collumn
 "3 3 3 3" | 4 | all collumns equal sized


{{% notification is-danger %}}
The sum of te numbers in colsizes could always be 12. Othervise an error is trigered.

Colsizes option | Sum | Evaluation
---------|----------|---------
 "2 4 8" | 14 | Bad
 "3 3 3 3" | 12 | Correct
 "4 44" | 48 | Real Bad
 "4 3 3" | 10 | Bad
{{% /notification %}}

### Rendered output of colsizes="2 4 6"

```text
{{</* columns  colsizes="2 4 6" _class="box"*/>}}
```
Added box option because it is easier to see output
{{< columns  colsizes="2 4 6" _class="box" >}}
  {{% column %}}
    field 1
  {{% /column %}}

  {{% column %}}
    field 2 
  {{% /column %}}

  {{% column %}}
    field 3 
  {{% /column %}}

  {{% column %}}
    field 4 
  {{% /column %}}
  
  {{% column %}}
    field 5
  {{% /column %}}

  {{% column %}}
    field 6 
  {{% /column %}}

  {{% column %}}
    field 7 
  {{% /column %}}

  {{% column %}}
    field 8 
  {{% /column %}}
  
  {{% column %}}
    field 9
  {{% /column %}}

  {{% column %}}
    field 10
  {{% /column %}}

  {{% column %}}
    field 11
  {{% /column %}}

  {{% column %}}
    field 12
  {{% /column %}}

{{< /columns >}}


### Rendered output of colsizes="4 8"

```text
{{</* columns  colsizes="4 8" _class="box"*/>}}
```
Added box option because it is easier to see output
{{< columns  colsizes="4 8" _class="box" >}}
  {{% column %}}
    field 1
  {{% /column %}}

  {{% column %}}
    field 2 
  {{% /column %}}

  {{% column %}}
    field 3 
  {{% /column %}}

  {{% column %}}
    field 4 
  {{% /column %}}
  
  {{% column %}}
    field 5
  {{% /column %}}

  {{% column %}}
    field 6 
  {{% /column %}}

  {{% column %}}
    field 7 
  {{% /column %}}

  {{% column %}}
    field 8 
  {{% /column %}}
  
  {{% column %}}
    field 9
  {{% /column %}}

  {{% column %}}
    field 10
  {{% /column %}}

  {{% column %}}
    field 11
  {{% /column %}}

  {{% column %}}
    field 12
  {{% /column %}}

{{< /columns >}}

### Rendered output of colsizes="3 3 3 3"

```text
{{</* columns  colsizes="3 3 3 3" _class="box"*/>}}
```
Added box option because it is easier to see output
{{< columns  colsizes="3 3 3 3" _class="box" >}}
  {{% column %}}
    field 1
  {{% /column %}}

  {{% column %}}
    field 2 
  {{% /column %}}

  {{% column %}}
    field 3 
  {{% /column %}}

  {{% column %}}
    field 4 
  {{% /column %}}
  
  {{% column %}}
    field 5
  {{% /column %}}

  {{% column %}}
    field 6 
  {{% /column %}}

  {{% column %}}
    field 7 
  {{% /column %}}

  {{% column %}}
    field 8 
  {{% /column %}}
  
  {{% column %}}
    field 9
  {{% /column %}}

  {{% column %}}
    field 10
  {{% /column %}}

  {{% column %}}
    field 11
  {{% /column %}}

  {{% column %}}
    field 12
  {{% /column %}}

{{< /columns >}}