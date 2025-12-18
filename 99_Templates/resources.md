<%*
const nome = await tp.system.prompt("Nome");
const autor = await tp.system.prompt("Autor/Banda");
const tipo = await tp.system.prompt("Temas");

const dataAdicao = tp.file.creation_date("DD/MM/YYYY");

// status começa desmarcado (false)
const status = false;

const tags = [
  `${tipo}`
];

tR += `---
nome: ${nome}
autor/banda: ${autor}
tags:
${tags.map(t => `  - "${t}"`).join("\n")}
status: ${status}
data_adicao: ${dataAdicao}
---
`;
-%>

## Anotações