# Proyecto Intermodular <img src="LogoEmpresa.png" alt="Icono" width="60"/>

# 📊 Servicio de Reparación de Ordenadores  

# Subsistema de Informes 

# ![Logo de la Empresa](https://github.com/wendolin-byte/Informes-Sistema-de-Reparaciones/blob/main/logo-informes.jpg?raw=true)


---

## 📌 Índice

- [🔍 Descripción del Subsistema](#descripción-del-subsistema)
- [🛠 Funcionalidades](#funcionalidades)
- [🌐 Páginas Bootstrap](#páginas-bootstrap)
- [📄 Código Java](#código-java)
- [👥 Integrantes del Grupo](#integrantes-del-grupo)
- [⚠️ Notificaciones](#notificaciones)

---

## 🔍 Descripción del Subsistema

Este subsistema permite generar informes útiles para el seguimiento y control de las reparaciones, materiales, técnicos y clientes. Forma parte del proyecto colaborativo de reparación de ordenadores.

---

## 🛠 Funcionalidades

- 💰 Informes financieros (costos, ingresos, rentabilidad).
- 🧰 Inventario de materiales (stock, consumo, alertas).
- 👨‍🔧 Rendimiento del personal técnico.
- 😊 Satisfacción del cliente (encuestas).
- 📤 Exportación de informes a PDF o Excel.
- 📥 Importación de datos desde ficheros.

---
## 👥 Equipo

Este proyecto ha sido desarrollado por:
👨 Manuel Rubio – Gestión de Materiales
👨 Lucas Alamar – Gestión de Personal
👨 Ruben Sánchez – Gestión de Reparaciones
👨 Alejandro Farinós – Gestión de Clientes
👩 Irma Domínguez – Generación de Informes

---

## 🌐 Páginas Bootstrap

Puedes navegar por las páginas del subsistema directamente desde aquí:

- [📋 Encuesta de Satisfacción](https://wendolin-byte.github.io/Informes-Sistema-de-Reparaciones/wireframe-bootstrap/Encuesta.html)
- [💰 Informe Financiero](https://wendolin-byte.github.io/Informes-Sistema-de-Reparaciones/wireframe-bootstrap/Financiero.html)
- [📦 Informe de Inventario](https://wendolin-byte.github.io/Informes-Sistema-de-Reparaciones/wireframe-bootstrap/Inventario.html)
- [👨‍🔧 Rendimiento del Personal](https://wendolin-byte.github.io/Informes-Sistema-de-Reparaciones/wireframe-bootstrap/RendimientoPersonal.html)
- [📑 SubInforme Principal](https://wendolin-byte.github.io/Informes-Sistema-de-Reparaciones/wireframe-bootstrap/SubInformePrincipal.html)
- [📊 Tipo de Informes](https://wendolin-byte.github.io/Informes-Sistema-de-Reparaciones/wireframe-bootstrap/TipoInformes.html)

---
## 🌐 Capturas de Pantalla de las páginas

### 🖼️ Vista de Subinforme Principal
![Subinforme](Capturas/SubsistemaInforme.png)

### 📊 Vista de Tipo de Informes
![Tipo de Informes](Capturas/TipoInformes.png)

### 💰 Vista del Informe Financiero
![Informe Financiero](Capturas/Financiero.png)

### 👨‍🔧 Vista del Rendimiento del Personal
![Rendimiento del Personal](Capturas/Personal.png)

### 📦 Vista del Inventario
![Inventario](Capturas/Inventario.png)

### 😊 Encuesta de Satisfacción
![Encuesta](Capturas/Encuesta.png)

---


## 📄 Código Java

```java
import java.util.ArrayList;
/**
 * @author Irma
 */
public class GestionPersonal {
    private ArrayList<Empleado> empleados;

    public GestionPersonal() {
        empleados = new ArrayList<>();
    }

    public void agregarEmpleado(Empleado e) {
        empleados.add(e);
    }

    public void generarInformeGeneral() {
        System.out.println("===== INFORME DE EMPLEADOS =====");
        for (Empleado e : empleados) {
            System.out.println(e.generarInforme());
        }
    }

    public boolean eliminarEmpleado(String nombre) {
        for (Empleado e : empleados) {
            if (e.getNombre().equalsIgnoreCase(nombre)) {
                empleados.remove(e);
                return true;
            }
        }
        return false;
    }

    public ArrayList<Empleado> getListaEmpleados() {
        return empleados;
    }
}

```

---

## ⚠️ Notificaciones
- ✅ Estado actual: Sitio funcionando de forma correcta
- ⚠️ Advertencia: Para generar los Informes Generales debe lograrse la conexión final con los otros subsistemas
- ❗ Importante: Aún está pendiente lograr la exportación de los Informes a formatos PDF y EXCEL.

