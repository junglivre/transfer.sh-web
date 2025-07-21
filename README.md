# transfer.sh-web

Este repositório contém o frontend web para [transfer.sh](https://github.com/dutchcoders/transfer.sh/), um serviço de compartilhamento de arquivos via linha de comando.

## Estrutura do Projeto

O projeto contém as seguintes páginas:
- `index.html` - Página principal
- `download.html` - Página de download padrão
- `download.audio.html` - Visualizador de arquivos de áudio
- `download.image.html` - Visualizador de imagens
- `download.video.html` - Visualizador de vídeos
- `download.markdown.html` - Visualizador de arquivos markdown
- `download.sandbox.html` - Ambiente sandbox para visualização segura

## Como Usar

Para executar o serviço, você precisa especificar o diretório `web-path` apontando para a pasta que contém os arquivos HTML.

Exemplo com Docker:
```bash
docker run -d \
  -v /pasta/uploads:/uploads \
  -v /pasta/web:/webapp \
  --publish 5000:8080 \
  dutchcoders/transfer.sh:latest \
  --provider local \
  --basedir /uploads \
  --web-path /webapp/
```

## Licença
Veja o arquivo [LICENSE](LICENSE) para detalhes.
