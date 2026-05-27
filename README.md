# ---------------------------------------------------------
# Nombre: Javier Dario Santos Montes
# Grupo: 213022_879
# Programa: Ingeniería de Sistemas
# Código Fuente: Autoría propia
# ---------------------------------------------------------

# Matriz de sesiones de clientes
sesiones = [
    ["C001", 240, 12],
    ["C002", 45, 2],
    ["C003", 120, 5],
    ["C004", 300, 15],
    ["C005", 70, 4]
]

# Función para clasificar el compromiso
def clasificar_compromiso(duracion, clics):

    if duracion > 180 and clics > 8:
        return "Alto"

    elif duracion < 60 or clics < 3:
        return "Bajo"

    else:
        return "Medio"

# Mostrar informe final
print("======================================")
print(" INFORME DE COMPROMISO DE CLIENTES ")
print("======================================")

for sesion in sesiones:

    id_cliente = sesion[0]
    duracion = sesion[1]
    clics = sesion[2]

    clasificacion = clasificar_compromiso(duracion, clics)

    print(f"Cliente: {id_cliente}")
    print(f"Duración: {duracion} segundos")
    print(f"Clics: {clics}")
    print(f"Clasificación: {clasificacion}")
    print("--------------------------------------")
