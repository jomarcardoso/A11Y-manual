# Manual de acessibilidade na WEB

## Regras

A base das regras desse manual é o [WCAG](https://www.w3c.br/traducoes/wcag/wcag21-pt-BR/), porém vão muito adiante trazendo mais detalhes quanto a leitura correta, melhor experiência para o usuário, entre outros. As regras aqui têm o objetivo de complementar o WCAG e organizá-las por relevância, visto que nem sempre será possível atender todas as regras, então sempre buscar atender da mais importante para a menos importante ao se construir com componente.

## Técnicas de desenvolvimento

###  <a name="leitura-como-botão-de-alternância"></a> Leitura como botão de alternância

1. tag `button` ou `role="button"`
2. `aria-pressed="true|false"`

###  <a name="não-duplicar-leitura-de-rótulos-em-campos-de-formulário"></a> Não duplicar leitura de rótulos em campos de formulário

1. colocar `aria-hidden` na tag label atrelada ao `input`.

## Componentes

- [Lista](#lista)

## <a name="lista"></a>Lista

Regras da lista para leitores de tela:

- Para leitores com atalho de navegação de item de lista (tecla I no NVDA), usando o atalho deve ler o item inteiro e usando a navegação padrão deve separar por parábrafo, assim como qualquer conteúdo;
- Para leitores que não possuem atalho de navegação de item de lista, deve ler todo conteúdo.
- Leitor informar que entrou numa lista;
- Não duplicar leitura de rótulos em campos de formulário.

## <a name="switch"></a>Switch

Regras da lista para leitores de tela:

- [Ler como botão de alternância](#leitura-como-botão-de-alternância)
- Não duplicar a leitura de rótulos](#não-duplicar-leitura-de-rótulos-em-campos-de-formulário)

Exemplo usando bootstrap:

```html
<div class="form-check form-switch">
  <input class="form-check-input" type="checkbox" role="button" id="flexSwitchCheckChecked" aria-pressed="{CHECKED}">
  <label class="form-check-label" for="flexSwitchCheckChecked">Checked switch checkbox input</label>
</div>
```
