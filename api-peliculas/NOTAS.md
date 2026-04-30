# 1. ¿Por qué es mejor tener el controlador separado de las rutas?

Porque si el día de mañana quiero añadir una nueva funcionalidad puedo hacerlo de una forma sencilla, sin depender de las rutas. Al igul que si quiero reutilizar estas funciones puedo hacerlo. Por otra parte el código queda mucho más legible y modular, lo que favorece el mantenimiento del mismo.

# 2. Si mañana quisieras cambiar los datos en memoria por una base de datos PostgreSQL, ¿en qué archivo harías el cambio principalmente?

Los principales y notorios cambios se haría en el archivo peliculas.js de la carpeta data

# 3. ¿Qué pasaría si en el router tuvieras /:id antes que /:id/resenas? Pruébalo y describe el resultado.

En el código que se proporciona en el ejercicio aparece antes las rutas /:id que las de /:id/resenas y ambas funcionan perfectamente. He estado investigando y en teoría como las /:id aparecen primero cuando se hace un get /:id/resenas no debería de aparecer las reseñas de esa película, pero si aparecen. Esto se debe a que no hay una ruta estática con dos segmentos, si la hubiera debería de ir antes, porque sino interpretaría que esa parte de la ruta estática es un id o el parámetro que se buscara.
