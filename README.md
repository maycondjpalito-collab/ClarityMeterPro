# 🎚️ Clarity Meter Pro

**Medidor de loudness profissional para Mac. Grátis.**

App de segunda tela + plug-in **VST3**, **AU** (Logic) e **AAX** (Pro Tools) com Loudness Radar, LUFS, True Peak, RTA e correlação de fase.

> Desenvolvido por **Palitomix** · Instagram [@PalitoMix_](https://instagram.com/PalitoMix_)

![Clarity Meter Pro](docs/tela.png)

---

## ⬇️ Download

👉 **[Baixar o instalador — Clarity Meter Pro 1.0.1 (.pkg)](https://github.com/maycondjpalito-collab/ClarityMeterPro/raw/main/downloads/ClarityMeterPro-1.0.1.pkg)**

Instala o app de segunda tela, o dispositivo de áudio e os plug-ins VST3, AU e AAX.

<sub>Prefere instalar à mão? [Versão manual (.zip)](https://github.com/maycondjpalito-collab/ClarityMeterPro/raw/main/downloads/ClarityMeterPro-1.0.1-macOS.zip)</sub>

**Requisitos:** macOS 10.15 (Catalina) ou mais novo · Apple Silicon (M1, M2, M3, M4…) ou Intel.

---

## ✨ O que ele mede

| | |
|---|---|
| 📡 **Loudness Radar** | Histórico do Short Term girando + anel de LEDs com o Momentary, resolução de 3, 6, 9 ou 12 dB |
| 🔊 **LUFS** | Integrado (Program Loudness), Short Term, Momentary, Loudness Range (LRA) e máximos — padrão **EBU R128 / ITU-R BS.1770** |
| ⚠️ **True Peak** | Barras L/R até +3 dBTP com marcador de pico branco (segura 3 s quando passa de 0 dBTP) |
| 📊 **RTA** | 31 bandas de 1/3 de oitava |
| 🎧 **Estéreo** | Vectorscope, correlação, Balance-o-Meter e Mono Deviation |
| 🎯 **Alvos** | +20 prontos (Spotify, Apple Music, YouTube, Amazon, Tidal, Deezer, EBU R128, ATSC A/85, podcast, Music Mastering) ou valor personalizado |
| 🎨 **Temas** | Vários temas de cores |

O áudio passa pelo plug-in **sem nenhuma alteração**: ele só mede.

---

## 🛠️ Como instalar

1. Baixe o **`ClarityMeterPro-1.0.1.pkg`** e dê **dois cliques**.
2. Siga as telas: **Continuar → Concordo → Instalar** e digite a senha do Mac.
3. Quer só alguns itens? Na tela **Tipo de Instalação**, clique em **Personalizar** e escolha:
   app, dispositivo de áudio, VST3, AU e/ou AAX.

| Item | Pasta |
|---|---|
| App | `Aplicativos` |
| Dispositivo de áudio | `/Library/Audio/Plug-Ins/HAL` |
| VST3 | `/Library/Audio/Plug-Ins/VST3` |
| AU | `/Library/Audio/Plug-Ins/Components` |
| AAX | `/Library/Application Support/Avid/Audio/Plug-Ins` |

### 🔒 O macOS não deixou abrir o instalador?
Ele aparece como "de desenvolvedor não identificado". Abra **Ajustes do Sistema → Privacidade e Segurança**, role até o aviso do `ClarityMeterPro-1.0.1.pkg` e clique em **Abrir Mesmo Assim** (no macOS mais antigo: botão direito no arquivo → **Abrir**).

---

## 🎛️ Como usar

### Na DAW (plug-in)
Coloque o **Clarity Meter Pro** no **último insert do Master**.

- **Pro Tools (AAX):** categoria **Sound Field**, fabricante Palitomix. Insira como *multichannel → stereo*.
- **Logic Pro (AU):** Audio Units → Palitomix → Clarity Meter Pro.
- **Cubase, Studio One, Reaper, Ableton, FL Studio… (VST3):** procure por Palitomix / Clarity Meter Pro.

### App de segunda tela
Mede tudo o que sai do Mac: DAW, player, navegador.

1. Abra o **Clarity Meter Pro** em Aplicativos (o dispositivo de áudio "Clarity Meter Pro" já foi instalado pelo instalador).
2. Em **Opções (⌘,)**: entrada = **Clarity Meter Pro**, saída = sua interface de áudio.
3. Com o roteamento automático ligado, o som continua saindo nos seus monitores e o medidor mostra tudo.

**Atalhos:** `R` zera · `M` troca Radar / RTA / Scope · `T` troca o tema · `Espaço` inicia/para · roda do mouse = alvo (±1 LU; com Option ±0,5).

---

## 📄 Licença

**Freeware**: grátis para uso pessoal e profissional (pode usar em trabalhos pagos). Veja [`LICENCA.txt`](LICENCA.txt).
Avisos de componentes de terceiros: [`AVISOS-DE-TERCEIROS.txt`](AVISOS-DE-TERCEIROS.txt).
O dispositivo de áudio do app é baseado no BlackHole (GPL v3); o código dele está em [`codigo-do-driver`](codigo-do-driver).

Este projeto é independente e **não tem afiliação** com a TC Electronic, a Music Tribe, a Avid ou a Steinberg. As marcas citadas pertencem aos seus donos.

---

Feito em Campo Grande – MS por **Palitomix**. Se o medidor te ajudou, marca o [@PalitoMix_](https://instagram.com/PalitoMix_) e compartilha! ⭐
