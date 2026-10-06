# Hermes Zero-to-Hero

A static, bilingual (English and Turkish) visual guide to operating [Hermes Agent](https://github.com/NousResearch/hermes-agent) from the terminal.

**Status:** published. Commands were checked against Hermes Agent v0.21.5 (2026-09-24) on 2026-10-06. The guide is unofficial and not affiliated with Nous Research.
**Live site:** <https://hermes-guide.neurabytelabs.com> ([English](https://hermes-guide.neurabytelabs.com/en/), [Türkçe](https://hermes-guide.neurabytelabs.com/tr/))

## What this is

The guide describes one working loop: inspect the current state, plan a change, act with real tools, and keep what worked. It includes setup commands (`hermes setup`, `hermes doctor`, `hermes model`), memory and skills, the messaging gateway, scheduled jobs, MCP servers, and an animated ASCII walkthrough.

The site is plain HTML. It has no build step and no dependencies.

## Run locally

```bash
python3 -m http.server 8000
# open http://localhost:8000/en/
```

Or build the container that production uses:

```bash
docker build -t hermes-guide .
docker run --rm -p 8080:80 hermes-guide
```

## Repository layout

| Path | Content |
|------|---------|
| `index.html` | Language selector |
| `en/index.html` | English guide |
| `tr/index.html` | Turkish guide |
| `voice-to-knowledge/index.html` | ASCII animation companion page |
| `Dockerfile` | `nginx:alpine` image that serves the files |

## License

- Text and written content: [CC BY 4.0](LICENSE). Reuse is allowed with attribution, a link to the license, and a note of any changes.
- Code (HTML, CSS and JavaScript in the pages, `Dockerfile`): [MIT](LICENSE-CODE).

## Author

[Mustafa Saraç](https://twitter.com/0xsarac), [NeuraByte Labs](https://neurabytelabs.com).

---

## Türkçe

Hermes Agent'ı terminalden kullanmak için hazırlanmış, statik ve iki dilli (İngilizce, Türkçe) görsel rehber. [Hermes Agent](https://github.com/NousResearch/hermes-agent) için resmi olmayan bir rehberdir; Nous Research ile bağlantısı yoktur.

**Durum:** yayında. Komutlar 2026-10-06'da Hermes Agent v0.21.5 (2026-09-24) ile karşılaştırıldı.
**Canlı site:** <https://hermes-guide.neurabytelabs.com> ([Türkçe rehber](https://hermes-guide.neurabytelabs.com/tr/))

Site düz HTML'dir. Derleme adımı yoktur. Yerelde açmak için yukarıdaki "Run locally" bölümündeki komutları kullan.

**Lisans:** Metin [CC BY 4.0](LICENSE) altındadır; atıf, lisans bağlantısı ve değişiklik notu ile yeniden kullanılabilir. Kod [MIT](LICENSE-CODE) altındadır.
