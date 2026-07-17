# rafaelfonseca.ai — versão premium (deploy)

Site estático pronto para produção. Sem build, sem dependências.
A foto do hero referencia `assets/rafael.jpg` (34KB, com cache do navegador).

## Deploy em 4 passos

### 1. Subir para o GitHub
No terminal, dentro desta pasta (ou peça ao Claude Code: "suba esta pasta para um novo repositório no meu GitHub"):

```bash
git init
git add .
git commit -m "Site premium v1"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/rafaelfonseca-ai.git
git push -u origin main
```

Sem terminal: crie o repositório em github.com/new e arraste os arquivos
(index.html e a pasta assets) em "uploading an existing file".

### 2. Conectar à Vercel
- vercel.com > login com GitHub > Add New > Project > importe o repositório
- Framework Preset: **Other** | Build Command: **vazio** | Output Directory: **vazio**
- Deploy. Em ~1 min o site está em `SEU-PROJETO.vercel.app`

### 3. Apontar o domínio rafaelfonseca.ai
No projeto da Vercel: Settings > Domains > adicione `rafaelfonseca.ai`.
No registrador do domínio, configure o que a Vercel indicar:
- Registro **A** do domínio raiz -> `76.76.21.21`
- **CNAME** do `www` -> `cname.vercel-dns.com`
HTTPS é automático. Propagação: de minutos a algumas horas.

## Fluxo de atualização
Todo `git push` na main publica sozinho. Abra esta pasta no Claude Code e peça
a mudança + "commit e push": em segundos está no ar. Zero créditos do Lovable.

## Checklist pós-deploy
- [ ] Testar o botão do WhatsApp no celular
- [ ] Testar navegação do topo e o carrossel de projetos (setas e swipe)
- [ ] Conferir preview social (og:image) ao compartilhar o link
