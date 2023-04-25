# ** IMPORTANTE, ES OBLIGATORIO QUE SE HAYA INSTALADO GIT CON PERMISOS DE ADMINISTRADOR, DE NO SER ASÍ NO PODRAS ACCEDER A LA RUTA DE MANEJO DE CREDENCIALES **

## Consultar lista de keys secretas
*gpg --list-secret-keys*

## Eliminar una key de la lista
*gpg --delete-secret-key "NombreDeUsuario"*

------------------------------------------------
# ** DEBES HABER INTENTADO HACER AL MENOS UN COMMIT ANTERIORMENTE Y GENERADO UN TOKEN DE ACCESO PERSONAL EN GITHUB **

## Para solucionar el error...

*error: gpg failed to sign the data*
*fatal: failed to write commit object*

## Usar el siguiente comando
*echo "test" | gpg --clearsign*

## Mostrará el siguiente mensaje de error...

*-----BEGIN PGP SIGNED MESSAGE-----
Hash: SHA512*

*test
gpg: signing failed: Inappropriate ioctl for device
gpg: [stdin]: clear-sign failed: Inappropriate ioctl for device*



## Usar el siguiente comando
*export GPG_TTY=$(tty)*

## Esos comandos solo serviran mientras la terminal se mantenga abierta, sin embargo se puede configurar para que el token se mantenga activo

## Usar el siguiente comando
*nano .zshrc*

![image](https://user-images.githubusercontent.com/85717673/234409603-25a7d5e1-44fa-4a77-b40b-b79ac88ef5ec.png)

## Añadir el comando *export GPG_TTY=$(tty)* debajo del texto "export" resatado en color verde

![image](https://user-images.githubusercontent.com/85717673/234410099-94b5f14c-0c4b-4294-b201-808dca5347ff.png)

## Presionar "ctrl + x" para salir y guardar los cambios confirmando con "y"

![image](https://user-images.githubusercontent.com/85717673/234410508-cc8c5e11-d27e-454b-9223-d371e1b6f78c.png)

