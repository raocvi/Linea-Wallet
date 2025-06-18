# Estructura de Datos

Se sugiere crear las siguientes tablas (listas de SharePoint o Dataverse):

## Clientes
- **NombreCliente** (Texto)
- **Correo** (Texto)
- **Telefono** (Texto)
- **Direccion** (Texto)

## Usuarios
- **Nombre** (Texto)
- **Rol** (Opciones: Vendedor, Gerente, Administrador, Secretaria)
- **Correo** (Texto)

## Marcas
- **NombreMarca** (Texto)
- **Descripcion** (Texto)

## Productos
- **NombreProducto** (Texto)
- **Marca** (Búsqueda a *Marcas*)
- **Precio** (Número)

## Oportunidades
- **Cliente** (Búsqueda a *Clientes*)
- **Vendedor** (Búsqueda a *Usuarios*)
- **Estado** (Opciones: Sospechoso, Prospecto, Analisis, Negociacion, Cierre, Orden, Pago)
- **FechaInicio** (Fecha)
- **FechaCierreEsperada** (Fecha)
- **ValorCotizado** (Moneda)
- **ProductosRelacionados** (Tabla relacionada a *Productos*)
- **Comentarios** (Texto enriquecido o relación a tabla *Comentarios*)

## Comentarios
- **Oportunidad** (Búsqueda a *Oportunidades*)
- **Usuario** (Búsqueda a *Usuarios*)
- **Comentario** (Texto de varias líneas)
- **Fecha** (Fecha y hora)

## Tareas
- **Oportunidad** (Búsqueda a *Oportunidades*)
- **AsignadoA** (Búsqueda a *Usuarios*)
- **Descripcion** (Texto)
- **FechaVencimiento** (Fecha)
- **EstadoTarea** (Opciones: Pendiente, Completada)
