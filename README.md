# Solución Problema 3 - Auditoría de inventario
# Autor: [Tu nombre]
# Curso: Fundamentos de Programación - UNAD

def calcular_pedido(stock_actual, stock_minimo):
    """
    Calcula la cantidad a pedir para un artículo.
    Retorna la diferencia si stock_actual < stock_minimo, sino 0.
    """
    if stock_actual < stock_minimo:
        return stock_minimo - stock_actual
    else:
        return 0
def main():
    # Matriz de inventario: [Código, Nombre, Stock Actual, Stock Mínimo]
    inventario = [
        ["A101", "Mouse USB", 5, 10],
        ["B202", "Teclado mecánico", 3, 8],
        ["C303", "Monitor 24\"", 2, 5],
        ["D404", "Audífonos", 12, 10],
        ["E505", "Webcam", 0, 7]
    ]
    print("=== LISTA DE PEDIDOS ===")
    print("Nombre del artículo | Cantidad a pedir")
    print("-" * 35) 
    for articulo in inventario:
        nombre = articulo[1]
        actual = articulo[2]
        minimo = articulo[3]
        pedido = calcular_pedido(actual, minimo)
        print(f"{nombre:20} | {pedido}")
        # Opcional: si quieres mostrar también los códigos, modifica la línea anterior.
# Punto de entrada del programa
if __name__ == "__main__":
    main()
