codeRR.Client configuration
===========================

If you have not done that yet, install the nuget package called `coderr.client`.

Next, you need to tell the codeRR library what it should upload all error reports to.

Add the following code in your `Program.cs` (or the starting point of the framework that you use).

```csharp
var url = new Uri("http://yourServer/coderr/");
Err.Configuration.Credentials(url, 
                              "yourAppKey", 
                              "yourSharedSecret");
```

Once done, try to report an exception.
Add the following somewhere and then invoke your application:

```csharp
try
{
    throw new Exception("Hello world");
}
catch (Exception ex)
{
    Err.Report(ex, new { SampleData = "Context example"});
}
```

## More information

Want to dig deeper? Read the [client documentation](index.md) or how you can [report errors](../../gettingstarted.md)
