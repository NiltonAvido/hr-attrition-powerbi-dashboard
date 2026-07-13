# Dicionário de Dados — HR Analytics

Dataset com **1480 colaboradores** e **37 variáveis**. Fonte: dataset público de RH (variante enriquecida do IBM HR Attrition), Kaggle — dados para fins educativos.

| # | Coluna | Tipo | Descrição |
|---|--------|------|-----------|
| 1 | `EmpID` | texto | Identificador do colaborador |
| 2 | `Age` | inteiro | Idade |
| 3 | `AgeGroup` | texto | Faixa etária |
| 4 | `Attrition` | texto | Saída da empresa (Yes/No) |
| 5 | `BusinessTravel` | texto | Frequência de viagens |
| 6 | `DailyRate` | inteiro | Tarifa diária |
| 7 | `Department` | texto | Departamento |
| 8 | `DistanceFromHome(KM)` | inteiro | Distância a casa (km) |
| 9 | `Education` | inteiro | Nível de escolaridade (1-5) |
| 10 | `EducationField` | texto | Área de formação |
| 11 | `EmployeeCount` | inteiro | Contagem (constante=1) |
| 12 | `EmployeeNumber` | inteiro | Número interno |
| 13 | `EnvironmentSatisfaction` | inteiro | Satisfação com o ambiente (1-4) |
| 14 | `Gender` | texto | Género |
| 15 | `JobInvolvement` | inteiro | Envolvimento no trabalho (1-4) |
| 16 | `JobLevel` | inteiro | Nível hierárquico (1-5) |
| 17 | `JobRole` | texto | Função |
| 18 | `JobSatisfaction` | inteiro | Satisfação no trabalho (1-4) |
| 19 | `MaritalStatus` | texto | Estado civil |
| 20 | `MonthlyIncome` | inteiro | Rendimento mensal |
| 21 | `SalarySlab` | texto | Escalão salarial |
| 22 | `HourlyRate` | decimal | Tarifa horária |
| 23 | `NumCompaniesWorked` | inteiro | N.º de empresas anteriores |
| 24 | `Over18` | texto | Maior de 18 (constante) |
| 25 | `OverTime` | texto | Faz horas extraordinárias (Yes/No) |
| 26 | `SalaryHike %` | inteiro | Aumento salarial (%) |
| 27 | `PerformanceRating` | inteiro | Avaliação de desempenho (3-4) |
| 28 | `RelationshipSatisfaction` | inteiro | Satisfação nas relações (1-4) |
| 29 | `StandardWorkingHours` | inteiro | Horas padrão (constante) |
| 30 | `StockOptionLevel` | inteiro | Nível de stock options (0-3) |
| 31 | `TotalExperience(Years)` | inteiro | Experiência total (anos) |
| 32 | `TrainingsLastYear` | inteiro | Formações no último ano |
| 33 | `WorkLifeBalance` | inteiro | Equilíbrio vida-trabalho (1-4) |
| 34 | `YearsatCompany` | inteiro | Anos na empresa |
| 35 | `YearsinCurrentRole` | inteiro | Anos na função atual |
| 36 | `YearsSincePromotion` | inteiro | Anos desde a última promoção |
| 37 | `YearsWithCurrManager` | decimal | Anos com o gestor atual |

## Notas de qualidade

- **Colunas constantes** (sem valor analítico): `EmployeeCount`, `Over18`, `StandardWorkingHours`.
- **Valores em falta:** 61 células nulas no dataset em bruto.
- **Inconsistência de categorias:** a coluna `BusinessTravel` contém variações do mesmo valor (`Travel_Rarely`, `TravelRarely`, `Travel-Frequently`) que exigem normalização.
- **`EmpID` repetidos:** 16 identificadores duplicados a tratar na limpeza.
- **`PerformanceRating`** só contém valores 3 e 4 (não há avaliações baixas).