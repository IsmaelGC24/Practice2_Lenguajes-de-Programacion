% Catálogo de vehículos
% vehiculo(Marca, Referencia, Tipo, Precio, Año)

vehiculo(toyota, corolla, sedan, 22000, 2022).
vehiculo(toyota, rav4, suv, 28000, 2022).
vehiculo(ford, mustang, sport, 45000, 2023).
vehiculo(ford, explorer, suv, 35000, 2022).
vehiculo(ford, focus, sedan, 21000, 2021).
vehiculo(bmw, x5, suv, 60000, 2021).
vehiculo(bmw, serie3, sedan, 45000, 2022).
vehiculo(honda, civic, sedan, 23000, 2021).
vehiculo(honda, crv, suv, 29000, 2023).
vehiculo(chevrolet, equinox, suv, 28000, 2022).
vehiculo(nissan, altima, sedan, 24000, 2023).

% Consultas básicas

cumple_presupuesto(Referencia, PresupuestoMax) :-
    vehiculo(_, Referencia, _, Precio, _),
    Precio =< PresupuestoMax.

cumple_tipo_presupuesto(Referencia, Tipo, PresupuestoMax) :-
    vehiculo(_, Referencia, Tipo, Precio, _),
    Precio =< PresupuestoMax.

% Agrupación por marca

vehiculos_por_marca(Marca, Referencias) :-
    findall(Ref, vehiculo(Marca, Ref, _, _, _), Referencias).

% Generar reporte con lista de vehículos y valor total

generar_reporte(Marca, Tipo, PresupuestoUnidad, [Inventario, ValorTotal]) :-
    findall(vehiculo(Marca, Ref, Tipo, Precio, Año),
            (vehiculo(Marca, Ref, Tipo, Precio, Año), Precio =< PresupuestoUnidad),
            Inventario),
    valor_total(Inventario, ValorTotal),
    ValorTotal =< 1000000.

valor_total([], 0).
valor_total([vehiculo(_, _, _, Precio, _) | T], Total) :-
    valor_total(T, Subtotal),
    Total is Subtotal + Precio.
