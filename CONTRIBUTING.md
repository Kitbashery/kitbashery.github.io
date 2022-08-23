# Contributing documentation:

If you see something wrong or missing from the documentation and want to fix it yourself you may modify the GitHub markdown files in the /docs folder and put in a pull request.
Documentation is written in [markdown](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

Kitbashery uses the Jekyll theme: [Just the Docs](https://github.com/just-the-docs/just-the-docs) and uses the following navigation structure:

```
Asset Name 
  Classes
    Script.cs
  Structs
    MyStruct
  Enumerations
    MyEnum
```
Navigation structure is defined by the theme using YAML front matter you can read about the theme's navigation system [here](https://just-the-docs.github.io/just-the-docs/docs/navigation-structure/).


# Page layout is:

`
Page navigation YAML Front Matter...
`

# Class/Struct/Enum Name

### Inherits from:
Link to class (if applicable)
  
## Description:
You description

## Usage Notes:
any remarks on how to use the file.

## Public Properties:
```
| Type        | Name | Description         | Default Value |
|:-------------|:----|:--------------------|:--------------|
|  `type` | name | description | `default value` |
```
## Public Methods:

```
| Name | Summary      | Parameters | Returns |
|:----|:--------------|:-----------|:--------|
| MethodName | MethodSummary... | Type paramName "param summary", Type, paramName2 "param summary" | `Void` "returns summary" |
```

## Structs:

### `[Serializable]` Struct Name

## Struct Public Properties:
...

## Enumerations

### Enumeration Name

`{ enumValue, enumValue2 }`
