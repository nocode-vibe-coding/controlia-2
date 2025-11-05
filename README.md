# ControlAI - Template do Curso "Do Zero ao App"

> **Template exclusivo para alunos do módulo Vibe Coding Avançado da [NoCode StartUp](https://nocodestartup.io/)**

Este repositório é um template criado especificamente para que os alunos acompanhem as aulas ministradas no módulo **Vibe Coding Avançado** que se chama **"Do Zero ao App"** da escola **[NoCode StartUp](https://nocodestartup.io/)**.

## 📚 Sobre o Curso

Este template faz parte de um curso privado da **[NoCode StartUp](https://nocodestartup.io/)**, onde você aprenderá a desenvolver uma plataforma SaaS Multi-tenant completa do zero, utilizando o Cursor como ferramenta principal de desenvolvimento.

### 🎯 Objetivo do Projeto

O **ControlAI** é uma Plataforma de Inteligência Artificial Privada (SaaS Multi-tenant) que servirá como MVP (Produto Mínimo Viável) do curso. Esta plataforma permitirá que empresas (Tenants) se inscrevam, gerenciem seus colaboradores e utilizem modelos de LLM (como OpenAI/Claude) sob um contexto seguro e privado.

## 🚀 Como Começar

### 1. Criar seu repositório a partir do template

1. Acesse o repositório template: [https://github.com/NoCode-StartUp/controlia-1.0.git](https://github.com/NoCode-StartUp/controlia-1.0.git)
2. Clique no botão **"Use this template"** (verde, no topo da página)
3. Escolha **"Create a new repository"**
4. Preencha:
   - **Owner**: Sua conta do GitHub
   - **Repository name**: Nome do seu repositório (ex: `controlia-meu-projeto`)
   - **Visibility**: Public ou Private (escolha conforme preferir)
5. Clique em **"Create repository from template"**

### 2. Clonar o repositório localmente

```bash
git clone https://github.com/SEU-USUARIO/SEU-REPOSITORIO.git
cd SEU-REPOSITORIO
```

### 3. Verificar a branch atual

Ao clonar, você já estará na branch `inicio`, que contém o projeto inicial do Lovable pronto para começar.

```bash
# Verificar branch atual
git branch

# Ver todas as branches disponíveis
git branch -a
```

### 4. Criar sua branch de trabalho

Para cada aula, crie uma branch de trabalho seguindo o padrão `aula-XX-a`:

```bash
# Para a aula 01
git checkout -b aula-01-a

# Para a aula 02
git checkout -b aula-02-a

# Para a aula 03
git checkout -b aula-03-a
```

## 📋 Padrão de Branches

Este repositório utiliza uma estrutura de branches clara para separar o trabalho do professor e do aluno:

### Branches Principais

- **`inicio`** (default branch) - Projeto inicial do Lovable, estado limpo para começar
- **`main`** (protegida) - Projeto completo final, apenas para referência

### Branches do Professor (Referência)

- **`aula-XX-p`** (p = professor) - Solução completa do professor para cada aula
  - Use apenas para **comparar** sua solução ao final da aula
  - **NÃO trabalhe diretamente** nessas branches

### Branches do Aluno (Trabalho)

- **`aula-XX-a`** (a = aluno) - Sua branch de trabalho para cada aula
  - **Crie esta branch** para trabalhar em cada aula
  - Faça seus commits aqui durante a aula

#### Exemplo de Branches Disponíveis:

```
inicio              → Projeto inicial (comece aqui)
aula-01-p           → Solução do professor - Aula 01 (referência)
aula-01-a           → Seu trabalho - Aula 01 (você cria)
aula-02-p           → Solução do professor - Aula 02 (referência)
aula-02-a           → Seu trabalho - Aula 02 (você cria)
aula-03-p           → Solução do professor - Aula 03 (referência)
aula-03-a           → Seu trabalho - Aula 03 (você cria)
... (uma branch por aula)
main                → Projeto completo final (referência)
```

## 📖 Como Trabalhar com as Branches

### Seguindo uma aula específica

```bash
# 1. Ver todas as branches disponíveis
git branch -a

# 2. Ver a solução do professor (opcional, para entender o objetivo)
git checkout aula-03-p
git log  # Ver o que o professor implementou
git checkout inicio  # Voltar para a branch inicial

# 3. Criar sua branch de trabalho
git checkout -b aula-03-a

# 4. Trabalhar na aula normalmente
# ... seguir a aula e implementar junto ...
git add .
git commit -m "Minha implementação da aula 03"
git push origin aula-03-a

# 5. Ao final da aula, comparar com a solução do professor
git diff aula-03-p

# Ou verificar a solução completa
git checkout aula-03-p
# (depois volte para sua branch)
git checkout aula-03-a
```

### Comparar seu trabalho com a solução do professor

```bash
# Ver diferenças entre sua branch e a solução do professor
git diff aula-03-p

# Ver quais arquivos foram modificados
git diff --name-only aula-03-p

# Ver estatísticas de mudanças
git diff --stat aula-03-p
```

### Se se perder durante a aula

```bash
# Voltar para a branch inicial e recomeçar
git checkout inicio
git checkout -b aula-03-a-v2  # Criar nova versão
```

## 🎯 Como Seguir o Curso Corretamente

### ⚠️ ORDEM DAS AULAS É ESSENCIAL

**NÃO pule aulas!** Cada aula prepara o terreno para a próxima.

### 📋 Fluxo Correto para Cada Aula:

1. **Verifique a aula atual** (ex: Aula 03)
2. **Crie sua branch de trabalho**:
   ```bash
   git checkout -b aula-03-a
   ```
3. **Siga a aula e implemente junto**
4. **Faça commits conforme avança**:
   ```bash
   git add .
   git commit -m "Implementando funcionalidade X"
   git push origin aula-03-a
   ```
5. **Ao final, compare com a solução do professor** (opcional):
   ```bash
   git diff aula-03-p  # Ver diferenças
   ```

### ❌ O QUE NÃO FAZER:

- ❌ **Não trabalhe diretamente nas branches `aula-XX-p`** - Elas são apenas para referência
- ❌ **Não pule aulas** - Você vai se perder
- ❌ **Não faça checkout de `main`** - Ela tem o projeto completo
- ❌ **Não trabalhe na branch `inicio` diretamente** - Crie sempre uma branch `aula-XX-a`

### ✅ O QUE FAZER:

- ✅ **Sempre crie uma branch `aula-XX-a` para cada aula**
- ✅ **Siga as aulas na ordem**
- ✅ **Use as branches `aula-XX-p` apenas para comparar no final**
- ✅ **Faça commits frequentes durante a aula**

## ⚠️ Importante

- **NÃO use a branch `main` diretamente para trabalhar!** Ela contém o projeto completo final.
- **Sempre crie uma branch `aula-XX-a`** para trabalhar em cada aula.
- **As branches `aula-XX-p` são apenas para referência** - não trabalhe nelas diretamente.
- Se se perder em alguma aula, volte para a branch `inicio` e crie uma nova branch `aula-XX-a`.

## 📄 Sobre o Projeto ControlAI

### Visão Geral

O **ControlAI** é uma Plataforma SaaS Multi-tenant que permite que empresas:

- Se inscrevam e gerenciem seus colaboradores
- Utilizem modelos de LLM (OpenAI/Claude) sob contexto seguro e privado
- Gerenciem múltiplos agentes de IA customizados
- Tenham controle total sobre seus custos de tokens (modelo BYOK - Bring Your Own Key)

### Stack Tecnológica

- **Framework**: React & Vite
- **Roteamento**: React Router DOM
- **Banco de Dados**: Supabase (PostgreSQL, Auth, RLS, Storage)
- **Pagamentos**: Stripe (Assinaturas SaaS)
- **E-mails**: Resend (E-mails Transacionais)
- **IA/LLM**: OpenAI/Claude (Via Chave BYOK) e AI SDK
- **Hosting**: Vercel
- **UI/Design**: Shadcn UI

### Pilares do Produto

1. **Segurança Multi-tenant (RLS)**: Segregação estrita de dados entre empresas
2. **Modelo BYOK**: Cliente fornece sua própria chave API de LLM
3. **Gestão Completa**: Painéis separados para Admin Master e Admin Tenant
4. **Foco na Conversão**: Landing Page e Pricing otimizados

> Para mais detalhes sobre o projeto, consulte o **PRD (Product Requirements Document)** disponível nas aulas do curso.

## 🛠️ Tecnologias Utilizadas

Este projeto foi criado com:

- [Vite](https://vitejs.dev/)
- [TypeScript](https://www.typescriptlang.org/)
- [React](https://react.dev/)
- [shadcn-ui](https://ui.shadcn.com/)
- [Tailwind CSS](https://tailwindcss.com/)

## 📚 Recursos Adicionais

- **Repositório Template**: [https://github.com/NoCode-StartUp/controlia-1.0.git](https://github.com/NoCode-StartUp/controlia-1.0.git)
- **NoCode StartUp**: [Escola de desenvolvimento NoCode/LowCode](https://nocodestartup.io/)
- **Curso**: Vibe Coding Avançado - "Do Zero ao App"

## 🤝 Suporte

Este template é exclusivo para alunos do curso "Do Zero ao App" da [NoCode StartUp](https://nocodestartup.io/). Para dúvidas sobre o curso, consulte os canais de suporte da escola.

---

**Desenvolvido exclusivamente para o curso "Do Zero ao App" da [NoCode StartUp](https://nocodestartup.io/)**

