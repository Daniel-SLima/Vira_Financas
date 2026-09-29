# Vira Finanças

<div align="center">

**Finanças pessoais de forma simples, local e offline no Android.**

[![Android APK](https://github.com/Daniel-SLima/Vira_Financas/actions/workflows/android-apk.yml/badge.svg?branch=main)](https://github.com/Daniel-SLima/Vira_Financas/actions/workflows/android-apk.yml)
![Kotlin](https://img.shields.io/badge/Kotlin-Android-7F52FF?logo=kotlin&logoColor=white)
![Status](https://img.shields.io/badge/status-Alpha%2007-orange)

</div>

## Sobre o projeto

O **Vira Finanças** é um aplicativo Android de controle financeiro pessoal desenvolvido com foco em uso rápido, privacidade e funcionamento offline.

O projeto começou como um protótipo simples e evoluiu para um aplicativo com identidade própria, persistência local, planejamento mensal, lançamentos recorrentes, parcelamentos, orçamento por categoria, exportação e backup.

> **Versão atual:** `1.0.0-alpha07`

## Principais recursos

- Registro rápido de **ganhos e gastos**
- Navegação entre competências mensais
- Saldo **realizado** e **previsto**
- Valores **recebidos, pagos, a receber e a pagar**
- Lançamentos fixos mensais com projeções futuras
- Gastos parcelados entre 2 e 60 vezes
- Categorias e filtros de movimentações
- Orçamento mensal por categoria
- Gráfico de gastos por categoria
- Busca por nome ou categoria
- Exportação mensal em CSV
- Backup completo e restauração em JSON
- Tema escuro seguindo o Android
- Proteção opcional com PIN, padrão ou senha do próprio aparelho
- Funcionamento totalmente offline

## Privacidade

O Vira foi pensado como um aplicativo **local-first**:

- não exige cadastro;
- não envia movimentações para servidor externo;
- mantém os dados financeiros no próprio aparelho;
- não armazena o PIN ou a senha do usuário;
- backups são criados apenas quando o usuário solicita.

## Stack

| Área | Tecnologia |
|---|---|
| Aplicativo | Kotlin |
| Plataforma | Android SDK |
| Persistência | SQLite |
| Build | Gradle |
| CI | GitHub Actions |
| Java | 17 |
| Android | minSdk 26 · targetSdk 36 |

## Interface

A versão 1.0 introduziu uma nova identidade para o produto e separou o aplicativo em quatro áreas principais:

**Início** — resumo financeiro, saldo, atalhos rápidos e próximos vencimentos.

**Movimentações** — histórico, busca, filtros e controle de lançamentos.

**Planejamento** — lançamentos fixos, parcelas e orçamento mensal.

**Ajustes** — preferências, segurança, exportação, backup e restauração.

## Regras financeiras

O aplicativo trabalha com o calendário do aparelho como competência. Ao mudar o mês, a nova competência passa a ser exibida automaticamente e os meses anteriores continuam acessíveis no histórico.

O saldo pode ser carregado entre competências. Como o cálculo usa os lançamentos registrados, alterações em meses anteriores também atualizam os saldos posteriores.

Lançamentos fixos aparecem como projeções nos meses futuros sem alterar o saldo realizado até serem efetivados.

## Backup e exportação

O backup em JSON inclui movimentações, lançamentos fixos, parcelamentos, preferências financeiras e orçamentos por categoria.

A restauração é transacional: um arquivo inválido ou incompatível não substitui os dados existentes.

O CSV foi preparado para uso em Excel e Google Sheets, incluindo tratamento de acentuação, separador compatível com formato brasileiro e proteção contra interpretação acidental de fórmulas.

## Build

O projeto possui workflow de CI para gerar o APK automaticamente.

```powershell
.\build.bat
```

Ou, em ambiente configurado com Gradle:

```bash
./gradlew assembleDebug
```

O pipeline também suporta APK release assinado. A chave privada não é armazenada no repositório e é fornecida ao GitHub Actions por Secrets.

## Estado atual

A **Alpha 07** consolida o redesign do Vira Finanças e mantém as funcionalidades financeiras desenvolvidas nas versões anteriores.

O projeto continua em evolução, com foco em experiência de uso, confiabilidade dos dados e expansão gradual das ferramentas de planejamento financeiro.

---

Desenvolvido por [Daniel Lima](https://github.com/Daniel-SLima).
