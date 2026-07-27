# Calculadora de Coerência — GZero

Protótipo v3. A organização escolhe as ações que condizem com o jeito real de
operar; a ferramenta simula o "corpo" da organização reagindo a essas escolhas,
marco a marco, e devolve os futuros prováveis ao longo de **24 anos**.

## Publicação

Site estático de um arquivo só. `index.html` é autossuficiente — todo o CSS e o
JavaScript vão embutidos.

Na Vercel: importe este repositório, deixe o framework como **Other** e não
configure build nem diretório de saída. O `index.html` na raiz já é o site.

## Conexão com IA

O v3 chama uma API compatível com OpenAI (base URL, chave e modelo informados
na própria tela). A chave fica só no navegador do usuário e não é versionada.

Aberto por `file://` (duplo clique), o navegador **bloqueia** essas chamadas de
rede — por isso a tela mostra um aviso e um passo a passo para rodar em
`http://localhost`. Servido pela Vercel (HTTPS), as chamadas funcionam
normalmente.

## Como atualizar

`index.html` é o entregável. Para publicar uma nova versão, substitua o arquivo,
faça commit e push:

```
cp nova-versao.html index.html
git commit -am "atualiza calculadora" && git push
```
