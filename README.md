# Envista MVP

MVP frontend navegável da plataforma Envista, construído com Next.js, React, TypeScript e CSS responsivo. Não há backend, banco de dados, autenticação real, pagamentos ou upload real de arquivos.

## Rodar localmente

```bash
npm install
npm run dev
```

Depois abra `http://localhost:3000`.

## Demonstrações rápidas

Na rota `/login` existem dois atalhos:

- Demo Participante — Lucas Ferreira
- Demo Investidor — Marina Alves / Horizonte Ventures

## O que funciona no frontend

- login simulado e seleção de role;
- cadastro/onboarding visual;
- navegação participante e investidor;
- criação de projetos e equipes;
- projetos detalhados, comentários, salvar e acompanhar;
- descoberta com busca/filtro;
- competições e inscrição simulada;
- cursos, aulas e progresso salvo;
- projeto final do curso adicionado ao portfólio;
- mensagens locais;
- interesse de investidor criando contexto de conversa;
- notificações;
- busca global com `Ctrl + K`;
- perfil e conquistas;
- landing, sobre e página para escolas;
- responsividade para desktop/tablet/mobile.

As principais mudanças são persistidas em `localStorage` com prefixo `envista:`.

## Arquitetura

- `app/` — App Router e estilos globais
- `components/EnvistaApp.tsx` — composição das telas e interações do MVP
- `data/mock.ts` — dados mockados centralizados
- `types/` — modelos conceituais
- `lib/storage.ts` — camada simples de persistência local
- `public/envista-logo.png` — logo fornecida

A camada de dados foi separada para facilitar a troca futura de `localStorage`/mocks por APIs reais.

## Segurança

Este MVP não afirma criptografia, autenticação ou segurança que não existem. Mensagens, login e ações são apenas simulações locais. A implementação futura deve incluir autenticação, autorização/RBAC, persistência segura, proteção de arquivos, políticas de privacidade, LGPD, auditoria e uma camada real de mensagens.
