# Simulador Humanware — GZero

Protótipo do simulador de cenários organizacionais. O usuário marca ações; a
ferramenta devolve, para cada um dos 4 âmbitos, o cenário provável em
**2027 · 2030 · 2035 · 2040 · 2045 · 2050**.

Sem IA e sem API: os cenários são textos pré-escritos e o roteamento é
determinístico.

## Publicação

Site estático de um arquivo só. `index.html` é autossuficiente — fontes, dados
e logo vão embutidos, sem nenhuma requisição externa.

Na Vercel: importe este repositório, deixe o framework como **Other** e não
configure build nem diretório de saída. O `index.html` na raiz já é o site.

## De onde vem este arquivo

`index.html` é **gerado** — não edite aqui. A fonte de verdade fica no projeto
`calculadora de coerência`:

```
dados/humanware.json            conteúdo (24 ações + 72 cenários)
visual/cenarios-humanware.html  app
build/gerar_assets.py           JSON  -> data.js / fonts.css / gzero.svg
build/gerar_bundle.py           app   -> index.html
```

Para atualizar esta pasta e republicar:

```
cd ".../calculadora de coerência"
python3 build/gerar_bundle.py ~/Documents/GitHub/humanware
cd ~/Documents/GitHub/humanware && git commit -am "atualiza simulador" && git push
```

## Tipografia

O arquivo embute ABC Whyte, ABC Whyte Inktrap e ABC Whyte Mono em versão
**Trial**. Antes de qualquer uso público em produção, trocar por licença
comercial.
