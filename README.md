# GL Sync-in-Tap

Aplicação web para sincronizar vídeo com marcações musicais em tempo real, ajudando no processo de criação de trilha sonora com integração a arquivos MusicXML (MuseScore).

## O que este repositório contém

Este repositório contém uma aplicação front-end em arquivo único (`index.html`) que permite:

- carregar vídeo local (`.mp4`) ou link do YouTube;
- criar marcas pontuais e contínuas sincronizadas ao vídeo;
- ajustar BPM, compasso e compensação de atraso A/V;
- importar e exportar marcações em MusicXML;
- salvar e reabrir projetos em `.txt`.

## Estrutura principal

- `/home/runner/work/gl-sync-video-in-tap/gl-sync-video-in-tap/index.html` — aplicação principal (HTML, CSS e JavaScript);
- `/home/runner/work/gl-sync-video-in-tap/gl-sync-video-in-tap/meu-exemplo-de-marcas.musicxml` — exemplo de arquivo MusicXML;
- `/home/runner/work/gl-sync-video-in-tap/gl-sync-video-in-tap/Gl-Sync-in-tap.mp4` — vídeo de exemplo;
- `/home/runner/work/gl-sync-video-in-tap/gl-sync-video-in-tap/parede.png` — imagem usada na interface.

## Como executar

Como é uma aplicação estática, basta abrir o arquivo `index.html` no navegador.

Opcionalmente, você pode servir localmente com qualquer servidor HTTP simples.

## Objetivo

Facilitar o workflow de estudantes e compositores que precisam marcar eventos musicais em vídeo e levar esse material para edição no MuseScore.

## Preview

<img width="827" height="716" alt="GL Sync-in-Tap preview" src="https://github.com/user-attachments/assets/d329a3e1-4a85-4d1e-8d19-2979f3330e66" />
