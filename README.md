This is a basic ASP.NET Core application (using the Web API (MVC) template in Rider) with Sentry added, created as a minimal reproduction for https://github.com/getsentry/sentry-dotnet/issues/4672. .NET 9 is required to run.

To reproduce:

1. Clone the repository
2. In your appsettings.json or using an environment variable, set your Sentry DSN.
3. Restore the project dependencies and run the program. 

On visiting any endpoint, you will see that the exception within the ConfigureScope call is thrown, and then execution of the application finishes with exit code 134.
