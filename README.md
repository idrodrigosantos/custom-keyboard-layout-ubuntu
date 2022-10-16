# Layout de Teclado Personalizado para Ubuntu

Layout de teclado em Português adaptado para teclados com padrão americano.

## Layout do Teclado

![keyboard-layout](https://user-images.githubusercontent.com/23555768/195992445-659fa934-7b47-408b-ab2c-ac92127ae9aa.png)

## Instalação

Baixar o repositório e descompactar.

Abrir o terminal e acessar o repositório descompactado.

Copiar o arquivo `pten` para o diretório `symbols` com o comando:

```bash
sudo cp pten /usr/share/X11/xkb/symbols
```

Após copiar o arquivo, acesse o diretório `rules` com o comando:

```bash
cd /usr/share/X11/xkb/rules
```

Abrir o arquivo `evdev.xml` com algum editor de texto (Nano, Gedit, Visual Studio Code, etc).

Antes da tag `</layoutList>` adicionar o código:

```xml
<layoutList>
  <!-- código omitido -->
  <layout>
    <configItem>
      <name>pten</name>
      <shortDescription>pten</shortDescription>
      <description>Português (para teclados americanos)</description>
      <languageList>
        <iso639Id>pte</iso639Id>
      </languageList>
    </configItem>
    <variantList></variantList>
  </layout>
</layoutList>
```

Salvar as alterações do arquivo e reiniciar o sistema.

## Adicionar Layout

[Como adicionar layout no Ubuntu](https://github.com/idrodrigosantos/custom-keyboard-layout-ubuntu/wiki/Instru%C3%A7%C3%B5es-de-Uso)

### Fonte

<https://www.kavalier.tv/blog/custom-keyboard-layout-for-coding-on-ubuntu-linux>
