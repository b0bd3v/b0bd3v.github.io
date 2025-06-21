---
title: "IA Para programadores - Parte 1"
description: "Introdução ao Ollama, uma ferramenta de IA para programadores."
layout: post
date: 2025-06-21
categories: [programming, AI]
---

Sou programador a quase duas décadas, e nesse tempo todo nunca me interessei
sobre o assunto IA. Mas recentemente com todo esse hype em torna dela e por uma questão de necessidade, 
já que o mercado está clamando por isso, resolvi dar uma chance. 
Mas por enquanto pensando apenas como uma ferrenta.  
Então resolvi compartilhar meus passos, ainda sim que babysteps, para que outros programadores possam 
acompanhar e aprender junto comigo.


# Ollama

Movido pela curiosidade, não queria apenas utilizar passivamente ferrentas como o chatGPT, Gemini, ou outras APIs de IA. 
Queria algo que pudesse rodar localmente, sem depender de nuvem ou serviços externos. Queria testar modelos de IA diretamente 
no meu computador, de forma simples e prática.
---

## O que é o Ollama?

O Ollama é uma ferramenta que permite rodar modelos de linguagem no seu próprio 
computador, sem precisar de conta, API ou depender da nuvem.

---

## Instalação

A instalação do Ollama é absurdamente simples e rápida. Vou colocar alguns 
comandos para fazer isso no linux, macOS e Windows.

### Linux

```bash
curl -fsSL https://ollama.com/install.sh | sh
```

### macOS (com Homebrew)

```bash
brew install ollama
```

### Windows
Primeiro passo é desinstalar o Windows. 😆

Baixe o instalador em:
👉 [https://ollama.com/download](https://ollama.com/download)

---

### Como iniciar com seu primeiro modelo

Tenha em mente a capacidade do seu computador no momento de baixar os modelos.  

Um modelos que seja mais leve, como o **LLaMA 2**, pode ser uma boa escolha para começar.


No terminal, digite:

```bash
ollama run llama3
```

O Ollama vai baixar o modelo automaticamente. Isso pode demorar alguns minutos na primeira vez, mas é só esperar.

Depois disso, você verá algo como:

```
>
```

Esse `>` indica que você pode conversar com o modelo.

Tente algo como:

```
> Qual a capital do Japão?
```

E ele responderá:

```
Tóquio.
```
