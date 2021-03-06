# ASP.NET Core Identity Series

![ASP.NET Core Identity Series](https://chsakell.files.wordpress.com/2018/04/aspnet-core-identity-13.png)

## Part 1 - [Getting Started](http://chsakell.com/2018/04/28/asp-net-core-identity-series-getting-started)

* Introduction to ASP.NET Core Identity library
* Describe ASP.NET Core Identity basic archirecture
* Explain the role and relationship between `Stores` and `Managers` and how they function under the hood
* Explain what `Claims`, `ClaimsIdentity` and `ClaimsPrincipal` entities are and how they are related
* Step by step guide on how to install and start using the core packages
* Associated repository branch: [getting-started](https://github.com/chsakell/aspnet-core-identity/tree/getting-started)

## Part 2 - [Integrate Entity Framework](https://wp.me/p3mRWu-1i4)

* Introduce `Microsoft.Extensions.Identity.Stores` and `UserStoreBase` store implementations
* Plug and configure Entity Framework Core with ASP.NET Core Identity and minimum configuration
* Explain Entity Framework different store implementations such as `UserOnlyStore` or `UserStore`
* Step by step guide for applying migrations and creating Identity's SQL Schema
* Discuss whether you should use ASP.NET Core Identity with Entity Framework
* Associated repository branch: [entity-framework-integration](https://github.com/chsakell/aspnet-core-identity/tree/entity-framework-integration)

## Part 3 - [Deep Dive in authorization](https://wp.me/p3mRWu-1ik)

* Explain `Claims-based` authorization by example
* Explain `Role-based` authorization by example
* Step by step guide for creating custom `Authorization Policy Provider`
* Explain how authorization works under the hood
* Explain `Imperative authorization` by example
* Associated repository branch: [authorization](https://github.com/chsakell/aspnet-core-identity/tree/authorization)

## Installation instructions

The project is built with ASP.NET Core with Angular on the client side. 
1. **Visual Studio 2017**: Just open the solution and wait to install the npm packages before running
2. **Without Visual Studio**:
    * `cd ./AspNetCoreIdentity` where the package.json file exist
    * `npm install`
    * `dotnet restore`
    * `dotnet build`
    * `dotnet run`
3. **Create the database** *(required for second part and later)*
    * `cd ./AspNetCoreIdentity` where the AspNetCoreIdentity.csproj exist
    * `dotnet ef migrations add initial_migration`
    * `dotnet ef database update`

> In case you don't want to use SQL Database simply set **InMemoryProvider: true** in the *appsettings.json*

<h3 style="font-weight:normal;">Follow chsakell's Blog</h3>
<table id="gradient-style" style="box-shadow:3px -2px 10px #1F394C;font-size:12px;margin:15px;width:290px;text-align:left;border-collapse:collapse;" summary="">
<thead>
<tr>
<th style="width:130px;font-size:13px;font-weight:bold;padding:8px;background:#1F1F1F repeat-x;border-top:2px solid #d3ddff;border-bottom:1px solid #fff;color:#E0E0E0;" align="center" scope="col">Facebook</th>
<th style="font-size:13px;font-weight:bold;padding:8px;background:#1F1F1F repeat-x;border-top:2px solid #d3ddff;border-bottom:1px solid #fff;color:#E0E0E0;" align="center" scope="col">Twitter</th>
</tr>
</thead>
<tfoot>
<tr>
<td colspan="4" style="text-align:center;">Microsoft Web Application Development</td>
</tr>
</tfoot>
<tbody>
<tr>
<td style="padding:8px;border-bottom:1px solid #fff;color:#FFA500;border-top:1px solid #fff;background:#1F394C repeat-x;">
<a href="https://www.facebook.com/chsakells.blog" target="_blank"><img src="https://chsakell.files.wordpress.com/2015/08/facebook.png?w=120&amp;h=120&amp;crop=1" alt="facebook" width="120" height="120" class="alignnone size-opti-archive wp-image-3578"></a>
</td>
<td style="padding:8px;border-bottom:1px solid #fff;color:#FFA500;border-top:1px solid #fff;background:#1F394C repeat-x;">
<a href="https://twitter.com/chsakellsBlog" target="_blank"><img src="https://chsakell.files.wordpress.com/2015/08/twitter-small.png?w=120&amp;h=120&amp;crop=1" alt="twitter-small" width="120" height="120" class="alignnone size-opti-archive wp-image-3583"></a>
</td>
</tr>
</tbody>
</table>
<h3>License</h3>
Code released under the <a href="https://github.com/chsakell/aspnet-core-identity/blob/master/LICENSE" target="_blank"> MIT license</a>.
