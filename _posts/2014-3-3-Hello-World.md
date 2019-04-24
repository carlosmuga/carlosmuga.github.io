---
layout: post
title: INYECCION DE DEPENDENCIAS
---
En informática, inyección de dependencias (en inglés Dependency Injection, DI) es un patrón de diseño orientado a objetos, en el que se suministran objetos a una clase en lugar de ser la propia clase la que cree dichos objetos. Esos objetos cumplen contratos que necesitan nuestras clases para poder funcionar (de ahí el concepto de dependencia). Nuestras clases no crean los objetos que necesitan, sino que se los suministra otra clase 'contenedora' que inyectará la implementación deseada a nuestro contrato.

siempre ha sido uno de los conceptos que cuesta entender en el mundo del desarrollo de software sobre todo a la gente que esta empezando. ¿Para qué sirve este patrón de diseño y cual es su utilizad? Normalmente cuando nosotros programamos en el día a día con la programación orientada a objeto nos encontramos construyendo objetos y relacionando objetos utilizando dependencias.

https://www.arquitecturajava.com/wp-content/uploads/inyecciondependenciaobjeto.png


Por ejemplo podemos tener un programa principal que use un sencillo servicio de impresión para imprimir un documento.

package com.arquitecturajava;
public class ServicioImpresion {
  
  public void imprimir() {
    
    System.out.println("enviando el documento a imprimir");
    
    System.out.println("imprimiendo el documento en formato pdf");
  }
}

Utilizamos un programa main e imprimimos:

package com.arquitecturajava;
public class Principal {
  public static void main(String[] args) {
  
    ServicioImpresion miServicio= new ServicioImpresion();
    
    miServicio.imprimir();
  }
}



