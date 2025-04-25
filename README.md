# DockerdotnetApp

Aplicação ASP.NET 9 Web API rodando em container Docker. Criada e testada via WSL no Ubuntu, com Docker rodando no Windows 10.

## 🔧 Tecnologias

- .NET 9
- ASP.NET Core Web API
- Docker
- Ubuntu via WSL

## 🚀 Como executar

### Build da imagem Docker

```bash
docker build -t dockerdotnetapp .
docker run -d -p 8081:8080 dockerdotnetapp
```
![image](https://github.com/user-attachments/assets/3206ae63-84c2-46f5-a829-f51b6cd6c4e7)

A API estará disponível em:
http://localhost:8081/weatherforecast
```json
[{"date":"2025-04-26","temperatureC":42,"summary":"Balmy","temperatureF":107},{"date":"2025-04-27","temperatureC":41,"summary":"Hot","temperatureF":105},{"date":"2025-04-28","temperatureC":-2,"summary":"Mild","temperatureF":29},{"date":"2025-04-29","temperatureC":-5,"summary":"Hot","temperatureF":24},{"date":"2025-04-30","temperatureC":50,"summary":"Scorching","temperatureF":121}]
```

📌 Observações
A porta 8080 está configurada no container, e mapeada para 8081 no host.

O nginx pode estar rodando na porta 8080 do host, então evitamos conflito com -p 8081:8080.
