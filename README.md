# GroControleContas
Um projeto simples de Registro e Login de contas

Passos
1. Criar uma aplicação MVC com autenticação individual
2. instalar o package Pomelo.EntityFrameworkCore.Mysql
3. Alterar string de conexão no appsetings
4. configurar o "configureServices": Utilizar o script abaixo (substituir):

var connectionString = builder.Configuration.GetConnectionString("DefaultConnection");
builder.Services.AddDbContext<ApplicationDbContext>(options =>
    options.UseMySql(connectionString, ServerVersion.AutoDetect(connectionString)));

5. Excluir pasta migrations (Caso já tenho uma)
6. Criar novo migrations; add-migrations inicial
7. update da base do mysql: update-database

Obs: Video de apoio: https://www.youtube.com/watch?v=i5L3wsnYMEE&ab_channel=DataVids



