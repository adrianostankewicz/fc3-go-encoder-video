# FC3 Go Encoder Video

Serviço de codificação de vídeos em Go com FFmpeg e Bento4.

## 📋 Sobre

Aplicação para processamento e codificação de arquivos de vídeo. O sistema gerencia vídeos e trabalhos de codificação em um banco de dados PostgreSQL.

## 🛠️ Tech Stack

- **Go** 1.14+
- **PostgreSQL** (produção) / **SQLite** (testes)
- **FFmpeg** + **Bento4**
- **GORM** (ORM)

## 📁 Estrutura

```
├── domain/           # Modelos (Video, Job)
├── application/      # Casos de uso
├── framework/        # Drivers e APIs
├── Dockerfile
└── docker-compose.yaml
```

## 🚀 Quick Start

### Com Docker

```bash
git clone https://github.com/adrianostankewicz/fc3-go-encoder-video.git
cd fc3-go-encoder-video
docker-compose up -d
```

### Localmente

```bash
go mod download
go test ./...
go build -o encoder
```

## ⚙️ Configuração

Edite `.env`:

```env
DB_TYPE="postgres"
DNS="dbname=encoder sslmode=disable user=postgres password=root host=localhost"
ENV="dev"
DEBUG=true
AUTO_MIGRATE_DB=true
```

## 🧪 Testes

```bash
go test ./...
```

## 📝 Modelos

- **Video**: Arquivo de vídeo a ser codificado
- **Job**: Trabalho de codificação de um vídeo

## 📄 Licença

MIT
