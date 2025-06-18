# Flujos de Power Automate

A continuación se describen los flujos recomendados para completar la funcionalidad del CRM.

## Notificación de nueva oportunidad
1. **Disparador:** Cuando se cree un elemento en la lista *Oportunidades*.
2. **Acciones:**
   - Obtener los detalles de la oportunidad.
   - Enviar un correo al vendedor asignado y, opcionalmente, al gerente.
   - Mensaje sugerido: "Se ha creado una nueva oportunidad para el cliente X".

## Notificación de nueva tarea
1. **Disparador:** Cuando se cree un elemento en la lista *Tareas*.
2. **Acciones:**
   - Obtener los detalles de la tarea.
   - Enviar un correo al usuario asignado indicando la descripción y fecha de vencimiento.

## Recordatorio de vencimientos
1. **Disparador:** Flujo recurrente diario.
2. **Acciones:**
   - Filtrar tareas u oportunidades con fecha de vencimiento en los próximos 3 días.
   - Enviar recordatorio por correo o Teams a los usuarios responsables.
