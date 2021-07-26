# Identity

**referências:**
- https://docs.microsoft.com/pt-br/aspnet/core/security/authentication/add-user-data


1. mover classe usuário para um projeto de library (camada de domínio)

2. adicionar propriedades a entidade usuario

3. trazer o hosting startup do identity para o default do app.

4. mover a classe de dbcontext para um projeto de library (camada de infra)
   - instalar packages
     - Microsoft.EntityFrameworkCore
     - Microsoft.EntityFrameworkCore.Tools
     - Microsoft.EntityFrameworkCore.SqlServer

5. criar migration relacionado as novas propriedades criadas na entidade usuário

6. atualizar banco de dados com o migration criado anteriormente.




