---
title: "test"
date: 2019-03-08T09:43:22+01:00
featured: true
draft: true
toc: true
---

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

  {{% column %}}
    field 5 
  {{% /column %}}

{{< /columns >}}






***
## class and _class


### columns  class="is-mobile" _class="box"

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