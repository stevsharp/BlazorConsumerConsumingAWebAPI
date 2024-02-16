# Blazor Consumer: Consuming a Web API

This repository contains a sample project demonstrating how to consume a Web API using Blazor, a web framework for building interactive web UIs.

## Description

Blazor is a framework for building interactive web UIs using C# instead of JavaScript. This project illustrates how you can 
use Blazor to consume a Web API, allowing you to retrieve data from a server and render it in your Blazor application.

## Features
- Consumes a Web API using Blazor
- Retrieves data from the server and displays it in the UI
- Provides a basic example for integrating Blazor with backend services

## Getting Started
To get started with this project, follow these steps:

1. Clone this repository to your local machine.
2. Open the project in your preferred development environment (e.g., Visual Studio, Visual Studio Code).
3. Build and run the project.
4. Explore the code to understand how the Web API is consumed in the Blazor application.
5. Modify Web API launchSettings. ( "applicationUrl": "https://localhost:7195;http://localhost:5057" )
6. Add Cors to Web Api Start Up

builder.Services.AddCors(policy =>
{
    policy.AddPolicy("CorsPolicy", opt => opt
        .AllowAnyOrigin()
        .AllowAnyHeader()
        .AllowAnyMethod());
});

app.UseCors("CorsPolicy");

7. We can use the HttpClient service provided by the framework. It is already registered in the Program.cs class:

builder.Services.AddScoped(sp => new HttpClient { BaseAddress = new Uri("https://localhost:7195/") });

## Dependencies

This project depends on the following:

- .NET Core/.NET 7
- Blazor
- Web API (backend service)

## Usage
This project serves as a demonstration and starting point for building Blazor applications that consume Web APIs. You can use it as a reference or template for your own projects.

## Contributing
Contributions are welcome! If you have any ideas for improvement or bug fixes, feel free to submit a pull request.

## License
This project is licensed under the [MIT License](LICENSE).

## Acknowledgements
Special thanks to the Blazor community and the creators of the Web API used in this project.
