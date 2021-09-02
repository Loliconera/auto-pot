# Autopot
Esto es lo mismo let-me-pot</br>
- Soporte para el modo asesino.
- Soporte para quien no necesita usar poción solo en combate.</br>
- Soporte para Civil Unrest y la poción de Battleground.</br>
- Recarga del archivo por comandos (No necesita Relog o Reiniciar).</br>
- Requiere Caali's Proxy "tera-game-state"</br>

# Comandos
Comience escribiendo el comando **autopot** o **pot**

Toolbox(/8) | Descripción del comando
--- | ---
**pot** | abre la GUI
**pot id** [item link] | Obtenga una ID del artículo **Mantenga Presionada la tecla Shift + Clic Izquierdo** para el enlace del artículo
**pot hp** | Habilitar y deshabilitar el uso automático de la poción de HP
**pot mp** | Habilitar y deshabilitar el uso automático de la poción de MP **Habilitado por defecto**
**pot slaying** | Habilitar y deshabilitar el uso automático de la poción de HP con el modo asesino
**pot reload hp** | Recargue el archivo HP.json **abra su inventario para actualizar la cantidad del artículo**
**pot reload mp** | Recargue el archivo MP.json **abra su inventario para actualizar la cantidad del artículo**
**pot reload config** | Recargar archivo Config.json
**pot debug** | Mostrar DEBUG

***HP Pot modo de asesino solo se usa en combate***</br>
***La poción no se usará cuando esté montada y en contrato.***</br>
***para la poción de battleground, debes configurarla tú mismo***</br>
***config.json, hp.json, mp.json se generará después de ingresar al juego***</br>

## Menú GUI
* En el canal de chat **Toolbox(/8)** escriba el siguiente comando **pot** para mostrar una interfaz gráfica de usuario del modulo.   
  ![](https://i.imgur.com/NVztT13.png)   

# Config.json
```
{
    "enabled": true,    //habilitar y deshabilitar este módulo
    "hp": false,        //Si se establece true = Habilitar el uso automático de la poción de HP
    "mp": true,         //Si se establece true = Habilitar el uso automático de la poción de MP
    "slaying": false,   //Si se establece true = Habilitar modo asesino
    "notice": false     //Si se establece true = Avisar cuando tu poción se acaba, false = no avisar
}
```
# HP.json
```
{
    "6552": {                               //Tu ID de poción (ItemId)
        "name": "Prime Recovery Potable",   //El nombre de tu poción para el aviso de artículo si está habilitado
        "inBattleground": false,            //Si se establece true = esta poción solo se usará en Civil Unrest y Battleground
        "inCombat": true,                   //Si se establece true = solo usar en combate, false = usar siempre ignorar combate
        "use_at": 80,                       //Establecer uso con x porcentaje
        "slay_at": 30,                      //Establecer el uso en el modo asesino con x porcentaje
        "cd": 10                            //Establecer el tiempo de reutilización de la poción x segundo
    }
}
```
# MP.json
```
{
    "6562": {                                   //Tu ID de poción (ItemId)
        "name": "Prime Replenishment Potable",  //El nombre de tu poción para el aviso de artículo si está habilitado
        "inBattleground": false,                //Si se establece true = esta poción solo se usará en Civil Unrest y Battleground
        "inCombat": false,                      //Si se establece true = solo usar en combate, false = usar siempre ignorar combate
        "use_at": 50,                           //Establecer uso con x porcentaje
        "cd": 10                                //Establecer el tiempo de reutilización de la poción x segundo
    }
}
```
## Créditos
- Original de Fukky -> https://github.com/Fukki/auto-pot
- Esta es una bifurcación de **Fukki** auto-pot.  

# Utilidad 
[Algo útil para nuevos usuarios](https://github.com/Fukki/auto-pot/issues/6)

# Preguntas & Respuestas
Pregunta: mi archivo *.json se reemplazó después de editar.</br>
Respuesta: verifique su sintaxis antes de guardar el archivo porque *.json reemplazará si el sistema no puede leer.</br>

Pregunta: después de recargar el archivo *.json con el comando del juego auto-pot no funciona.</br>
Respuesta: actualice su inventario abriéndolo una vez o use el artículo una vez.</br>

Pregunta: tengo un error.</br>
Respuesta: verifique que su Toolbox y el módulo Auto-Pot esté actualizado o no.</br>

Pregunta: cómo obtener el enlace del artículo para "pot id XXXX"</br>
Respuesta: solo mantenga presionada la tecla Shift izquierda + clic izquierdo en el articulo</br>
![image](https://user-images.githubusercontent.com/26898177/52502964-bb9c5c00-2c16-11e9-9019-0de08f5a06fb.png)</br>
***Cualquier problema, abra Issues**
