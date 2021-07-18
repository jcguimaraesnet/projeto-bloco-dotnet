
# Migrations

**referências:**
- https://docs.microsoft.com/pt-br/ef/core/managing-schemas/migrations/?tabs=dotnet-core-cli
- https://docs.microsoft.com/pt-br/ef/core/cli/dotnet

**steps:**

1. antes de rodar os comandos de migrations, entrar no folder raiz da solução
    ```cmd
    cd <raiz da solution>
    ```

2. instalar cli do ef (entity framework)
    ```cmd
    dotnet tool install --global dotnet-ef
    ```

3. para verificar se ef está instalado na máquina
    ```cmd
    dotnet ef
    ```

4. para usar o ef em um projeto específico, você precisará adicionar uma package ao seu projeto
    ```cmd
    dotnet add <nome do projeto> package Microsoft.EntityFrameworkCore.Design
    ```

5. adicionando um migration ao projeto
    ```cmd
    dotnet ef migrations add <nome do migration> --startup-project <nome do projeto web> --project <nome do projeto de infraestrutura com a classe dbcontext> --context <classe dbcontext> --output-dir <folder onde será gerado os migrations>
    ```

6. aplicando migrations em banco de dados
    ```cmd
    dotnet ef database update --project <nome do projeto de infraestrutura com a classe dbcontext> --context <classe dbcontext> 
    ```









