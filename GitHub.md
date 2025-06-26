Para **inicializar un repositorio Git** y **vincularlo con GitHub**, sigue estos pasos en tu terminal (Linux/macOS) o Git Bash (Windows):

---

### **1. Inicializar Git en tu proyecto local**
```sh
# Inicializa un repositorio Git en la carpeta actual
git init
```

---

### **2. Agregar archivos al área de preparación (staging)**
```sh
# Agrega todos los archivos modificados/nuevos
git add .
# O agrega un archivo específico
git add nombre_archivo
```

---

### **3. Hacer tu primer commit**
```sh
git commit -m "Primer commit: mensaje descriptivo"
```

---

### **4. Vincular el repositorio local con GitHub**
#### **Opción A: Si ya creaste el repositorio en GitHub**
```sh
# Conéctate al repositorio remoto (cambia la URL por la tuya)
git remote add origin https://github.com/tu-usuario/tu-repositorio.git
```

#### **Opción B: Si NO has creado el repositorio en GitHub**
1. Crea un repositorio nuevo en [github.com/new](https://github.com/new) (sin inicializar con README).  
2. Ejecuta:
```sh
git remote add origin https://github.com/tu-usuario/tu-repositorio.git
```

---

### **5. Subir cambios a GitHub (primer push)**
```sh
# Envía los commits a la rama 'main' (o 'master' en repositorios antiguos)
git push -u origin main
```
Si GitHub creó el repositorio con la rama por defecto `master`, usa:
```sh
git push -u origin master
```

---

### **Comandos adicionales útiles**
- Verifica la conexión remota:
  ```sh
  git remote -v
  ```
- Cambiar la URL del remoto (si te equivocaste):
  ```sh
  git remote set-url origin https://github.com/nueva-url.git
  ```

---

### **¿Problemas comunes?**
- **Error: "Remote origin already exists"**:  
  Elimínalo primero con:
  ```sh
  git remote remove origin
  ```
- **Error de autenticación**:  
  Usa [SSH](https://docs.github.com/es/authentication/connecting-to-github-with-ssh) o un [token de acceso](https://docs.github.com/es/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens) en lugar de contraseña.

---

### **Resumen gráfico del flujo**
```
git init → git add . → git commit -m "..." → git remote add origin [url] → git push -u origin main
```

¡Listo! Ahora tu repositorio local está sincronizado con GitHub. ¿Necesitas ayuda con algún paso en específico? 😊
