# {{Nombre de la Máquina}}

> **Plataforma:** DockerLabs  
> **Dificultad:** 🟢 Easy / 🟡 Medium / 🔴 Hard  
> **Sistema Operativo:** Linux / Windows  
> **Fecha de resolución:** DD/MM/AAAA  
> **Autor del writeup:** Raquel Romero

---

# 📖 Descripción

Breve descripción de la máquina y del objetivo del laboratorio.

---

# 🎯 Objetivos

- Enumerar los servicios expuestos.
    
- Identificar posibles vulnerabilidades.
    
- Obtener acceso inicial.
    
- Escalar privilegios.
    
- Obtener acceso como root/Administrator.
    

---

# 🛠️ Herramientas utilizadas

|Herramienta|Uso|
|---|---|
|Nmap|Enumeración|
|FFUF|Descubrimiento de directorios|
|Gobuster|Enumeración web|
|Burp Suite|Análisis de peticiones|
|Netcat|Reverse Shell|
|LinPEAS|Enumeración para escalada|
|Otros|...|

---

# 🧠 Metodología

```text
Reconocimiento
      ↓
Enumeración
      ↓
Análisis
      ↓
Explotación
      ↓
Acceso Inicial
      ↓
Escalada de Privilegios
      ↓
Root
```

---

# 1️⃣ Reconocimiento

## Descubrimiento de la máquina

Explica cómo identificaste la IP de la máquina.

### Evidencia

![Descubrimiento](https://chatgpt.com/c/images/01-discovery.png)

---

# 2️⃣ Enumeración

## Escaneo con Nmap

### Comando

```bash
nmap -sCV -Pn <IP>
```

### Resultado

```text
(Pegar aquí la salida)
```

### Análisis

Explica qué servicios llaman la atención y por qué.

### Evidencia

![Nmap](https://chatgpt.com/c/images/02-nmap.png)

---

# 3️⃣ Enumeración Web

## Acceso inicial

Describe la aplicación web.

### Evidencia

![Web](https://chatgpt.com/c/images/03-web.png)

---

## Directorios encontrados

### Comando

```bash
ffuf -u http://IP/FUZZ -w /ruta/wordlist.txt
```

### Resultado

Explica qué directorios encontraste.

### Evidencia

![FFUF](https://chatgpt.com/c/images/04-ffuf.png)

---

# 4️⃣ Análisis de la vulnerabilidad

## Vulnerabilidad encontrada

Describe la vulnerabilidad.

### ¿Por qué funciona?

Explica técnicamente qué ocurre.

---

# 5️⃣ Explotación

## Obtención del acceso inicial

Describe paso a paso cómo obtuviste la shell.

### Comandos utilizados

```bash
# Comandos
```

### Evidencia

![Shell](https://chatgpt.com/c/images/05-shell.png)

---

# 6️⃣ Escalada de privilegios

## Enumeración

Comandos utilizados.

```bash
sudo -l
find / -perm -4000 2>/dev/null
```

---

## Técnica utilizada

Explica la técnica de escalada.

---

## Evidencia

![Root](https://chatgpt.com/c/images/06-root.png)

---

# 7️⃣ Resumen del ataque

|Fase|Descripción|
|---|---|
|Reconocimiento||
|Enumeración||
|Explotación||
|Acceso inicial||
|Escalada||
|Root||

---

# 🛡️ MITRE ATT&CK

|Táctica|Técnica|
|---|---|
|Reconnaissance||
|Initial Access||
|Execution||
|Privilege Escalation||
|Credential Access||
|Discovery||

---

# 🔍 Indicadores encontrados (IoCs)

|Tipo|Valor|
|---|---|
|Puerto||
|Servicio||
|Usuario||
|Archivo||
|Credencial||

---

# 💡 Lecciones aprendidas

- Qué has aprendido con esta máquina.
    
- Qué harías diferente.
    
- Qué técnica era nueva para ti.
    

---

# 📚 Referencias

- DockerLabs
    
- HackTricks
    
- GTFOBins
    
- PayloadsAllTheThings
    
- Documentación oficial de las herramientas utilizadas
    

---

# ✅ Conclusiones

Resumen personal de la máquina:

- Dificultad percibida:
    
- Técnicas utilizadas:
    
- Aspectos más interesantes:
    
- Recomendación para otros estudiantes:
    

---

# 📂 Estructura de archivos

```text
FindYourStyle/
│
├── README.md
└── images/
    ├── 01-discovery.png
    ├── 02-nmap.png
    ├── 03-web.png
    ├── 04-ffuf.png
    ├── 05-shell.png
    └── 06-root.png
```