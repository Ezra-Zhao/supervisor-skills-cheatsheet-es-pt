# 🎓 Guía rápida: Supervisor-Skills — un co-supervisor de IA para tu doctorado (ES · PT)

Una sola página para trabajar con los *skills* de investigación de **Supervisor-Skills** (proyecto de HKUSTDial): del tema a la respuesta a los revisores, en el orden real del ciclo de vida de un paper.

**Autor:** Ezra-Zhao · Octubre 2026

Proyecto original: https://github.com/HKUSTDial/Supervisor-Skills (más de 9.000 estrellas en octubre de 2026)

> **Nota de autoría:** esta guía es una síntesis original, escrita por el autor a partir de su propio uso de la herramienta. No reproduce el *handbook* ni ningún texto del proyecto original (cuya licencia es CC BY-NC-SA); si quieres el material completo, ve al repositorio enlazado.

---


Apoyo y más: [GitHub Sponsors](https://github.com/sponsors/Ezra-Zhao) · [Gumroad — plantillas y cuadernos que uso](https://ezraflow28.gumroad.com) · [Ko-fi](https://ko-fi.com/ezra777zhao)

## 🇪🇸 Español

### Instalación (una sola vez)

```bash
git clone https://github.com/HKUSTDial/Supervisor-Skills.git
# Copia SOLO la carpeta del skill que vayas a usar a tu proyecto:
cp -r Supervisor-Skills/skills/idea-evaluator tu-proyecto/.claude/skills/
```

Cada skill es una carpeta con un `SKILL.md`. Tu agente (Claude Code u otro compatible con Agent Skills) lo descubre solo al abrir el proyecto, y lo invocas pidiendo la tarea en lenguaje natural o nombrando el skill.

### La tabla: un skill por etapa

| Etapa | Skill | Uso en una línea | ⚠️ Error típico |
|---|---|---|---|
| Instalación | *(la carpeta `skills/`)* | Copia la carpeta del skill a `.claude/skills/` de tu proyecto (o a `~/.claude/skills/` para usarlo en todo) | Copiar el repo entero dentro del proyecto: ensucia tu repo y mezcla versiones |
| 1. Tema | `idea-evaluator` | Describe tu idea en 5–10 líneas y pide la evaluación: novedad, factibilidad y encaje con tu perfil | Pedir la evaluación sin contexto de tu campo: la respuesta será genérica. Añade 2–3 papers de referencia |
| 2. Literatura | `deep-research` | Pide un barrido del estado del arte sobre tu pregunta, organizado por líneas de trabajo y huecos | Aceptar las citas sin abrirlas: cualquier modelo puede inventar referencias. Verifica cada cita en la fuente |
| 3. Introducción | `intro-drafter` | Dale tu contribución en 3 frases y el hueco que llena; pide el borrador de la introducción en ese orden | Empezar por la introducción sin tener claros los resultados: la intro promete lo que el paper debe cumplir |
| 4. Redacción | `paper-writer` | Trabaja sección por sección, con el esquema aprobado por ti antes de redactar cada parte | Pedir «el paper completo» de una vez: obtienes texto fluido pero sin tu voz ni tus decisiones |
| 5. Plantillas | `tech-paper-template` / `benchmark-paper-template` | Parte de la plantilla según el tipo de paper (método técnico o benchmark) y rellena con tu material | La plantilla no sustituye las normas de la revista o conferencia destino: contrasta siempre con su guía oficial |
| 6. Figuras | `figure-designer` (+ `drawio-reconstruction`) | Diseña la figura principal pensando en qué debe entender el lector en 10 segundos; reconstruye diagramas en Draw.io para editarlos | Figuras en mapa de bits borroso: exporta siempre en vectorial (PDF/SVG) para la versión final |
| 7. Pulido | `paper-polish` | Pide pulir claridad y ritmo **sin tocar** términos técnicos, notación ni números | No dar esa instrucción de «no tocar»: el pulido puede «corregir» un término que era intencional |
| 8. Pre-revisión | `pre-submission-reviewer` | Antes de enviar, pide una revisión dura simulando un revisor hostil de tu venue | Usarlo como palmadita en la espalda: su valor está en que encuentre los problemas antes que el revisor real |
| 9. Rebuttal | `rebuttal-guidance` | Pega los comentarios y responde punto por punto, separando lo que aceptas, lo que aclaras y lo que defiendes | Prometer experimentos que no vas a hacer: el revisor lo nota y pierdes credibilidad en todo lo demás |
| Todo el flujo | `vibe-research-workflow` | Encadena los skills anteriores como un flujo continuo, con una parada tuya al final de cada etapa | Dejarlo correr sin paradas: un error en la etapa 2 se convierte en un paper entero mal orientado |

### Regla de oro

El co-supervisor de IA acelera el trabajo mecánico (buscar, estructurar, pulir), pero **la pregunta de investigación, los datos y las conclusiones siguen siendo tuyas**: son lo que el comité y los revisores van a juzgar.

---

## 🇵🇹 Português

### Instalação (uma única vez)

```bash
git clone https://github.com/HKUSTDial/Supervisor-Skills.git
# Copie SOMENTE a pasta do skill que você vai usar para o seu projeto:
cp -r Supervisor-Skills/skills/idea-evaluator seu-projeto/.claude/skills/
```

Cada skill é uma pasta com um `SKILL.md`. Seu agente (Claude Code ou outro compatível com Agent Skills) o descobre sozinho ao abrir o projeto, e você o chama pedindo a tarefa em linguagem natural ou citando o nome do skill.

### A tabela: um skill por etapa

| Etapa | Skill | Uso em uma linha | ⚠️ Erro típico |
|---|---|---|---|
| Instalação | *(a pasta `skills/`)* | Copie a pasta do skill para `.claude/skills/` do seu projeto (ou para `~/.claude/skills/` para usar em tudo) | Copiar o repositório inteiro para dentro do projeto: suja seu repo e mistura versões |
| 1. Tema | `idea-evaluator` | Descreva sua ideia em 5–10 linhas e peça a avaliação: novidade, viabilidade e encaixe com o seu perfil | Pedir a avaliação sem contexto da sua área: a resposta sai genérica. Acrescente 2–3 papers de referência |
| 2. Literatura | `deep-research` | Peça um varredura do estado da arte sobre a sua pergunta, organizada por linhas de trabalho e lacunas | Aceitar as citações sem abri-las: qualquer modelo pode inventar referências. Confira cada citação na fonte |
| 3. Introdução | `intro-drafter` | Passe sua contribuição em 3 frases e a lacuna que ela preenche; peça o rascunho da introdução nessa ordem | Começar pela introdução sem ter os resultados claros: a intro promete o que o paper precisa cumprir |
| 4. Redação | `paper-writer` | Trabalhe seção por seção, com o esqueleto aprovado por você antes de redigir cada parte | Pedir «o paper completo» de uma vez: sai um texto fluido, mas sem a sua voz nem as suas decisões |
| 5. Modelos | `tech-paper-template` / `benchmark-paper-template` | Comece pelo modelo conforme o tipo de paper (método técnico ou benchmark) e preencha com o seu material | O modelo não substitui as normas da revista ou conferência de destino: confira sempre o guia oficial |
| 6. Figuras | `figure-designer` (+ `drawio-reconstruction`) | Desenhe a figura principal pensando no que o leitor deve entender em 10 segundos; reconstrua diagramas no Draw.io para editá-los | Figuras em bitmap borrado: exporte sempre em vetor (PDF/SVG) para a versão final |
| 7. Polimento | `paper-polish` | Peça polimento de clareza e ritmo **sem mexer** em termos técnicos, notação nem números | Não dar essa instrução de «não mexer»: o polimento pode «corrigir» um termo que era intencional |
| 8. Pré-revisão | `pre-submission-reviewer` | Antes de enviar, peça uma revisão dura simulando um revisor hostil do seu venue | Usar como tapinha nas costas: o valor está em achar os problemas antes do revisor de verdade |
| 9. Rebuttal | `rebuttal-guidance` | Cole os comentários e responda ponto a ponto, separando o que você aceita, o que esclarece e o que defende | Prometer experimentos que você não vai fazer: o revisor percebe e você perde credibilidade em todo o resto |
| Fluxo todo | `vibe-research-workflow` | Encadeie os skills acima como um fluxo contínuo, com uma parada sua no fim de cada etapa | Deixar rodar sem paradas: um erro na etapa 2 vira um paper inteiro mal orientado |

### Regra de ouro

O coorientador de IA acelera o trabalho mecânico (buscar, estruturar, polir), mas **a pergunta de pesquisa, os dados e as conclusões continuam sendo seus**: é isso que a banca e os revisores vão julgar.

---

## 🇬🇧 English summary

One-page cheat sheet (Spanish + Portuguese) for **Supervisor-Skills** (HKUSTDial): research-lifecycle agent skills — `idea-evaluator`, `deep-research`, `intro-drafter`, `paper-writer`, the paper templates, `figure-designer`, `paper-polish`, `pre-submission-reviewer`, `rebuttal-guidance` and the end-to-end `vibe-research-workflow`. Each row: what the skill does in one line, plus the typical mistake to avoid. Original synthesis by the author; no text from the original project's handbook (CC BY-NC-SA) is reproduced.

**Author:** Ezra-Zhao · October 2026 · MIT License
