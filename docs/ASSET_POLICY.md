# Política de código e assets

## Regra obrigatória

Um repositório público não é automaticamente reutilizável. Antes de adicionar qualquer carro, pessoa, casa, som, textura ou trecho de código, registar:

1. URL de origem e autor;
2. licença específica do ficheiro ou pacote;
3. versão/commit;
4. uso no jogo;
5. atribuição exigida.

Não importar conteúdo sem licença explícita. Não extrair recursos de jogos comerciais, demos fechadas ou repositórios sem licença.

## Fontes aprovadas para a seleção inicial

| Fonte | Uso permitido no projeto | Regra |
| --- | --- | --- |
| [Poly Haven](https://polyhaven.com/) | Texturas PBR, HDRIs, modelos pontuais e materiais de interiores/exteriores. | CC0; descarregar apenas as resoluções adequadas ao Intel Iris Xe. |
| [Khronos glTF Sample Assets](https://github.com/KhronosGroup/glTF-Sample-Assets) | Teste de importação, materiais PBR e animação. | Verificar a licença individual de cada modelo; não tratar todo o catálogo como CC0. |
| [Kenney](https://kenney.nl/assets) | Protótipos, ícones e placeholders. | CC0, mas o estilo low-poly não será usado como arte final realista. |
| Repositórios MIT/BSD/Apache-2.0 | Código de sistemas, exemplos e ferramentas. | Manter aviso/licença quando exigido. |

## Exemplos que podemos estudar

- [Cannon Car Simulator](https://github.com/NullCipherr/Cannon-Car-Simulator): organização de física veicular e câmaras; não copiar modelos sem verificar a licença.
- [three.js examples](https://github.com/mrdoob/three.js/tree/dev/examples): carregamento GLTF, chuva, pós-processamento e LOD.
- [recast-navigation-js vanilla example](https://github.com/isaac-mason/recast-navigation-js/tree/main/examples/three-vanilla-example): integração de navegação para NPCs.

## Processo de importação

1. Guardar asset original em `assets/source/` com `LICENSE` e ficheiro de proveniência.
2. Otimizar para GLB com glTF Transform.
3. Criar versão de execução em `assets/models/` ou `assets/textures/`.
4. Testar em qualidade média a 1080p antes de aceitar no jogo.
