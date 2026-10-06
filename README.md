# monitor-ambiental-iot

MVP de IoT que integra Arduino, servidor Node.js e painel web. O Arduino envia leituras pela serial, o servidor valida o protocolo e disponibiliza os dados para o painel.

## Protocolo

```text
LEITURA,temperatura, 23
```

## Executar

```bash
npm test
npm start
# em outra janela
curl -X POST localhost:3000/readings -d 'LEITURA,temperatura, 23'
```

Abra `web/index.html` por um servidor estático apontando para a API. O sketch em `arduino/` funciona com um sensor analógico simples e pode ser adaptado ao sensor real.

## Limitações

O MVP não persiste dados, autentica clientes nem substitui calibração de sensores. Essas são etapas seguintes do projeto.

MIT — Mateus Florido Pena
