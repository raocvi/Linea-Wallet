# Fórmulas de ejemplo (Power Fx)

Los siguientes fragmentos pueden emplearse dentro de formularios y botones de la aplicación.

## Crear una nueva oportunidad
```PowerFx
Patch(Oportunidades, Defaults(Oportunidades),
    {
        Cliente: ClienteDropdown.Selected,
        Vendedor: VendedorDropdown.Selected,
        Estado: "sospechoso",
        FechaInicio: Today(),
        FechaCierreEsperada: FechaCierreInput.SelectedDate,
        ValorCotizado: ValorCotizadoInput.Text,
        ProductosRelacionados: ProductosSeleccionados
    }
);
```

## Actualizar el estado de una oportunidad
```PowerFx
Patch(Oportunidades, ThisItem,
    { Estado: EstadoDropdown.Selected.Value }
);
```

## Agregar un comentario
```PowerFx
Collect(Comentarios,
    {
        Oportunidad: ThisItem,
        Usuario: User().Email,
        Comentario: TextoComentario.Text,
        Fecha: Now()
    }
);
```

## Crear una tarea
```PowerFx
Patch(Tareas, Defaults(Tareas),
    {
        Oportunidad: ThisItem,
        AsignadoA: UsuarioTareaDropdown.Selected,
        Descripcion: DescripcionTarea.Text,
        FechaVencimiento: FechaVencimientoInput.SelectedDate,
        EstadoTarea: "Pendiente"
    }
);
```
