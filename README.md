# Informes-Sistema-de-Reparaciones
Subsistema Informes Irma Wendolin

# ![Logo de la Empresa](https://github.com/wendolin-byte/Informes-Sistema-de-Reparaciones/blob/main/logo.jpg?raw=true)

# 📊 Subsistema de Informes - Proyecto Intermodular

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

## 🌐 Páginas Bootstrap

Puedes navegar por las páginas del subsistema directamente desde aquí:

- [📋 Encuesta de Satisfacción](https://wendolin-byte.github.io/Informes-Sistema-de-Reparaciones/wireframe-bootstrap/Encuesta.html)
- [💰 Informe Financiero](https://wendolin-byte.github.io/Informes-Sistema-de-Reparaciones/wireframe-bootstrap/Financiero.html)
- [📦 Informe de Inventario](https://wendolin-byte.github.io/Informes-Sistema-de-Reparaciones/wireframe-bootstrap/Inventario.html)
- [👨‍🔧 Rendimiento del Personal](https://wendolin-byte.github.io/Informes-Sistema-de-Reparaciones/wireframe-bootstrap/RendimientoPersonal.html)
- [📑 SubInforme Principal](https://wendolin-byte.github.io/Informes-Sistema-de-Reparaciones/wireframe-bootstrap/SubInformePrincipal.html)
- [📊 Tipo de Informes](https://wendolin-byte.github.io/Informes-Sistema-de-Reparaciones/wireframe-bootstrap/TipoInformes.html)

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

---

## ⚠️ Notificaciones
✅ Estado actual: Sitio funcionando correctamente
⚠️ Advertencia: Para generar los Informes Generales debe lograrse la conexión final con los otros subsistemas
❗ Importante: Aún está pendiente lograr la exportación de los Informes a formatos PDF y EXCEL.

