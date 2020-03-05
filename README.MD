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
  -Datas -Cosas que implican varias tablas (explicando con que se deberia hacer)
