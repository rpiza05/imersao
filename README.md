# imersao

projeto para o curso da alura/google Imersao em IA


É o tradicional jogo da forca mas com a palavra sugerida pela IA do gemini

Você tem 10 chances até acertar a palavra

Digite fim para finalizar a qualquer momento

Obs: tive problemas com a largura do input que ocupava toda a tela, percebi que começou a ocorrer após a inclusão da linha:
result = model.generate_content(prompt)
Depois de muita busca utilizei o trecho de código abaixo, no começo da célula, e resolveu:

codigo para corrigir largura do input que estava estourando:

<code>from IPython.display import HTML
def set_css():
  display(HTML('''
  <style>
    input { width: 100px!important; }
  </style>
  '''))
get_ipython().events.register('pre_run_cell', set_css)
</code>

(Hello Google Colab lets check this 'error' above)

Proximos passos (se houvesse tempo):
- permitir escolher categorias de palavras no começo do jogo e alterar o prompt adequadamente para então pegar a palavra
- permitir solicitar 1 dica e pedir a AI um sinonimo da palavra e exibir (neste caso utilizaria model.start_chat ao invés de model.generate_content)
- perguntar no final se quer jogar de novo e reiniciar o jogo

Obrigado, espero que gostem e ajude alguém.
Renato

