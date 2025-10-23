> Archived – Now maintained in the Netherlands3D Main Repository; OpenUPM updates suspended.

# JSON Extra's for Netherlands3D

## Installing

This package is provided through OpenUPM, to install it using the CLI you can perform the following:

```bash
$ openupm add eu.netherlands3d.json
```

or, you have to add `https://package.openupm.com` as a scoped registry with, at least, the following scopes:

- `eu.netherlands3d`

## JSON Converters

## Color

A JSON Converter for JSON.net is provided that can interpret hexadecimal or CSS-named color codes in JSON, and convert 
them into UnityEngine.Color objects. To use this, ensure the type of a field is UnityEngine.Color and add the following 
annotation:

```csharp
using UnityEngine;
using Netherlands3D.Json.JsonConverters;
using Newtonsoft.Json;

class MyJson {
    [JsonConverter(typeof(ColorConverter))]
    public Color $color;
}
```

Accepted color variants are every variant supported by [ColorUtility.TryParseHtmlString](https://docs.unity3d.com/ScriptReference/ColorUtility.TryParseHtmlString.html). 
When serializing to a JSON file, it will always output as `#RRGGBBAA`.

## System.URI

A JSON Converter for JSON.net is provided that can interpret URIs in JSON and convert them into URI objects. To use 
this, ensure the type of a field is System.URI and add the following annotation:

```csharp
using System;
using Netherlands3D.Json.JsonConverters;
using Newtonsoft.Json;

class MyJson {
    [JsonConverter(typeof(UriConverter))]
    public Uri $uri;
}
```

# Repository Archived

This repository has been **archived** and is no longer maintained independently.

The contents of this package have been merged into the  
**[Netherlands3D Main Repository](https://github.com/Netherlands3D/twin)**  
into the `Packages` folder.

## Current Location

The latest version and future updates of this package will be maintained inside the Netherlands3D main repository as part of an effort to simplify and unify our development workflow.

## Why was this repository archived?

To streamline development and reduce overhead, the Netherlands3D packages are being integrated into the main repository.  
This approach allows for better coordination between packages and features, while we continue to evaluate whether a full monorepo setup (including versioning) is desirable in the future.

## Where to contribute

Please open issues and pull requests in the [Netherlands3D Main Repository](https://github.com/Netherlands3D/twin).

## Publication status

Updates to this package on **OpenUPM** are **suspended until further notice**.  
Future releases will be managed from the main repository once the new development flow has been finalized.

## Historical reference

This repository remains available in read-only mode as a historical record of its standalone development.
