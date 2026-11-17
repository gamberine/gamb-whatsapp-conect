# Gamb WhatsApp Conect | MVP 1.2

## Objetivo
Evoluir o MVP 1.1 com transcrição manual de mensagens de voz e futura integração autorizada à WhatsApp Business Platform.

## Implementação local validada
- Nova aba **Transcrever áudios**, upload manual e transcrição por serviço speech-to-text
- Formatos: MP3, MP4, M4A, WAV, WebM, OGG e MPEG; limite de 20 MB
- API no servidor Node.js: `/api/transcription/status` e `POST /api/transcribe`
- Chave de API apenas no servidor, via `OPENAI_API_KEY`
- Copiar texto e criar tarefa; sem armazenar o áudio automaticamente
- 11 testes locais aprovados, sintaxe aprovada

## Limitações e critérios de aceite
- A captura automática do WhatsApp ainda não existe. Não confundir importação manual com integração oficial.
- Chave de API ausente: UI informa indisponibilidade. Não simular transcrição.
- Transcrições são enviadas a provedor externo: avaliar LGPD, consentimento e retenção.
- Antes da produção, adicionar login, rate limit, custos, logs e HTTPS.
- O código executável está preparado no pacote MVP 1.2 desta conversa e precisa ser enviado ao repositório. Este arquivo é documentação de acompanhamento, **não comprova publicação do código-fonte**.

## Fluxo de versionamento
- Base: `main`
- Desenvolvimento: `feat/audio-transcription-mvp-1-2`
- Revisar configurações de proteção da `main`, CI, dependências e secrets antes de produção.
