# swagger-compact-theme

## Features

### A compact theme for Swagger UI

![Compact theme](https://github.com/creewick/swagger-compact-theme/blob/master/pictures/pic1.png?raw=true)
A lot of space was saved by reducing margins around: API title, contoller titles, method titles, model blocks

### Two-column view

![Two-column view](https://github.com/creewick/swagger-compact-theme/blob/master/pictures/pic2.png?raw=true)

API method blocks are now shown as two columns: Parameters and Responses. 

Some margins were removed from there, too.

### Other tweaks

File's divided onto regions, so you can easily disable or remove some parts of this theme.

For example, some specific styles are located in `/*#region Extra specific styles*/`

## How to use

### ASP.NET CORE MVC

1. Put the .css into your `wwwroot` folder

2. Inject it in `Startup` with Swashbuckle methods

```c#
public void Configure(IApplicationBuilder app, ...)
{
    ...
    app.UseSwaggerUI(options =>
    {
        options.InjectStylesheet("/custom.css");
        ...
    }
    ...
}
```
