# Primer-avance
Primer avance 
'''mermaid
flowchart TD
    A[Inicio] --> B{¿Ya tienes cuenta?}
    B -- Sí --> C[Iniciar sesión]
    B -- No --> D[Registrarse]
    C --> E{¿Inicio de sesión exitoso?}
    E -- Sí --> F[Acceder al sistema]
    E -- No --> G[Mostrar error de inicio de sesión]
    D --> H{¿Registro exitoso?}
    H -- Sí --> I[Iniciar sesión]
    H -- No --> J[Mostrar error de registro]
    F --> K{¿Deseas salir?}
    G --> K
    J --> K
    K -- Sí --> L[Salir]
    K -- No --> M[Continuar en el sistema]
