# Identity

**referências:**
- https://docs.microsoft.com/pt-br/aspnet/core/security/authentication/identity
- https://docs.microsoft.com/pt-br/aspnet/core/security/authentication/scaffold-identity


1. add scaffolding identity

2. alterar appsettings para usar um mesmo database (opcional)

3. add migrations identity e update database
    ```cmd
    dotnet ef migrations add AddInitIdentityMigration --startup-project WebApplication1  --project WebApplication1 --context IdentityDBContext --output-dir Areas/Identity/Data/Migrations
    ```

    ```cmd
    dotnet ef database update --project WebApplication1 --context IdentityDBContext
    ```

4. startup identity => configurar password (opcional)

5. startup => usar autenticação
    ```csharp 
    app.UseAuthentication();
    app.UseAuthorization();
    ```

6. startup => mapear rotas páginas razor
    ```csharp
    endpoints.MapRazorPages();
    ```

7. decorar controllers/actions authorizadas e anonimas
    ```csharp
    [Authorize] ou [AllowAnonymous]
    ```

8. add partial view
    ```csharp
    <partial name="_LoginPartial" /> na pág de layout (após <ul> navbar-nav)
    ```

