# Learning Journal
so today we take about Identity and how to use it in the project.

first the identity in simple term it someplace created for users data and the authentications specially and have funcinality for that.


after we add Identity to our project we can see that we have now around 7 new tabels this all tabels to use the identity in what wvwer we want.

## steps to implement identity  in the project


first of all we need to add dependecy from NuGet package called `Microsoft.aspNetcore.Identity.EntityFrameworkCore`.

then in data folder (context) we replase the inhert from `DbContext` to `IdentityDbContext` then in the same folder we make sure that we have this line `base.OnModelCreating(modelBuilder);`

then from `startup.cs` go to `services` then add 
```
services.AddIdentity<AddIdentity<ApplicationUser, IdentityRole>()
        .AddEntityFrameworkStores<ApplicationDbContext>();
```
then go to  `Configure` then add this `app.UseAuthentication();` 

 last thing we add the `add migration` then `update database`.
