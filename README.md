# Plan_Sis_Inf

Instalando git en usb 

https://github.com/sheabunge/GitPortable

Ejecutamos el archivo *.paf.exe -> este descarga los archivos base.
	D:\GitPortable\App\Git\GitPortable_2.27.0.windows.1_Development_Test_1_online.paf.exe

Ejecutamos: "D:\GitPortable\App\Git\git-bash.exe" --no-needs-console --hide --no-cd --command=post-install.bat
	  Descarga e instala git client.

Creamos las llaves ssh para conectarnos con GitHub
$ mkdir .ssh
$  ssh-keygen -o
	cambiar la ruta por defecto /.ssh/id_rsa

Copiamos la llave publica a nuestras llaves ssh-key de Github
$ cat id_rsa.pub

Indicamos al agente para que maneje nuestras llaves
	$ eval "$(ssh-agent -s)"
	$ ssh-add /.ssh/id_rsa

Testeamos con git-hub
	$ ssh -T git@github.com

Clonamos nuestro repositorio de Github previamente creado.
 	$ git clone git@github.com:edgargregori/Plan_Sis_Inf.git

Añadimos las excepciones de seguridad para esta carpeta
	git config --global --add safe.directory D:/GitPortable/App/Git/PortableGit/Plan_Sis_Inf

Configuramos nuestras credenciales GitHub:
	  git config --global user.email "you@example.com"
	  git config --global user.name "Your Name"

Realizamos cambios en nuestro directorio -> confirmamos -> colocamos en GitHub.
 	$ git status
	$ git add .
	$ git commit -m "mensaje"
	$ git push origin main

Si hay cambios de otros usuario o ramas:
	$ git fetch origin main


	






		