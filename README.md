# Primero
Primer repositorio creado por Izan Martín Velasco

## Intro
Este es mi primer repositorio y mi primera práctica de 1 DAM en github

## Índice
   <table>
    <tr>
        <td>Indice</td>
    </tr>
    <tr>
        <td>Introduccion</td>
    </tr>
    <tr>
        <td>Explicacion del codigo</td>
    </tr>
    <tr>
        <td>Codigo</td>
    </tr>
    <tr>
        <td>Bugs</td>
    </tr>
    <tr>
        <td>Nuevas resoluciones y cambios</td>
    </tr>
</table>

### Inicio
Vamos a porbar el código de un ejercicio resuelto sobre un gestor de contraseñas

#### Código 
/*
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 * Click nbfs://nbhost/SystemFileSystem/Templates/Classes/Class.java to edit this template
 */
package com.jdh.entornos;

/**
 * @author imanol.marroj
 */
public class GestorContraseñas {

    // Atributos
    private final String contraseña;
    private int minChars = 4;
    private int maxChars = 32;

    // Constructor

    /**
     * Contrusctor con intervalo por defecto [4, 32].
     *
     * @param pContraseña Contraseña del usuario.
     */
    public GestorContraseñas(String pContraseña) {
        contraseña = pContraseña;
    }

    /**
     * Contrusctor con intervalo definido [pMin, pMax].
     *
     * @param pContraseña Contraseña del usuario.
     * @param pMin        Mínimo de carácteres de la contraseña.
     * @param pMax        Máximo de carácteres de la contraseña.
     */
    public GestorContraseñas(String pContraseña, int pMin, int pMax) {
        contraseña = pContraseña.trim();
        minChars = pMin;
        maxChars = pMax;
    }

    // Métodos

    /**
     * Este método valida si la cantidad de carácteres de la contraseña está
     * dentro del intervalo definido.
     *
     * @return true si la longitud de {@link GestorContraseñas#contraseña} es
     * mayor o igual que {@link GestorContraseñas#minChars} y menor o igual que
     * {@link GestorContraseñas#maxChars}.
     */
    public boolean intervaloCaracteres() {
        boolean resultado = false;
        // TODO
        return (resultado);
    }

    /**
     * Indica si la contraseña incluye carácteres en minúscula.
     *
     * @return true si tiene minusculas; false si no.
     */
    public boolean tieneMinusculas() {
        // TODO
        return (false);
    }

    /**
     * Indica si la contraseña incluye carácteres en mayúsculas.
     *
     * @return true si tiene mayúsculas; false si no.
     */
    public boolean tieneMayusculas() {
        // TODO
        return (false);
    }

    /**
     * Revisa si la contraseña tiene carácteres especiales
     *
     * @return true si la contraseña tiene carácteres que no sean alfanuméricos
     * y que no sea null.
     */
    public boolean tieneCaracteresEspeciales() {
        return (contraseña == null || contraseña.equals(""))
                ? false : contraseña.matches("[^A-Za-z0-9 ]");
    }

    /**
     * Calcula una puntuación según el nivel de seguridad de la contraeña
     * (cuanto más alto, mayor el nivel de seguridad).
     *
     * @return integer entre el 1 y el 5, según el nivel de seguridad.
     */
    public int evaluarSeguridad() {
        int puntuacion = 1;
        if (intervaloCaracteres())
            puntuacion++;
        if (tieneMinusculas())
            puntuacion++;
        if (tieneMayusculas())
            puntuacion++;
        if (tieneCaracteresEspeciales())
            puntuacion++;

        return (puntuacion);
    }
}
****
