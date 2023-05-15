## Ajustes archivo spec

Editar el archivo package.py  de wrf para la compilación de WRF+Chem

~~~bash
spack edit wrf 
~~~~
Se agregan como dependencias bison y flex (se indican los número de línea )

~~~bash
192     depends_on("bison", when="+chem")
193     depends_on("flex", when="+chem")
....
224             env.set("WRF_KPP", 1)
225             env.set("YACC", self.spec["bison"].prefix+"/bin/yacc -d")
226             env.set("FLEX_LIB_DIR", self.spec["flex"].prefix+"/lib")
~~~

Se adjunta archivo package.py para referencia: spack version 0.20.0.dev0 (2dcc55d6c524048e56f7231b755d133af79cdf7b)

