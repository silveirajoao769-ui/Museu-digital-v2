# Plano de migração do acervo fotográfico — Museu Digital de Meleiro V2

## Estado verificado
- O museu V2 é um site 2D em `index.html`.
- As galerias de Cultura e Tradições, Famílias Pioneiras e Arquivo Fotográfico estão preparadas, mas ainda **não contêm fotografias históricas verificadas**.
- O repositório 3D `silveirajoao769-ui/museu-digital-` permanece separado e não deve ser alterado durante a migração.
- Não usar imagens de bancos genéricos como se fossem documentos históricos.

## Itens a localizar e validar
| Coleção | Identificação provisória | Arquivo | Legenda original | Fonte/autorização | Estado |
| --- | --- | --- | --- | --- | --- |
| Cultura e Tradições | Desfile Cultural da Agrimeleiro | A localizar | A confirmar | A confirmar | Pendente |
| Cultura e Tradições | Festa do Colono | A localizar | A confirmar | A confirmar | Pendente |
| Cultura e Tradições | Agrimeleiro | A localizar | A confirmar | A confirmar | Pendente |

## Procedimento de importação
1. Localizar os arquivos originais, incluindo eventual origem fora do repositório GitHub (por exemplo, imagens enviadas durante a montagem do museu 3D).
2. Confirmar a correspondência de cada imagem, sua legenda e autorização de uso.
3. Salvar arquivos otimizados em `assets/acervo/cultura/` (preferencialmente WebP/AVIF com cópia preservada do original em arquivo seguro).
4. Cadastrar em `collections.cultura.photos` no `index.html` como objetos `{src, alt, caption}`, por exemplo:
   `{src:'/assets/acervo/cultura/nome-validado.webp',alt:'Descrição objetiva da cena',caption:'Legenda original confirmada'}`.
5. Verificar em desktop e celular: abertura, swipe, setas, contador, Escape, foco e falha de carregamento.
6. Conferir o deploy READY na Vercel e inspecionar a página real antes de anunciar o acervo publicado.

## Critério de conclusão
Uma coleção só é considerada publicada quando pelo menos um arquivo autêntico estiver acessível, com legenda e procedência conferidas. Não anunciar imagens inexistentes como conteúdo concluído.
