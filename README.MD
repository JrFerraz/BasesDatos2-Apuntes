Restricciones de integridad referencial...
NO ACTION: Cuando borras algo en la tabla padre no afecta a las hijas q contengan información derivada de esa.
CASCADE: Seria lo contrario a no action. Osea, si me cargo una, acabo con todas las que guarden relación.(Borra los registros de la tabla dependiente cuando se borra el registro de la tabla principal)
SET NULL: Establece NULL como valor a una tabla que se ve afectada por algo de la principal
SET DEAFULT: Das un valor por defecto a la columna
MATCH FULL:
MATCH PARTIAL:
CONSTRAIT (cname-derestricicon)
UNIQUE (<atrib>)
  RESTRICCIONES DE COMPROBACION
  CHECK predicado(atributos)
  ----> VALOR PREDET------> [[NOT]DEFERRABLE]
  INITIALLLY INMEDIATE | DEFERRABLE
  DROP SCHEMA
  ALTER TABLE
    COLUMNA | RESTRICCION
  ADD|DROP       ADD|DROP
INSERT INTO <nombre de la tabla>
 tipos de datos :
    datetime, nchar, integer
  va a caer ddl y dml
ISOMORFISMO CURRY HOWARD LAMBEK
  NUMEROS PG 
 -  INTEGER - DECIMAL -TEFALTAUNA
  
  nO PONER TEXT A TODO PRQ ESTA MAL
  
  CHAR---> LONGITUD FIJA
  VARCHAR ---> LONGITUD VARIABLE (LIMITADA)
  TEXT ---> VARIABLE (ILIMITADA)
  
  CASCADE 90% Y CON EL PERDEMOS DATOS
  EL WHERE ES OPTATIVOXd
  
  no hay porque hacer el seeect en el examen
  
  
  A buscar en el txt del examen
  -Datas -Cosas que implican varias tablas (explicando con que se deberia hacer)ç
  
  
  
  
  
  
  
  
  Ejercicio:
  -- CREATE TABLE Investigacion.Sede (
  
  CREATE TABLE Sede (
    Nome_Sede Nome_válido,
    Campus    Nome_Válido NOT NULL,
    CONSTRAINT PK_Sede
      PRIMARY KEY (Nome_Sede)
  );
  CREATE TABLE Departamento (
    Nome_Departamento Nome_Válido PRIMARY KEY,
    Telefono          CHAR(9)     NOT NULL,
    Director          Tipo_DNI
    --FK(Director)
  );
  CREATE TABLE Ubicación (
    Nome_Sede          Nome_Válido,
    Nome_Departamento  Nome_Válido,
    PRIMARY KEY (Nome_Sede, Nome_Departamento),
    CONTRAINT FK_Sede_Ubicación
      FOREIGN KEY (Nome_Sede)
      REFERENCES Sede (Nome_Sede),
    CONTRAINT FK_Departamento_Ubicacion
      FOREIGN KEY (Nome_Departamento)
      REFERENCES Departamento (Nome_Departamento),
      ON DELETE CASCADE
      ON UPDATE CASCADE
      --FK (Lider)
  );
  
  CREATE TABLE Profesor (
  DNI Tipo_DNI PRIMARY KEY,
  Nome_Profesor Nome_Válido NOT NULL,
  Titulación VARCHAR(20) NOT NULL,
  Experiencia Integer,
  N_Grupo     Nome_Válido
  N_Departamento Nome_Válido,
  FOREIGN KEY    (N_Grupo, N_Departamento)
    REFERENCES Grupo (Nome_Grupo, Nome_Departamento)
    ON DELETE SET NULL
    ON UPDATE CASCADE
  );
  
  ALTER TABLE Departamento
    ADD CONSTRAIT FK_Profesor_Departamento
      FOREIGN KEY (N_Grupo, N_Departamento)
      REFERENCES Grupo (Nome_Grupo, Nome_Departamento)
      ON DELETE SET NULL
      ON UPDATE SET NULL;
-- A FOREIGN KEY de Profesor está mal. Hacer una nueva
-- FOREIGN KEY con B:N M:N.
  ALTER TABLE Profesor
    DROP CONSTRAIT FK_Grupo_Profesor;
  ALTER TABLE Profesor
    ADD  CONSTRAIT FK_Grupo_Profesor
      FOREIGN KEY   (N_Grupo,   N_Departamento)
      REFERENCES Grupo (Nome)


---- El otro ejercicio

  CREATE TABLE Proxecto (
    Código_Proxecto Tipo_Código PRIMARY KEY,
    Nome_Proxecto    Nome_Válido NOT NULL,
    Orzamento        MONEY       NOT NULL,
    Data_Inicio      DATE        NOT NULL,
    Data_Fin         DATE,
    N_Gr             Nome_Válido,
    N_Dep            Nome_Válido,
    UNIQUE (Nome_Proxecto),
    CHECK (Data_Inicio < Data_Fin)
  }
  ALTER TABLE Proxecto
    ADD CONSTRAIT FK_Grupo_Proxecto
    FOREIGN KEY      (N_Gr,     N_Dep)
    REFERENCES Grupo (Nome_Grupo, Nome_Departamento)
    ON DELETE SET NULL
    ON UPDATE CASCADE;
  
  ALTER TABLE Proxecto
    ADD CONSTRAIT UNIQUE Data_Inicio_Única
      UNIQUE  (Data_Inicio);
      
      HAY QUE PEDIR EL OTRO EJEMPLO XD
      IAGO NO ME COPIES
ASDFGH
