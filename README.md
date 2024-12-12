<h1>Tabelas</h1>
<b>1. Cliente:</b><br>
Colunas:
id Cliente (INT) - Chave Primária, Nome (VARCHAR(45)), Endereço (VARCHAR(45)), Telefone (VARCHAR(45)),Email (VARCHAR(45))<br><br>

<b>2. Veículo:</b><br>
Colunas:
idVeículo (INT) - Chave Primária
Placa (VARCHAR(45))
Modelo (VARCHAR(45))
Ano (INT)
Cliente_idCliente (INT) - Chave Estrangeira

<b>3. Equipe de Mecânicos:</b><br>
Colunas:
idEquipe de Mecânicos (INT) - Chave Primária
Nome Equipe (VARCHAR(45))
Veículo_idVeículo (INT) - Chave Estrangeira
Veículo_Cliente_idCliente (INT) - Chave Estrangeira

<b>4. Mecânico:</b><br>
Colunas:
idMecânico (INT) - Chave Primária
Código (VARCHAR(45))
Nome (VARCHAR(45))
Endereço (VARCHAR(45))
Especialidade (VARCHAR(45))
Equipe de Mecânicos_idVeículo (INT) - Chave Estrangeira
Mecânico_Equipe de Mecânicos_Veículo_Cliente_idCliente (INT) - Chave Estrangeira
Mecânico_Serviços_idServiços (INT) - Chave Estrangeira
Mecânico_Mão-de-Obra_idMão-de-Obra (INT) - Chave Estrangeira
Peças OS_has_Peça_Peça_idPeça (INT) - Chave Estrangeira

<b>5. OS:</b><br>
Colunas:
idOS (INT) - Chave Primária
Número (INT)
Data Emissão (VARCHAR(45))
Valor (FLOAT)
Status (VARCHAR(45))
Data de Conclusão (DATE)
Mecânico_idMecânico (INT) - Chave Estrangeira
Mecânico_Equipe de Mecânicos_Veículo_idVeículo (INT) - Chave Estrangeira
Mecânico_Equipe de Mecânicos_Veículo_Cliente_idCliente (INT) - Chave Estrangeira
Mecânico_Serviços_idServiços (INT) - Chave Estrangeira
Mecânico_Mão-de-Obra_idMão-de-Obra (INT) - Chave Estrangeira
Peças OS_has_Peça_Peça_idPeça (INT) - Chave Estrangeira

<b>6.  Autorização Cliente:</b><br>
Colunas:
idAutorização Cliente (INT) - Chave Primária
Autorização para execução da OS (VARCHAR(45))
OS_idOS (INT) - Chave Estrangeira

<b>7. Mão-de-Obra:</b><br>
Colunas:
idMão-de-Obra (INT) - Chave Primária
Valores Referência (FLOAT)

<b>8. Serviços:</b><br>
Colunas:
idServiços (INT) - Chave Primária
Tipo de Serviço (VARCHAR(45))

<b>9. Peças OS:</b><br>
Colunas:
idPeças OS (INT) - Chave Primária
Peças da OS (VARCHAR(45))

<b>10. Peça:</b><br>
Colunas:
idPeça (INT) - Chave Primária
Peça (VARCHAR(45))
Valor (FLOAT)

<b>11. Peças OS_has_Peça:</b><br>
Colunas:
Peças OS_idPeças OS (INT) - Chave Estrangeira
Peça_idPeça (INT) - Chave Estrangeira

![Oficina](https://github.com/user-attachments/assets/685aebf5-c403-4fb6-8d55-1fabeb45e8dc)
