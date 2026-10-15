<p align="center">
  <img src="imagens/banner.png" alt="Sala de Tela" width="100%">
</p>

# Sala de Tela

Mostre sua tela para quem você quiser, por um link.

**Quem cria a sala hospeda a sala.** Você abre o app, cria uma sala, e o seu computador vira o servidor dela. Quem vai assistir não instala nada: abre o link no navegador e pronto.

A sala existe enquanto o app estiver aberto. Fechou, acabou. Não fica nada no ar, nem numa nuvem de ninguém.

[**Baixar a versão mais recente**](../../releases/latest)

---

## Sumário

- [Instalação](#instalação)
- [Passo a passo](#passo-a-passo)
- [Para quem vai assistir](#para-quem-vai-assistir)
- [Compartilhando com som](#compartilhando-com-som)
- [Perguntas frequentes](#perguntas-frequentes)
- [Limitações](#limitações)
- [Verificar o download](#verificar-o-download)

---

## Instalação

Na [página de versões](../../releases/latest) há dois arquivos para Windows:

| Arquivo | Para quem |
|---|---|
| `Sala de Tela Setup 0.1.0.exe` | Quem quer o app no menu Iniciar e um atalho na área de trabalho. Instala só para o seu usuário, sem pedir senha de administrador. |
| `SaladeTela-portatil-0.1.0.exe` | Quem não quer instalar nada, ou está numa máquina de trabalho sem direito de administrador. Baixou, executou, abriu. |

### O Windows vai reclamar na primeira vez

Vai aparecer uma tela azul dizendo **"O Windows protegeu o computador"**.

1. Clique em **Mais informações**.
2. Clique em **Executar assim mesmo**.

Isso acontece porque o instalador não é assinado digitalmente. A assinatura é um certificado que custa cerca de US$ 200 por ano. O aviso não é sobre vírus: é o Windows dizendo que não conhece quem publicou.

---

## Passo a passo

### 1. Crie a sala

Abra o app e clique em **Criar sala**. Ele leva alguns segundos abrindo um endereço público para o seu computador. Na primeira vez demora um pouco mais, porque baixa o `cloudflared` (uns 50 MB) e guarda para as próximas.

### 2. Copie o convite

Clique no convite, no alto da janela, para copiar o link. Mande no chat, no grupo, onde for. Quem abrir cai direto na sua sala.

### 3. Compartilhe a tela

Clique em **Compartilhar tela**. O seletor do Windows abre ali mesmo, na janela do app. Escolha uma tela inteira ou uma janela específica, e pronto.

### O endereço muda

Cada vez que você abre o app e cria uma sala, o endereço é outro. O link antigo para de funcionar. Se ele cair enquanto a sala está de pé, o convite no alto da janela fica amarelo avisando.

---

## Para quem vai assistir

**Pelo navegador, sem instalar nada.** Abra o link que te mandaram, em qualquer navegador, em qualquer computador. Até no celular, com sorte. É o caminho de quem só quer ver.

**Pelo app, se você já tiver.** Clique em **Entrar por link**, cole o convite, e a sala abre numa aba no alto da mesma janela. As suas salas continuam na primeira aba.

Vale a pena usar o app quando você também vai mostrar a sua tela: no app o seletor de tela abre na própria janela, enquanto pelo navegador você passa por uma aba de captura que precisa ficar aberta o tempo todo.

Entrar por link não hospeda nada. Quem hospeda continua sendo só quem criou a sala.

---

## Compartilhando com som

Na janela que abre ao compartilhar, **escolha uma aba** e marque a caixinha de áudio que aparece lá embaixo.

### Por que só aba?

Se você escolher a tela inteira, o computador entrega todo o som que está tocando, inclusive o do Discord. Aí todo mundo na call escuta a própria voz de volta, com atraso. Nenhum navegador consegue separar um programa específico dessa captura. Por isso, na tela inteira a transmissão vai **sem som**.

### Quero mostrar a tela inteira e ter som

Dá. Clique na engrenagem e escolha **Som de uma aba ou janela**. O vídeo continua sendo a tela inteira, e o som passa a vir da aba que você escolher.

Serve para YouTube, Twitch e jogos de navegador. Para um jogo instalado, cujo som não está em aba nenhuma, não tem como.

Quem assiste passa o mouse no alto-falante da barra de baixo para ajustar o volume, ou clica nele para silenciar.

---

## Perguntas frequentes

**O Windows diz que "protegeu o computador" ao abrir o instalador.**
É esperado. Clique em **Mais informações** e depois em **Executar assim mesmo**.

**O link que eu mandei não abre mais.**
O endereço muda a cada vez que o app abre uma sala, e some quando o app fecha. Crie a sala de novo e mande o convite novo.

**O convite ficou amarelo dizendo "Sem endereço".**
O túnel caiu. Ninguém de fora consegue entrar enquanto estiver assim. Volte para a lista de salas e crie a sala de novo.

**O botão de compartilhar abre uma aba e não acontece nada.**
Isso só acontece pelo navegador. Essa aba precisa continuar aberta enquanto você transmite. Pode voltar para o Discord normalmente, só não feche a aba.

**Não sai som.**
Abra o botão de informações na barra de baixo e olhe a linha **Som**. Ela diz em qual dos casos você está: sem áudio na transmissão, esperando o áudio, silenciado ou tocando.

**Funciona no celular?**
Para assistir, normalmente sim. Para compartilhar, não: nenhum navegador de celular permite capturar a tela.

**Qual navegador usar?**
Para assistir, qualquer um. Para mostrar a tela pelo navegador, sem o app, use Chrome, Edge, Brave ou Opera. Quem usa o app não precisa de navegador nenhum.

---

## Limitações

- Compartilhar do celular não é possível.
- Som de programa instalado em tela cheia não é possível, só som de aba.
- Muita gente ao mesmo tempo pesa na sua internet. Cada pessoa assistindo consome a qualidade escolhida, inteira. Em 2,5 Mb/s, cinco pessoas já são 12,5 Mb/s de subida.
- 60 fps depende do computador. Sem codificação por hardware no navegador, telas grandes entregam menos quadros.
- No máximo 4 telas ao mesmo tempo na mesma sala.

---

## Verificar o download

Para conferir que o arquivo não foi alterado, compare o hash SHA-256 no PowerShell:

```powershell
Get-FileHash "Sala de Tela Setup 0.1.0.exe" -Algorithm SHA256
```

O resultado deve ser:

```
0B7098B61AE998B4B76E02459C26184F2FFB3FB6557B9EA9FF0F63FFE5222517
```

---

## Código-fonte

O código do app e do servidor está em [VitorioCp/vigeance-screen](https://github.com/VitorioCp/vigeance-screen), com instruções para rodar pelo terminal, usar dentro do Discord e hospedar fora do seu computador.
