---
name: project-menores
description: Flag automática para ritmistas menores de 18 anos + controle de declaração do responsável
metadata:
  type: project
---

Quando o ritmista cadastrado tiver menos de 18 anos (calculado pela data de nascimento), o sistema deve:

1. **Flag automática** — marcar o ritmista como menor de idade no banco de dados
2. **Visibilidade no painel do diretor** — exibir destaque visual (badge/ícone) na lista de ritmistas menores
3. **Filtro** — diretor pode filtrar a lista para ver apenas menores
4. **Controle de declaração** — campo para registrar se a declaração do responsável foi entregue (sim/não) + data de entrega

**Why:** Menores de idade precisam de declaração do responsável para desfilar na Sapucaí. O diretor precisa controlar quem entregou e quem não entregou antes do carnaval.

**How to apply:** Implementar no painel do diretor (admin.html). A flag é calculada automaticamente pela data de nascimento no momento do cadastro. Adicionar coluna `declaracao_responsavel` (boolean) e `data_declaracao` (date) no banco Supabase.
