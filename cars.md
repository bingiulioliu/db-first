# Cars Store

## Schema tabella `cars`
| Nome Colonna | Tipo | Attributi | Indici |
|---|---|---|---|
| id | UNSIGNED INT | NOT NULL | PRIMARY KEY |
| name | VARCHAR(100) | NOT NULL | - |
| model | VARCHAR(50) | NOT NULL | INDEX |
| brand | VARCHAR(50) | NOT NULL | INDEX |
| segment | CHAR(1) | NULL | INDEX |
| vin | CHAR(17) | NOT NULL UNIQUE | - |
| condition | VARCHAR(15) | NOT NULL | INDEX |
| kilometers | MEDIUMINT | NOT NULL | - |
| year | SMALLINT | NOT NULL | INDEX |
| color | VARCHAR(10) | NULL | - |
| stolen | TINYINT | NULL | - |
| fermo_amministrativo | TINYINT | NULL | - |
| description | TEXT | NULL DEFAULT | - |
| img | TEXT | NULL ||
| price | CHAR(7) | NOT NULL ||

### Schema tabella `models` (relazione 1:N con cars)
| Nome Colonna | Tipo | Attributi | Indici |
|---|---|---|---|
| id | UNSIGNED INT | NOT NULL | PRIMARY KEY |
| name | VARCHAR(50) | NOT NULL | INDEX |
| description | TEXT | NULL | |

### Schema tabella `brands` (relazione 1:N con cars e N:1 con models?)
| Nome Colonna | Tipo | Attributi | Indici |
|---|---|---|---|
| id | UNSIGNED INT | NOT NULL | PRIMARY KEY |
| name | VARCHAR(50) | NOT NULL | INDEX |
| description | TEXT | NULL | |

### Schema tabella `segments` (relazione 1:N con cars e 1:N con models?)
| Nome Colonna | Tipo | Attributi | Indici |
|---|---|---|---|
| id | UNSIGNED INT | NOT NULL | PRIMARY KEY |
| name | CHAR(1) | NOT NULL | INDEX |
| description | TEXT | NULL | |

### Schema tabella `conditions` (relazione 1:N con cars)
| Nome Colonna | Tipo | Attributi | Indici |
|---|---|---|---|
| id | UNSIGNED INT | NOT NULL | PRIMARY KEY |
| name | VARCHAR(15) | NOT NULL | INDEX |
| description | TEXT | NULL | |

### Schema tabella `years` (relazione 1:N con cars)
| Nome Colonna | Tipo | Attributi | Indici |
|---|---|---|---|
| id | UNSIGNED INT | NOT NULL | PRIMARY KEY |
| name | year | NOT NULL | INDEX |

### Schema tabella `imgs` (relazione 1:1 con cars)
| Nome Colonna | Tipo | Attributi | Indici |
|---|---|---|---|
| id | UNSIGNED INT | NOT NULL | PRIMARY KEY |
| name | TEXT | NULL | |