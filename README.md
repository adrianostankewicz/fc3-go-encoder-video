# FC3 Go Encoder Video

Serviço de codificação de vídeos em Go com FFmpeg e Bento4.

## Sobre

Aplicação para processamento e codificação de arquivos de vídeo. O sistema gerencia vídeos e trabalhos de codificação em um banco de dados PostgreSQL.

## Tecnologias

- **Go** 1.14+
- **PostgreSQL** (produção) / **SQLite** (testes)
- **FFmpeg** + **Bento4**
- **GORM** (ORM)

## Estrutura

```
├── domain/           # Modelos (Video, Job)
├── application/      # Casos de uso
├── framework/        # Drivers e APIs
├── Dockerfile
└── docker-compose.yaml
```

## Como executar

### Com Docker

```bash
git clone https://github.com/adrianostankewicz/fc3-go-encoder-video.git
cd fc3-go-encoder-video
docker-compose up -d
```

## Configuração

Edite `.env`:

```env
DB_TYPE="postgres"
DNS="dbname=encoder sslmode=disable user=postgres password=root host=localhost"
ENV="dev"
DEBUG=true
AUTO_MIGRATE_DB=true
```
