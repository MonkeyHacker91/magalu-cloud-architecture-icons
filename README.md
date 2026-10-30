# Magalu Cloud Architecture Icons

Pack de ícones para diagramas de arquitetura da **Magalu Cloud (MGC)** — no mesmo espírito do [AWS Architecture Icons](https://aws.amazon.com/architecture/icons/).

Use estes SVGs em documentação, slides, whiteboards e no Magalu Infra Designer.

![preview](docs/preview.svg)

## O que tem no pack

| Pasta | Conteúdo |
| --- | --- |
| `Architecture-Service-Icons_1.0/` | Ícones de serviço por categoria (`_48.svg` e `_64.svg`) |
| `Architecture-Category-Icons_1.0/` | Ícones de categoria (Compute, Networking, Storage…) |
| `svg/` | Cópia plana de todos os recursos (fácil de importar) |
| `aliases.json` | Mapa de nomes curtos (`MgcVm` → nome oficial) |
| `manifest.json` | Metadados (cor, categoria, caminhos) |

## Categorias e cores

| Categoria | Cor | Exemplos |
| --- | --- | --- |
| Compute | `#0086FF` | Virtual Machine |
| Containers | `#2A67FB` / `#8B5CFF` | Kubernetes, Container Registry |
| Networking | `#8C4FFF` | VPC, Subnet, Load Balancer, Public IP, NAT |
| Storage | `#FF6A00` / `#1A8754` | Block Storage, Object Storage |
| Database | `#3B48CC` | DBaaS, DBaaS Replica |
| Security & Identity | `#DD344C` | Security Group, SSH Key |
| Artificial Intelligence | `#D91CAC` | AI Hub, Agentic Commerce |

## Convenção de nomes

Seguimos o padrão AWS Resource Icons:

```text
Res_Magalu-Cloud-<Service-Name>_64.svg
Arch-Category_<Category>.svg
```

Exemplos:

- `Res_Magalu-Cloud-Virtual-Machine_64.svg`
- `Res_Magalu-Cloud-Load-Balancer_48.svg`
- `Arch-Category_Networking.svg`

## Uso rápido

### HTML / web

```html
<img src="svg/Res_Magalu-Cloud-Virtual-Machine.svg" width="48" height="48" alt="VM" />
```

### Draw.io / diagrams.net

1. Arraste os SVGs de `Architecture-Service-Icons_1.0/` para o canvas  
2. Ou File → Open Library… (importe a pasta como biblioteca)

### Figma

Importe a pasta `svg/` como componentes. Mantenha o quadrado arredondado intacto para consistência visual.

### React

```jsx
<img src="@mgc/architecture-icons/svg/Res_Magalu-Cloud-VPC.svg" alt="VPC" width={48} />
```

## Linguagem visual

- Tile quadrado com cantos arredondados (`rx=12` em 64px)
- Fundo sólido por categoria (sem gradiente neon)
- Glifo branco central, legível em 48px e 64px
- Sem texto “MGC” dentro do ícone (a cor + glifo identificam o serviço)
- Ideal para fundo claro *ou* escuro de diagrama

## Preview local

Abra `preview.html` no navegador para ver o catálogo completo.

```bash
python3 -m http.server 8765
# http://127.0.0.1:8765/preview.html
```

## Versionamento

SemVer no `manifest.json` / `package.json`.

- **MAJOR** — mudança breaking de nome/caminho
- **MINOR** — novos ícones / categorias
- **PATCH** — ajuste visual sem trocar IDs

## Licença

MIT — veja [LICENSE](./LICENSE).

Você pode usar, modificar e redistribuir nos seus diagramas e produtos.  
**Magalu Cloud** e marcas relacionadas pertencem aos seus respectivos donos; este pack é um asset de arquitetura comunitário / de produto, não um kit de marca institucional completo.

## Contribuindo

1. Mantenha viewBox `0 0 64 64`
2. Use só a cor de categoria + `#FFFFFF`
3. Atualize `manifest.json` e `aliases.json`
4. Abra um PR com screenshot do ícone novo no `preview.html`

---

**Magalu Cloud Architecture Icons** · v1.0.0
