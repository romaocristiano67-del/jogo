# Arquitetura técnica

## Princípios

- Jogável antes de complexo: cada sistema novo deve funcionar com a cena atual.
- Orçamento para Intel Iris Xe, Full HD e 16 GB RAM: alvo de 30–60 FPS em qualidade média.
- Conteúdo modular: casas, vegetação, veículos e rotinas NPC não devem depender de coordenadas rígidas.
- Recursos originais ou devidamente licenciados; as imagens recebidas são apenas referências estéticas.

## Fundação adotada

| Componente | Repositório público | Papel no projeto |
| --- | --- | --- |
| Renderização | [three.js](https://github.com/mrdoob/three.js) | Cena 3D, materiais, luz, céu e áudio espacial. |
| Física | [cannon-es](https://github.com/pmndrs/cannon-es) | Colisões físicas, veículos e objetos interativos na próxima migração. |
| Colisão de geometria | [three-mesh-bvh](https://github.com/gkjohnson/three-mesh-bvh) | Colisão e raycast rápidos para interiores e terreno. |

## Estrutura-alvo

```
src/
  core/        renderer, ciclo de jogo, qualidade
  world/       loteamento, casas, portaria, piscina, vegetação
  player/      primeira pessoa e interação
  vehicles/    física, portas, cockpit, câmara e tráfego
  npc/         rotinas, navegação e animações
  systems/     clima, tempo, áudio, save e missões
assets/
  models/      GLB próprios ou com licença compatível
  audio/       sons CC0/autorais
  references/  referências recebidas; não publicar como assets do jogo
```

O protótipo atual está em `index.html` para preservar o funcionamento imediato. A próxima implementação deve mover sistemas completos, um de cada vez, para `src/`.
