Restricciones de integridad referencial...
NO ACTION: Cuando borras algo en la tabla padre no afecta a las hijas q contengan información derivada de esa.
CASCADE: Seria lo contrario a no action. Osea, si me cargo una, acabo con todas las que guarden relación.(Borra los registros de la tabla dependiente cuando se borra el registro de la tabla principal)
SET NULL: Establece NULL como valor a una tabla que se ve afectada por algo de la principal
SET DEAFULT: Das un valor por defecto a la columna
MATCH FULL:
MATCH PARTIAL:
