## Mapa de ventanas de la aplicación 

En el siguiente mapa se muestran la páginas presentes en la aplicación, así como la relación entre ellas.

En cada elemento anidado se podra subir de manera directa el elemento padre.

```mermaid
stateDiagram-v2
Home --> Nosotros
Home --> Contacto
Home --> Login
Login --> Usuario
Login --> Abogado
Login --> Administrador
Home --> Registro
state Usuario{
	MisProcesos
	MisPagos
	MisNotificaciones
	NuevoProceso
}
state Abogado{
	CasosAsignados
	Notificaciones
	state CasosAsignados{
		ActualizarStatus
		SolicitudCargaDeInformación
		Documentos
		state Documentos{
			CargarNuevoDocumento
			Actualizar
		}
	}
}
state Administrador{
	NuevosCasos
	Pagos
}
Registro --> Login

```

