# ASP.NET Core Razor

## Norma I. Ayala-Rosa

1. Open Visual Studio, Create New Project, name it ASP.NET Razor Pages

2. Select Visual C#, Web, ASP.NET Core Web Application, double click on Web Application (MVC).

3. Look at Solution Tab to ensure all required templates are in that area.

4. Click Pages tab and Open it on Windows Explorer, two different files should appear.

5. Right click Properties, Debug, to ensure it has ASPNETCORE_ENVIRONMENT Development.

6. Click appssetting.json to ensure it has "Logging", one set for "Warning" and the other one set for "Debug".

7. Return to Startup, ensure it has configuration, services.AddMVC(); and the If and Else statements, app.useMvc, app.UseStaticFiles();.

8. Under wwwroot is were static pages, images, etc are.
 
9. Check the Viewimports and Viewstart pages, under the Layout.chstml, add End Body after @RazorRenderBody(), and Start w/o Debugging.

10. Undo using Control Z, End Body. Deliver this step-by-step instructions and the source listing form the project.
