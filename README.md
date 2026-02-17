# Férias Jeri — Operação & Financeiro

## Objetivo
Substituir o controle operacional e financeiro feito em planilhas por um sistema interno, com histórico de alterações, controle por turnos e fechamento diário.

## Realidade da operação (turnos)
- **Madrugada (00h–07h):** criação/ajustes de reservas, confirmação operacional, suporte a clientes.
- **Dia (07h–18h):** operação principal (embarques, no-show, cancelamentos, atualizações).
- **Financeiro (18h–00h):** conferência de pagamentos, repasses de vendedores/parceiros, ajustes e fechamento do dia.

## Tipos de serviço
- **Bate-volta:** ida e volta no mesmo dia (criação automática das duas pernas).
- **Transfer:** pode ser **só ida**, **só volta** ou **ida e volta** (datas podem ser diferentes).

## Perfis e permissões
### Operacional (Dia / Madrugada)
Pode:
- Criar viagens e reservas (booking)
- Criar/editar pernas (ida/volta), embarque/desembarque e status operacional
- Registrar pagamento como **INFORMADO** (ex: “cliente pagou ao vendedor”)
Não pode:
- Confirmar pagamentos
- Dar baixa em repasses
- Fechar o dia financeiro

### Financeiro
Pode:
- Confirmar pagamentos (**INFORMADO → CONFIRMADO**)
- Controlar repasses de vendedores/parceiros
- Fechar o dia e bloquear alterações financeiras do dia
Não deve:
- Alterar dados operacionais (embarque/horários/roteiros)

## Fluxo do dia (00h → 00h)
1. Operacional cria/ajusta reservas e status operacionais.
2. Pagamentos podem ser registrados como **INFORMADO** durante o dia.
3. Financeiro confere valores e confirma pagamentos.
4. Financeiro fecha o dia (gera resumo e bloqueia alterações financeiras do dia).

## Status operacionais (por perna)
PENDENTE · CONFIRMADO · CANCELADO · NO_SHOW · EMBARCOU · CONCLUIDO

## Status financeiros (por reserva)
A_RECEBER · PARCIAL · PAGO · CORTESIA · ESTORNADO
