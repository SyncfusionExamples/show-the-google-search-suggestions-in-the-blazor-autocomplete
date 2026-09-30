# How to Implement Google Search Suggestions in Syncfusion Blazor AutoComplete

## Overview

This sample demonstrates how to implement Google-style search suggestions using the Syncfusion [Blazor AutoComplete](https://www.syncfusion.com/blazor-components/blazor-autocomplete) component. As users type into the input field, the application requests suggestion data from Google's public suggestion service and displays matching results in the AutoComplete popup.

The sample showcases a custom filtering scenario where suggestion data is retrieved dynamically from a remote endpoint instead of a local collection. It also demonstrates how to intercept user input, process asynchronous responses, and update the suggestion list programmatically for a responsive search experience.

## Key Features

- Uses the `SfAutoComplete` component to provide searchable type-ahead suggestions.
- Handles user input through the `Filtering` event.
- Implements a custom filtering method named `OnCustomFiltering`.
- Accesses entered text through the `FilteringEventArgs` parameter.
- Uses `HttpClient` to request search suggestions from Google's suggestion API.
- Parses suggestion data using `System.Text.Json`.
- Stores suggestion results in a custom `GoogleSearch` model.
- Uses the `SuggestionText` property to represent individual search suggestions.
- Dynamically updates the AutoComplete data source through the `FilterAsync()` method.
- References the component instance using `AutoCompleteRef` for programmatic filtering.

## Prerequisites

- [Visual Studio 2022](https://visualstudio.microsoft.com/vs/) or [Visual Studio Code](https://code.visualstudio.com/)
- [.NET SDK](https://dotnet.microsoft.com/en-us/download/dotnet) compatible with the project's target framework

## How to Run the Project

**Visual Studio 2022**

1. Clone this repository.
2. Open the solution file:

   `BlazorAutoComplete.sln`

3. Restore all NuGet packages.
4. Build the solution.
5. Press `Ctrl+F5` to run the application.

**Visual Studio Code**

1. Clone this repository.
2. Open the repository folder in Visual Studio Code.
3. Navigate to the project directory:

```bash
cd BlazorAutoComplete
```

4. Restore NuGet packages:

```bash
dotnet restore
```

5. Run the application:

```bash
dotnet run
```

6. Open the local URL displayed in the terminal after the application starts.

## Project Structure

`BlazorAutoComplete/Pages/Index.razor` - Main sample page containing the Syncfusion AutoComplete component, custom filtering logic, HTTP requests, JSON parsing, and dynamic suggestion population.

`BlazorAutoComplete/Pages/FetchData.razor` - Default Blazor sample data page included with the application template.

## Support and Feedback

- For general product questions, visit the [Syncfusion Community Forum](https://www.syncfusion.com/forums) or [Syncfusion Support](https://www.syncfusion.com/support).
- To report an issue specific to this sample, open a GitHub issue in this repository.
- Official Syncfusion AutoComplete documentation: https://blazor.syncfusion.com/documentation/autocomplete/getting-started

## License

This is a Syncfusion sample project provided to demonstrate product usage. Review the [Syncfusion license terms](https://www.syncfusion.com/sales/pricing?category=ui-components) before using Syncfusion components in your own applications.