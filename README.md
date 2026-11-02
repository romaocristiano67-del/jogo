# Vila Girassol 3D

Jogo de simulação e exploração de um condomínio residencial tropical contemporâneo, inspirado na arquitetura moderna de Angola sem copiar as referências recebidas.

## Estado atual

O vertical slice jogável contém:

- Primeira pessoa, corrida, salto, portas e interiores visíveis.
- Casas, portaria com seguranças, ruas, árvores, campo, piscina e residentes.
- Céu dinâmico com sol, lua, estrelas, nuvens e ciclo dia/noite.
- Veículos de tráfego, entrada/saída e condução inicial.
- Chuva visual ativável com `R`, som procedural e guardado local.
- Perfis de qualidade para PC com Intel Iris Xe.
- Navegação de NPCs e pipeline de otimização GLB preparados no projeto.

## Executar

```bash
npm install
npm run dev
```

Enquanto a migração para módulos não estiver concluída, também pode abrir `index.html` através de um servidor local.

## Comandos no jogo

| Tecla | Ação |
| --- | --- |
| WASD | Mover / conduzir |
| Rato | Olhar |
| Shift | Correr |
| Espaço | Saltar |
| E ou clique | Interagir, abrir portas, entrar/sair do veículo |
| R | Chuva |
| T | Avançar o tempo |

## Licenças e referências

O motor e as bibliotecas planeadas estão documentados em [docs/ARQUITETURA.md](docs/ARQUITETURA.md). As fotos em `assets/references/` servem apenas de orientação interna e não são recursos do jogo.

Consulte [docs/ASSET_POLICY.md](docs/ASSET_POLICY.md) antes de importar qualquer asset ou exemplo de outro repositório.
