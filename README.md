# Projeto Less

Este projeto demonstra como utilizar o pré-processador Less para simplificar o desenvolvimento de estilos CSS.

## Pré-requisitos

Antes de começar, certifique-se de ter o Node.js instalado em seu sistema. Você pode baixar e instalar o Node.js a partir do site oficial [nodejs.org](https://nodejs.org/en/).

## Instalação

1. **Inicialize um projeto npm:**
   Execute o seguinte comando no terminal para iniciar um novo projeto npm:

   ```
   npm init
   ```

2. **Instale o Less:**
   Instale o Less como uma dependência de desenvolvimento executando o seguinte comando:

   ```
   npm install --save-dev less
   ```

3. **Inicialize um repositório Git:**
   Se ainda não tiver um, inicie um novo repositório Git com o seguinte comando:
   ```
   git init
   ```

## Uso

### Compilação manual do Less para CSS

Você pode compilar manualmente seus arquivos Less em CSS executando o seguinte comando:

```
npm run less
```

Este comando compilará o arquivo `./src/styles/main.less` em `./build/styles/main.css`.

### Compilação automática do Less para CSS

Para compilar automaticamente seus arquivos Less em CSS sempre que houver alterações, você pode usar `less-watch-compiler`.

1. **Instale globalmente:**
   Execute o seguinte comando para instalar o `less-watch-compiler` globalmente:

   ```
   npm install -g less-watch-compiler
   ```

2. **Instale localmente no projeto**
   Instalar o `less-watch-compiler` localmente no projeto:

   ```
   npm install --save-dev less-watch-compiler
   ```

3. **Adicione os scripts ao arquivo `package.json`:**
   Adicione os seguintes scripts ao seu arquivo `package.json`:

   ```json
   {
     "scripts": {
       "less": "less-watch-compiler ./src/styles ./build/styles main.less"
     }
   }
   ```

4. **Inicie a compilação automática:**
   Execute o seguinte comando para iniciar a compilação automática:
   ```
   npm run less
   ```
