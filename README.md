Página de Teste - Olá, Mundo!

Este é um pequeno projeto para criar uma página HTML simples que exibe a mensagem "Olá, Mundo!" e serve como uma introdução ao aprendizado de HTML e Node.js.

## O que você vai encontrar aqui

Você verá um código HTML básico que faz o seguinte:

1. Exibe a saudação "Olá, Mundo!" em um título grande na página.
2. O título da aba do navegador será "Olá, Mundo! Kauã ta Aprendendo".
3. O código é bem simples, ideal para quem está começando no mundo do desenvolvimento web.

## Estrutura do Código HTML

O código HTML tem a seguinte estrutura:

- **`<!DOCTYPE html>`**: Inicia a definição do tipo de documento, informando que estamos usando HTML5.
- **`<html lang="pt-br">`**: Define que o conteúdo da página será em português (Brasil).
- **`<head>`**: Aqui estão as informações meta da página, como o conjunto de caracteres (`UTF-8`) e a configuração para que a página seja responsiva em dispositivos móveis.
- **`<title>`**: O título da página, que aparece na aba do navegador.
- **`<body>`**: O corpo da página, onde a saudação "Olá, Mundo!" é exibida com uma tag de cabeçalho `<h1>`.

### Como testar esse código no seu navegador

1. Copie o código HTML e cole em um arquivo chamado `index.html`.
2. Abra esse arquivo em seu navegador. Quando você fizer isso, verá a mensagem "Olá, Mundo!" e o título da aba do navegador será "Olá, Mundo! Kauã ta Aprendendo".

### O que aprender com isso

- **HTML básico**: Como criar um arquivo HTML simples.
- **Responsividade**: Como fazer sua página adaptar-se a diferentes tamanhos de tela (mobile, tablet, desktop).
- **Uso de metadados**: Como configurar as informações da sua página, como a codificação de caracteres e o título da página.

### Fazendo o código funcionar com Node.js (opcional)

Se você deseja levar isso para o próximo nível e aprender como servir sua página HTML com Node.js, temos um exemplo de código em Node.js:

1. Crie um arquivo `app.js` no mesmo diretório onde está o `index.html`.
2. Adicione o seguinte código para criar um servidor local que exibe sua página HTML:

```javascript
const http = require('http');
const fs = require('fs');

const server = http.createServer((req, res) => {
    fs.readFile('index.html', (err, data) => {
        if (err) {
            res.writeHead(500, { 'Content-Type': 'text/plain' });
            res.end('Erro ao carregar o arquivo HTML');
            return;
        }
        res.writeHead(200, { 'Content-Type': 'text/html' });
        res.end(data);
    });
});

server.listen(3000, () => {
    console.log('Servidor rodando em http://localhost:3000');
});