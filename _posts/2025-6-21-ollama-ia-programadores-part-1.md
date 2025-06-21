----
title: "IA Para programadores - Parte 1"
description: "Introdução ao Ollama, uma ferramenta de IA para programadores."
layout: post
date: 2025-06-21
categories: [programming, AI]
----

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

Simples assim.

---

[//]: # ()
[//]: # (## Dicas úteis)

[//]: # ()
[//]: # (* Para sair do modo de conversa: `Ctrl + C`.)

[//]: # (* Para testar outros modelos:)

[//]: # (  Ex: `ollama run mistral`, `ollama run gemma`)

[//]: # (* Para ver os modelos instalados:)

[//]: # ()
[//]: # (```bash)

[//]: # (ollama list)

[//]: # (```)

[//]: # ()
[//]: # (* Para baixar um modelo sem rodar:)

[//]: # ()
[//]: # (```bash)

[//]: # (ollama pull nome-do-modelo)

[//]: # (```)

[//]: # ()
[//]: # (---)

[//]: # ()
[//]: # (## E assim você pode dar seus primeiros passos com IA.)

[//]: # ()
[//]: # (Mesmo que você não entenda nada sobre inteligência artificial, o Ollama permite explorar esse universo de forma prática e acessível — direto do seu terminal.)

[//]: # ()
[//]: # (---)
[//]: # ()
[//]: # (## Executando o servidor local do Ollama)

[//]: # ()
[//]: # (Além do modo interativo, o Ollama também pode rodar como um **servidor HTTP local**, escutando na porta `11434`.)

[//]: # ()
[//]: # (Isso permite que você envie prompts via código, em qualquer linguagem que suporte requisições HTTP.)

[//]: # ()
[//]: # (Para iniciar o servidor, basta rodar:)

[//]: # ()
[//]: # (```bash)

[//]: # (ollama serve)

[//]: # (```)

[//]: # ()
[//]: # (Esse comando inicia o Ollama em modo servidor. Ele continuará rodando enquanto o terminal estiver aberto.)

[//]: # ()
[//]: # (---)

[//]: # ()
[//]: # (## Exemplo prático com Ruby)

[//]: # ()
[//]: # (Aqui está um exemplo simples em Ruby usando o servidor local do Ollama. Ele envia um prompt e imprime a resposta:)

[//]: # ()
[//]: # (```ruby)

[//]: # (require 'net/http')

[//]: # (require 'json')

[//]: # ()
[//]: # (uri = URI&#40;'http://localhost:11434/api/generate'&#41;)

[//]: # ()
[//]: # (req = Net::HTTP::Post.new&#40;uri, 'Content-Type' => 'application/json'&#41;)

[//]: # (req.body = {)

[//]: # (  model: 'llama3',)

[//]: # (  prompt: 'Explique o que é Ruby em poucas palavras.')

[//]: # (}.to_json)

[//]: # ()
[//]: # (res = Net::HTTP.start&#40;uri.hostname, uri.port&#41; { |http| http.request&#40;req&#41; })

[//]: # ()
[//]: # (puts JSON.parse&#40;res.body&#41;["response"])

[//]: # (```)

[//]: # ()
[//]: # (Esse script roda uma pergunta para o modelo `llama3` e imprime a resposta no terminal.)

[//]: # ()
[//]: # (---)

[//]: # ()
[//]: # (## Próximos passos)

[//]: # ()
[//]: # (Nos próximos posts, pretendo mostrar como usar isso dentro de aplicações reais, criar APIs simples com IA e integrar com outras ferramentas.)

[//]: # (Mas o mais importante é isso: **você pode começar agora, de forma simples, e aprender aos poucos**.)
