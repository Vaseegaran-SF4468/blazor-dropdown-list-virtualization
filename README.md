# Blazor Dropdown List Virtualization

## Overview

This sample demonstrates how to use the Syncfusion [Blazor Dropdown List](https://www.syncfusion.com/blazor-components/blazor-dropdown-list) with virtualization enabled to improve performance when working with large collections of data. Instead of rendering every item in the popup at once, the component loads and renders only the items required for the current viewport. This approach reduces rendering overhead, improves responsiveness, and provides a smoother scrolling experience for end users.

The project focuses on the virtualization scenario within a Blazor application and serves as a reference implementation for applications that need to bind large datasets to a dropdown selection control.

## Key Features

- Demonstrates the Syncfusion Blazor DropDownList component with virtualization enabled using the `EnableVirtualization="true"` property.
- Binds a collection of 200 records to the DropDownList through the `DataSource` property.
- Uses strongly typed component configuration with `TValue="int?"` and `TItem="DropdownModel"`.
- Configures text and value mappings using the `DropDownListFieldSettings` component:
  - `Text="TextField"`
  - `Value="ValueField"`
- Enables two-way value binding with `@bind-Value` to track and display the selected item.
- Populates the data source dynamically using `Enumerable.Range()` during the `OnInitialized()` lifecycle method.
- Defines a custom `DropdownModel` class containing `TextField` and `ValueField` properties for item representation.
- Displays the currently selected value outside the DropDownList for immediate selection feedback.
- Includes a standard Blazor `FetchData` page that demonstrates loading JSON data through `HttpClient` and rendering weather forecast information in a table.

## Prerequisites

- [Visual Studio 2022](https://visualstudio.microsoft.com/vs/) or [Visual Studio Code](https://code.visualstudio.com/)
- [.NET SDK](https://dotnet.microsoft.com/en-us/download/dotnet) compatible with the project's target framework

## How to Run the Project

**Visual Studio 2022**

1. Clone this repository.
2. Open the solution file:

   `BlazorApp_Dropdown_Virtual_Scrolling.sln`

3. Restore NuGet packages.
4. Build the solution.
5. If prompted, set `BlazorApp_Dropdown_Virtual_Scrolling` as the startup project.
6. Run the application using `Ctrl+F5`.

**Visual Studio Code**

1. Clone this repository.
2. Open the repository folder in Visual Studio Code.
3. Navigate to the project directory:

```bash
cd BlazorApp_Dropdown_Virtual_Scrolling
```

4. Restore dependencies:

```bash
dotnet restore
```

5. Run the application:

```bash
dotnet run
```

6. Open the locally displayed application URL shown in the terminal after launch.

## Project Structure

`Pages/Index.razor` - Demonstrates the Syncfusion DropDownList component with virtual scrolling enabled, local data binding, field mapping, and selected value tracking.

`Pages/FetchData.razor` - Demonstrates fetching weather forecast data from a JSON file using `HttpClient` and displaying the results in a table.

`BlazorApp_Dropdown_Virtual_Scrolling/wwwroot/sample-data/weather.json` - JSON data source consumed by the FetchData page.

## Support and Feedback

- For general product questions, visit the [Syncfusion Community Forum](https://www.syncfusion.com/forums) or [Syncfusion Support](https://www.syncfusion.com/support).
- To report an issue specific to this sample, open a GitHub issue in this repository.
- Documentation: https://blazor.syncfusion.com/documentation/dropdown-list/virtualization

## License

This is a Syncfusion sample project provided to demonstrate product usage. Review the [Syncfusion license terms](https://www.syncfusion.com/sales/pricing?category=ui-components) before using Syncfusion components in your own applications.