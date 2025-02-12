# .NET Extensions Library

This is a class library with .NET Extensions. It provides helper classes for Enums, strings, URLs, and will evolve with other classes over time. The library is packaged and published on [nuget.org](https://www.nuget.org/).

## Features

- **EnumHelper**: Provides methods to get display names and descriptions for enum values.
- **StringHelper**: Provides methods to manipulate strings, such as converting the first character to uppercase.
- **UrlHelper**: Provides methods to extract information from URLs, such as getting the host.

## Installation

You can install the library via NuGet Package Manager:

```sh
dotnet add package filipecarneiro.dotnetextensions
```

## Usage

### EnumHelper

```csharp
using DotNetExtensions;

public enum SampleEnum
{
    [Display(Name = "Sample Name", Description = "Sample Description")]
    SampleValue
}

var displayName = EnumHelper.GetDisplayName(SampleEnum.SampleValue);
var displayDescription = EnumHelper.GetDisplayDescription(SampleEnum.SampleValue);
```
### StringHelper

```csharp
using DotNetExtensions;

string input = "hello";
string result = input.FirstCharToUpper(); // Output: "Hello"
```
### UrlHelper

```csharp
using DotNetExtensions;

string url = "https://www.example.com/path/123";
string host = UrlHelper.GetHost(url); // Output: "www.example.com"
```

## Contributing
Contributions are welcome! Please open an issue or submit a pull request on GitHub.

## Build and Publish

Use the [Build and Push](https://github.com/filipecarneiro/DotNetExtensions/actions/workflows/build.yml) GitHub workflow Action to build and publish the library.

## License
This project is licensed under the MIT License.
