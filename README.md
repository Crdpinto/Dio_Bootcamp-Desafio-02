# Projeto Conceitual de Banco de Dados para Oficina Mecânica

## Descrição
Este projeto visa desenvolver um esquema conceitual de banco de dados para um sistema de controle e gerenciamento de ordens de serviço (OS) em uma oficina mecânica. O sistema permitirá que clientes levem seus veículos para consertos e revisões periódicas, gerenciando eficientemente as ordens de serviço, peças utilizadas, serviços realizados e equipes de mecânicos.

## Estrutura do Esquema
### Tabelas
**1. Cliente:**
- id Cliente (INT) - Chave Primária<br>
- Nome (VARCHAR(45))
- Endereço (VARCHAR(45))
- Telefone (VARCHAR(45))
- Email (VARCHAR(45))

**2. Veículo:**
- idVeículo (INT) - Chave Primária
- Placa (VARCHAR(45))
- Modelo (VARCHAR(45))
- Ano (INT)
- Cliente_idCliente (INT) - Chave Estrangeira

**3. Equipe de Mecânicos:**
- idEquipe de Mecânicos (INT) - Chave Primária
- Nome Equipe (VARCHAR(45))
- Veículo_idVeículo (INT) - Chave Estrangeira
- Veículo_Cliente_idCliente (INT) - Chave Estrangeira

**4. Mecânico:**
- idMecânico (INT) - Chave Primária
- Código (VARCHAR(45))
- Nome (VARCHAR(45))
- Endereço (VARCHAR(45))
- Especialidade (VARCHAR(45))
- Equipe de Mecânicos_idVeículo (INT) - Chave Estrangeira
- Mecânico_Equipe de Mecânicos_Veículo_Cliente_idCliente (INT) - Chave Estrangeira
- Mecânico_Serviços_idServiços (INT) - Chave Estrangeira
- Mecânico_Mão-de-Obra_idMão-de-Obra (INT) - Chave Estrangeira
- Peças OS_has_Peça_Peça_idPeça (INT) - Chave Estrangeira

**5. OS:**
- idOS (INT) - Chave Primária
- Número (INT)
- Data Emissão (VARCHAR(45))
- Valor (FLOAT)
- Status (VARCHAR(45))
- Data de Conclusão (DATE)
- Mecânico_idMecânico (INT) - Chave Estrangeira
- Mecânico_Equipe de Mecânicos_Veículo_idVeículo (INT) - Chave Estrangeira
- Mecânico_Equipe de Mecânicos_Veículo_Cliente_idCliente (INT) - Chave Estrangeira
- Mecânico_Serviços_idServiços (INT) - Chave Estrangeira
- Mecânico_Mão-de-Obra_idMão-de-Obra (INT) - Chave Estrangeira
- Peças OS_has_Peça_Peça_idPeça (INT) - Chave Estrangeira

**6.  Autorização Cliente:**
- idAutorização Cliente (INT) - Chave Primária
- Autorização para execução da OS (VARCHAR(45))
- OS_idOS (INT) - Chave Estrangeira

**7. Mão-de-Obra:**
- idMão-de-Obra (INT) - Chave Primária
- Valores Referência (FLOAT)

**8. Serviços:**
- idServiços (INT) - Chave Primária
- Tipo de Serviço (VARCHAR(45))

**9. Peças OS:**
- idPeças OS (INT) - Chave Primária
- Peças da OS (VARCHAR(45))

**10. Peça:**
- idPeça (INT) - Chave Primária
- Peça (VARCHAR(45))
- Valor (FLOAT)

**11. Peças OS_has_Peça:**
- Peças OS_idPeças OS (INT) - Chave Estrangeira
- Peça_idPeça (INT) - Chave Estrangeira

![Oficina](https://github.com/user-attachments/assets/685aebf5-c403-4fb6-8d55-1fabeb45e8dc)

### **Considerações Finais**
Este esquema conceitual foi desenvolvido com base na narrativa fornecida e abrange os principais aspectos operacionais de uma oficina mecânica, para garantir a integridade e a eficiência do gerenciamento de ordens de serviço.

> [!NOTE]
> Estou a disposição para sugestões e críticas que ajudem na melhoria deste modelo e na minha evolução pessoal.
