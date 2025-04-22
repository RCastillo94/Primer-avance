# Entrega final
Entraga final
```mermaid
flowchart TD
    A -->|Inicio| B[Mostrar Menú Principal]
    B -->|Seleccionar 'Iniciar Sesión'| C[Ingresar Cédula]
    C --> D{Usuario Encontrado?}
    D -->|Sí| E[Mostrar Menú del Usuario]
    D -->|No| F[Mostrar Mensaje de Error]
    F --> C 
    
    E -->|Seleccionar Opción| G{Rol del Usuario}
    G -->|Gerente| H[Mostrar Menú Gerente]
    G -->|Vendedor| I[Mostrar Menú Vendedor]

    H -->|Gestionar Usuarios| J[Registrar/Modificar/Eliminar Usuario]
    H -->|Gestionar Inventario| K[Agregar/Modificar/Eliminar Producto]
    H -->|Registrar Ventas| L[Registrar Venta]
    H -->|Salir| A 

    I -->|Registrar Ventas| L
    I -->|Mostrar Inventario| K
    I -->|Salir| A[Reiniciar programa]

    J -->|Registrar Usuario| M[Ingresar Datos del Usuario]
    J -->|Modificar Usuario| N[Modificar Datos del Usuario]
    J -->|Eliminar Usuario| O[Eliminar Usuario]

    K -->|Agregar Producto| P[Ingresar Datos del Producto]
    K -->|Modificar Producto| Q[Modificar Datos del Producto]
    K -->|Eliminar Producto| R[Eliminar Producto]
    K -->|Mostrar Inventario| S[Mostrar Lista de Productos]

    L -->|Ingresar Nombre del Producto| T[Ingresar Cantidad a Vender]
    T --> U{Inventario Suficiente?}
    U -->|Sí| V[Completar Venta]
    U -->|No| W[Mostrar Mensaje de inventario Insuficiente]
