# swagger-compact-theme

## Problem

Swagger default UI have too much unused space, so it makes you to scroll up and down a lot.

In cases, where an API method returns a lot of different status codes, the information doesn't even fit on screen.

When users needs to make a client for your API, they don't want to waste their time by scrolling

That's why we need a compact Swagger UI

## Solution

### A compact theme

![Compact theme](https://github.com/creewick/swagger-compact-theme/blob/master/pictures/pic1.png?raw=true)
A lot of space was saved by reducing margins around: API title, contoller titles, method titles, model blocks, etc.

### Two-column view

![Two-column view](https://github.com/creewick/swagger-compact-theme/blob/master/pictures/pic2.png?raw=true)

Showing an API method info in two-column view takes twice less space. Some margins were reduced there, too.

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
