# 🎬 GL Sync-in-Tap

**Pontuador de trilha sonora para estudantes de música**

> Desenvolvido pelo professor **Glauber Santiago** — DAC/UFSCar  
> 🌐 [servidores.ufscar.br/glauber](http://servidores.ufscar.br/glauber/) · [sites.google.com/view/glauberia](https://sites.google.com/view/glauberia)

---

## 🎯 Para que serve este app?

O **GL Sync-in-Tap** foi criado para facilitar o trabalho de **composição de trilha sonora** para vídeo no **MuseScore**.

O MuseScore não permite carregar um vídeo e sincronizá-lo diretamente. Este app resolve esse problema: você abre o MuseScore em paralelo, configura o andamento e, quando toca uma nota no teclado, o app **detecta o som pelo microfone e inicia o vídeo automaticamente** — tudo em sincronia.

Além disso, o app permite **criar marcas pontuais e contínuas** em momentos específicos do vídeo, exibindo a posição em notação musical (compasso|tempo|subdivisão). Essas marcas são exportadas em formato **MusicXML**, que pode ser importado diretamente no MuseScore para guiar sua composição.

---

## 🚀 Como acessar

O app roda **diretamente no navegador**, sem instalação. Basta abrir o arquivo `index.html` ou acessar o link publicado pelo professor.

> **Recomendado:** Google Chrome ou Microsoft Edge (para melhor compatibilidade com microfone e YouTube).

---

## 📋 Fluxo de trabalho básico

```
1. Abra o MuseScore com sua partitura
2. Abra o GL Sync-in-Tap no navegador (lado a lado na tela)
3. Carregue o vídeo no app
4. Configure o BPM e o compasso iguais ao seu projeto no MuseScore
5. Ative o Gatilho de Áudio (microfone)
6. Toque uma nota no teclado → o vídeo inicia em sincronia
7. Marque os momentos importantes com M (pontual) ou C (contínua)
8. Exporte o MusicXML e importe no MuseScore
```

---

## 🖥️ Painel do App — Seção por Seção

### 📁 Arquivo
| Opção | Descrição |
|---|---|
| **Upload de Vídeo Local** | Abre um arquivo de vídeo do seu computador (MP4, WebM, etc.) |
| **Link do Vídeo** | Cola uma URL do YouTube ou link direto de arquivo MP4 |
| **Importar MusicXML** | Importa um arquivo `.xml` / `.musicxml` com marcas salvas anteriormente |
| **Exportar XML** | Salva todas as marcas em formato MusicXML para importar no MuseScore |

---

### ♩ Andamento & Compasso
Configure o **BPM** (batidas por minuto) e o **compasso** (ex.: 4/4, 3/4, 6/8).

Esses valores determinam como o timecode musical é calculado. **Devem ser iguais aos do seu projeto no MuseScore.**

O timecode musical aparece no canto do vídeo no formato:

```
Compasso | Tempo | Subdivisão
    4   |   2   |    3
```

---

### 🎧 Atraso do Bluetooth (Sincronia A/V)
Se você usa **fone de ouvido Bluetooth**, pode haver um atraso entre o que você ouve e o que vê na tela. Use este painel para compensar esse atraso em milissegundos.

- **Atraso do Áudio (ms):** arraste o slider ou digite o valor em ms.
- **Ativar Sincronização A/V:** liga/desliga a compensação em tempo real.
- **Ajustar marcas existentes:** aplica o offset às marcas já criadas (útil antes de exportar).

> 💡 Fones Bluetooth comuns têm atraso entre 100 ms e 300 ms.

---

### 🎙 Gatilho de Áudio
Esta é a funcionalidade principal para sincronizar com o MuseScore:

1. Clique em **Ligar Escuta** — o app acessa o microfone.
2. Ajuste a **Sensibilidade** conforme o volume do seu instrumento.
3. Quando você **tocar uma nota** (ou bater no teclado), o app detecta o som e **inicia o vídeo automaticamente**.
4. Use o atalho **`S`** para pausar/retomar a escuta a qualquer momento.

> ⚠️ O navegador pedirá permissão para acessar o microfone — clique em "Permitir".

---

### 🔖 Marcas
As marcas são os **pontos de sincronismo** que você anota no vídeo para guiar sua composição.

#### 📍 Marcas Pontuais (`M`)
- Registram um **instante único** no vídeo (ex.: corte, explosão, impacto).
- Aparecem no MusicXML como uma nota curta (semínima com ponto de valor).
- Atalho: tecla **`M`** (durante a reprodução ou com vídeo pausado).

#### 〰 Marcas Contínuas (`C`)
- Registram um **trecho com duração** (ex.: cena de ação, diálogo).
- Clique **uma vez** para iniciar e **outra vez** para terminar a marca.
- Aparecem no MusicXML em pautas separadas ("Contínuas 1", "Contínuas 2", "Contínuas 3") com notas diatônicas sobrepostas (C4, E4, G4, Bb4).
- Atalho: tecla **`C`**.

#### Interações com as marcas
| Ação | Resultado |
|---|---|
| 1 clique simples | Vai para o início da marca no vídeo |
| 2º clique (contínua) | Vai para o fim da marca |
| 3º clique | Desmarca (deseleciona) |
| Clique duplo | Edita o nome e a posição musical da marca |

#### Som das Marcas
Ative **"Som das Marcas"** para ouvir:
- **Clique** nas marcas pontuais.
- **Notas musicais** diatônicas nas marcas contínuas.

---

### ⏱ Ajuste por Frame
Permite mover o vídeo frame a frame para posicionamento preciso.

| Botão / Atalho | Ação |
|---|---|
| `◀ Frame` / `▶ Frame` | Recua/avança 1 frame (30fps) |
| `−10f` / `+5f` etc. | Pula múltiplos frames |
| `←` Seta Esquerda | Recua 1 frame |
| `→` Seta Direita | Avança 1 frame |
| `Shift + ←` | Recua 5 frames |
| `Shift + →` | Avança 5 frames |

---

## ⌨️ Todos os Atalhos de Teclado

| Ação | Tecla |
|---|---|
| Play / Pause do Vídeo | `Espaço` |
| Criar Marca Pontual | `M` |
| Iniciar/Parar Marca Contínua | `C` |
| Voltar 1 Frame | `← Seta Esquerda` |
| Avançar 1 Frame | `Seta Direita →` |
| Voltar 5 Frames | `Shift + ←` |
| Avançar 5 Frames | `Shift + →` |
| Ativar/Pausar Sinc (Microfone) | `S` |
| Ir para Marca Anterior | `[` |
| Ir para Próxima Marca | `]` |

---

## 🎼 Exportando para o MuseScore

1. Após criar todas as marcas, clique em **📤 Exportar XML**.
2. Um arquivo `.musicxml` será baixado com o nome do seu projeto.
3. No MuseScore, vá em **Arquivo → Abrir** e selecione o arquivo exportado.
4. O arquivo abrirá com:
   - Uma **pauta "Sync Track"** com as marcas pontuais (notas de colcheia/16ª em B4, com o nome da marca acima).
   - Pautas **"Contínuas 1", "Contínuas 2", "Contínuas 3"** com as marcas de duração (quando houver).
5. Use essas marcas como **guia visual** ao compor sua trilha.

> 💡 Você também pode **importar** um MusicXML exportado anteriormente para continuar de onde parou.

---

## 🗂️ Arquivo de Exemplo

O repositório inclui o arquivo `meu-exemplo-de-marcas.musicxml` — um exemplo real de marcas exportadas pelo app, gerado no MuseScore Studio 4.6.5. Abra-o no MuseScore para ver como as marcas aparecem na partitura.

---

## ❓ Dúvidas Frequentes

**O microfone não funciona.**
> Verifique se o navegador tem permissão para acessar o microfone. Clique no ícone de cadeado na barra de endereço e permita o acesso ao microfone.

**O vídeo do YouTube não carrega.**
> Certifique-se de copiar a URL completa (ex.: `https://www.youtube.com/watch?v=XXXXXXXXXXX`). Algumas regiões podem ter restrições.

**O timecode não corresponde ao compasso do MuseScore.**
> Verifique se o **BPM** e o **compasso** (numerador/denominador) estão iguais nos dois programas.

**O vídeo e o áudio estão dessincronizados.**
> Use o painel **Atraso do Bluetooth** para ajustar. Experimente valores entre 100 ms e 300 ms se usar fone Bluetooth.

**Posso usar no celular?**
> Sim! O layout se adapta a telas pequenas. O uso do microfone e a navegação frame a frame funcionam melhor no desktop.

---

## 📄 Licença e Créditos

Desenvolvido pelo **Prof. Glauber Santiago** — Departamento de Artes e Comunicação (DAC), Universidade Federal de São Carlos (UFSCar).

- 🌐 [servidores.ufscar.br/glauber](http://servidores.ufscar.br/glauber/)
- 🌐 [sites.google.com/view/glauberia](https://sites.google.com/view/glauberia)
