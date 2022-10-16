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

1. Acesse as configurações do sistema no menu `Região e Idioma` em `Fontes de entrada` adicione um novo layout click no botão com o ícone `+`

![layout01](https://user-images.githubusercontent.com/23555768/196052913-de26a706-7d38-477b-b9f7-47d8948e4b29.png)

2. Click no botão com três pontos na vertical

![layout02](https://user-images.githubusercontent.com/23555768/196052919-02a8155a-bec0-414d-addc-8301281d1f28.png)

3. Na barra de pesquisa digite `Português (para teclados americanos)` para encontrar o layout

![layout03](https://user-images.githubusercontent.com/23555768/196052925-10771d58-ac7d-4a54-a396-3197b87644ea.png)

4. Acesse o menu `Outro`, selecione o layout e click no botão `Adicionar`

![layout04](https://user-images.githubusercontent.com/23555768/196052928-7bb451e4-e23e-4b7d-a6d9-45b387b68061.png)

5. O layout estará disponível para uso

![layout05](https://user-images.githubusercontent.com/23555768/196052935-c3ae16bd-c837-4b0f-b2d4-6152570cc649.png)

6. Para usar o layout selecione no menu do Ubuntu

![layout06](https://user-images.githubusercontent.com/23555768/196052941-a32d5a43-16af-4fcb-9936-5da717656c26.png)

### Fonte

<https://www.kavalier.tv/blog/custom-keyboard-layout-for-coding-on-ubuntu-linux>
