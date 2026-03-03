# Branding Iframes - EquiArena

Documento de referencia para mantener consistente el branding del microfrontend de **EquiArena** y su visualizacion embebida en iframe dentro del CRM.

## Alcance

- Microfrontend: `equi-arena-CRM`
- Shell embebedor: `crm-geofal` modulo EquiArena
- Flujo: CRM abre `https://equi-arena.geofal.com.pe` en dialog modal con `token` y opcionalmente `ensayo_id`

## Reglas visuales

- Mantener estilo tipo hoja tecnica, fiel a la plantilla Excel oficial de EquiArena.
- Preservar estructura de encabezado institucional y bloque ASTM D2419-22.
- Mantener botonera final con accion doble: `Guardar` y `Guardar y Descargar`.
- Mantener consistencia visual con GE Fino, GE Grueso, Gran Suelo y Gran Agregado.

## Contrato iframe

- Entrada por query params: `token`, `ensayo_id`.
- Mensajes hijo -> padre: `TOKEN_REFRESH_REQUEST`, `CLOSE_MODAL`.
- Mensaje padre -> hijo: `TOKEN_REFRESH`.

## Archivos clave

- `equi-arena-CRM/src/pages/EquiArenaForm.tsx`
- `equi-arena-CRM/src/App.tsx`
- `equi-arena-CRM/src/components/SessionGuard.tsx`
- `crm-geofal/src/components/dashboard/equi-arena-module.tsx`
