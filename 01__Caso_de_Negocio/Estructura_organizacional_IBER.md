# Estructura organizacional de IBER

## Propósito

Representación normalizada del organigrama proporcionado por el cliente. Este documento prioriza una estructura explícita y fácil de interpretar tanto por personas como por sistemas de inteligencia artificial.

## Jerarquía organizacional

- **Dirección**
  - **Gerente General**
    - **Jefatura de Gestión Humana**
    - **Jefatura de Operaciones y Ventas**
      - **Encargados de Tiendas**
        - **Colaboradores de Tiendas**
    - **Gerente Comercial**
      - **Jefatura de Compras**
        - **Asistente de Compras**
      - **Encargado del Centro Logístico**
        - **Auxiliares de Depósito**
    - **Jefatura de Marketing**
      - **Asistentes de Marketing**
    - **Brand Ambassador**
      - **Asistentes del Brand Ambassador**
    - **Gerencia de Administración**
      - **Asistentes de Administración**

## Relaciones de dependencia

| ID | Área o posición | Reporta directamente a |
| --- | --- | --- |
| `direccion` | Dirección | — |
| `gerente_general` | Gerente General | Dirección |
| `jefatura_gestion_humana` | Jefatura de Gestión Humana | Gerente General |
| `jefatura_operaciones_ventas` | Jefatura de Operaciones y Ventas | Gerente General |
| `encargados_tiendas` | Encargados de Tiendas | Jefatura de Operaciones y Ventas |
| `colaboradores_tiendas` | Colaboradores de Tiendas | Encargados de Tiendas |
| `gerente_comercial` | Gerente Comercial | Gerente General |
| `jefatura_compras` | Jefatura de Compras | Gerente Comercial |
| `asistente_compras` | Asistente de Compras | Jefatura de Compras |
| `encargado_centro_logistico` | Encargado del Centro Logístico | Gerente Comercial |
| `auxiliares_deposito` | Auxiliares de Depósito | Encargado del Centro Logístico |
| `jefatura_marketing` | Jefatura de Marketing | Gerente General |
| `asistentes_marketing` | Asistentes de Marketing | Jefatura de Marketing |
| `brand_ambassador` | Brand Ambassador | Gerente General |
| `asistentes_brand_ambassador` | Asistentes del Brand Ambassador | Brand Ambassador |
| `gerencia_administracion` | Gerencia de Administración | Gerente General |
| `asistentes_administracion` | Asistentes de Administración | Gerencia de Administración |

## Representación estructurada

```json
{
  "organizacion": "IBER",
  "estructura": {
    "id": "direccion",
    "nombre": "Dirección",
    "dependencias": [
      {
        "id": "gerente_general",
        "nombre": "Gerente General",
        "dependencias": [
          {
            "id": "jefatura_gestion_humana",
            "nombre": "Jefatura de Gestión Humana",
            "dependencias": []
          },
          {
            "id": "jefatura_operaciones_ventas",
            "nombre": "Jefatura de Operaciones y Ventas",
            "dependencias": [
              {
                "id": "encargados_tiendas",
                "nombre": "Encargados de Tiendas",
                "dependencias": [
                  {
                    "id": "colaboradores_tiendas",
                    "nombre": "Colaboradores de Tiendas",
                    "dependencias": []
                  }
                ]
              }
            ]
          },
          {
            "id": "gerente_comercial",
            "nombre": "Gerente Comercial",
            "dependencias": [
              {
                "id": "jefatura_compras",
                "nombre": "Jefatura de Compras",
                "dependencias": [
                  {
                    "id": "asistente_compras",
                    "nombre": "Asistente de Compras",
                    "dependencias": []
                  }
                ]
              },
              {
                "id": "encargado_centro_logistico",
                "nombre": "Encargado del Centro Logístico",
                "dependencias": [
                  {
                    "id": "auxiliares_deposito",
                    "nombre": "Auxiliares de Depósito",
                    "dependencias": []
                  }
                ]
              }
            ]
          },
          {
            "id": "jefatura_marketing",
            "nombre": "Jefatura de Marketing",
            "dependencias": [
              {
                "id": "asistentes_marketing",
                "nombre": "Asistentes de Marketing",
                "dependencias": []
              }
            ]
          },
          {
            "id": "brand_ambassador",
            "nombre": "Brand Ambassador",
            "dependencias": [
              {
                "id": "asistentes_brand_ambassador",
                "nombre": "Asistentes del Brand Ambassador",
                "dependencias": []
              }
            ]
          },
          {
            "id": "gerencia_administracion",
            "nombre": "Gerencia de Administración",
            "dependencias": [
              {
                "id": "asistentes_administracion",
                "nombre": "Asistentes de Administración",
                "dependencias": []
              }
            ]
          }
        ]
      }
    ]
  }
}
```
