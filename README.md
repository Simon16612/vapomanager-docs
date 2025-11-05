> Documento de Arquitectura de Software (DAS)
>
> **Proyecto**
>
> VapoManager
>
> **Arquitectos**
>
> Simón Ochoa Ríos
>
> José Alejandro Valencia Henao

# Contenido {#contenido .TOC-Heading}

[**1.** **Propósito del proyecto**
[8](#propósito-del-proyecto)](#propósito-del-proyecto)

[**2.** **Motivadores de la arquitectura**
[9](#motivadores-de-la-arquitectura)](#motivadores-de-la-arquitectura)

[2.1 Restricciones técnicas
[9](#restricciones-técnicas)](#restricciones-técnicas)

[2.2 Restricciones de negocio
[12](#restricciones-de-negocio)](#restricciones-de-negocio)

[2.3 Atributos de calidad
[14](#atributos-de-calidad)](#atributos-de-calidad)

[2.3.1 Atributo calidad 1 [14](#_Toc181301414)](#_Toc181301414)

[2.3.1.1 Característica 1 [14](#_Toc181301415)](#_Toc181301415)

[2.3.1.1.1 Escenario de calidad 1 [14](#_Toc181301416)](#_Toc181301416)

[2.3.1.1.2 Escenario de calidad 2 [15](#_Toc181301417)](#_Toc181301417)

[2.3.1.1.3 Escenario de calidad 3 [15](#_Toc181301418)](#_Toc181301418)

[2.3.1.1.4 Escenario de calidad 4 [15](#_Toc181301419)](#_Toc181301419)

[2.3.1.1.5 Escenario de calidad 5 [16](#_Toc181301420)](#_Toc181301420)

[2.3.1.1.6 Escenario de calidad 6 [16](#_Toc181301421)](#_Toc181301421)

[2.3.1.2 Característica 2 [16](#_Toc181301422)](#_Toc181301422)

[2.3.1.2.1 Escenario de calidad 1 [16](#_Toc181301423)](#_Toc181301423)

[2.3.1.2.2 Escenario de calidad 2 [17](#_Toc181301424)](#_Toc181301424)

[2.3.1.2.3 Escenario de calidad 3 [17](#_Toc181301425)](#_Toc181301425)

[2.3.1.2.4 Escenario de calidad 4 [17](#_Toc181301426)](#_Toc181301426)

[2.3.1.2.5 Escenario de calidad 5 [18](#_Toc181301427)](#_Toc181301427)

[2.3.1.2.6 Escenario de calidad 6 [18](#_Toc181301428)](#_Toc181301428)

[2.3.1.2.7 Escenario de calidad 7 [18](#_Toc181301429)](#_Toc181301429)

[2.3.1.2.8 Escenario de calidad 8 [19](#_Toc181301430)](#_Toc181301430)

[2.3.1.2.9 Escenario de calidad 9 [19](#_Toc181301431)](#_Toc181301431)

[2.3.1.2.10 Escenario de calidad 10
[19](#_Toc181301432)](#_Toc181301432)

[2.3.1.2.11 Escenario de calidad 11
[19](#_Toc181301433)](#_Toc181301433)

[2.3.1.2.12 Escenario de calidad 12
[20](#_Toc181301434)](#_Toc181301434)

[2.3.2 Atributo calidad 2 [20](#_Toc181301435)](#_Toc181301435)

[2.3.2.1 Característica 1 [20](#_Toc181301436)](#_Toc181301436)

[2.3.2.1.1 Escenario de calidad 1 [20](#_Toc181301437)](#_Toc181301437)

[2.3.2.1.2 Escenario de calidad 2 [21](#_Toc181301438)](#_Toc181301438)

[2.3.2.1.3 Escenario de calidad 3 [21](#_Toc181301439)](#_Toc181301439)

[2.3.2.1.4 Escenario de calidad 4 [21](#_Toc181301440)](#_Toc181301440)

[2.3.2.1.5 Escenario de calidad 5 [22](#_Toc181301441)](#_Toc181301441)

[2.3.2.2 Característica 2 [22](#_Toc181301442)](#_Toc181301442)

[2.3.2.2.1 Escenario de calidad 1 [22](#_Toc181301443)](#_Toc181301443)

[2.3.2.2.2 Escenario de calidad 2 [22](#_Toc181301444)](#_Toc181301444)

[2.3.2.2.3 Escenario de calidad 3 [23](#_Toc181301445)](#_Toc181301445)

[2.3.2.2.4 Escenario de calidad 4 [23](#_Toc181301446)](#_Toc181301446)

[2.3.2.2.5 Escenario de calidad 5 [23](#_Toc181301447)](#_Toc181301447)

[2.3.3 Atributo calidad 3 [24](#_Toc181301448)](#_Toc181301448)

[2.3.3.1 Característica 1 [24](#_Toc181301449)](#_Toc181301449)

[2.3.3.1.1 Escenario de calidad 1 [24](#_Toc181301450)](#_Toc181301450)

[2.3.3.1.2 Escenario de calidad 2 [24](#_Toc181301451)](#_Toc181301451)

[2.3.3.1.3 Escenario de calidad 3 [24](#_Toc181301452)](#_Toc181301452)

[2.3.3.1.4 Escenario de calidad 4 [25](#_Toc181301453)](#_Toc181301453)

[2.3.3.1.5 Escenario de calidad 5 [25](#_Toc181301454)](#_Toc181301454)

[2.3.3.1.6 Escenario de calidad 6 [25](#_Toc181301455)](#_Toc181301455)

[2.3.3.1.7 Escenario de calidad 7 [26](#_Toc181301456)](#_Toc181301456)

[2.3.3.1.8 Escenario de calidad 8 [26](#_Toc181301457)](#_Toc181301457)

[2.3.3.1.9 Escenario de calidad 9 [26](#_Toc181301458)](#_Toc181301458)

[2.3.3.1.10 Escenario de calidad 10
[26](#_Toc181301459)](#_Toc181301459)

[2.3.3.1.11 Escenario de calidad 11
[27](#_Toc181301460)](#_Toc181301460)

[2.3.3.1.12 Escenario de calidad 12
[27](#_Toc181301461)](#_Toc181301461)

[2.3.3.1.13 Escenario de calidad 13
[27](#_Toc181301462)](#_Toc181301462)

[2.3.3.1.14 Escenario de calidad 14
[27](#_Toc181301463)](#_Toc181301463)

[2.3.3.1.15 Escenario de calidad 15
[28](#_Toc181301464)](#_Toc181301464)

[2.3.3.1.16 Escenario de calidad 16
[28](#_Toc181301465)](#_Toc181301465)

[2.3.3.1.17 Escenario de calidad 17
[28](#_Toc181301466)](#_Toc181301466)

[2.3.3.1.18 Escenario de calidad 18
[29](#_Toc181301467)](#_Toc181301467)

[2.3.3.2 Característica 2 [29](#_Toc181301468)](#_Toc181301468)

[2.3.3.2.1 Escenario de calidad 1 [29](#_Toc181301469)](#_Toc181301469)

[2.3.3.2.2 Escenario de calidad 2 [29](#_Toc181301470)](#_Toc181301470)

[2.3.3.2.3 Escenario de calidad 3 [30](#_Toc181301471)](#_Toc181301471)

[2.3.3.2.4 Escenario de calidad 4 [30](#_Toc181301472)](#_Toc181301472)

[2.3.3.2.5 Escenario de calidad 5 [30](#_Toc181301473)](#_Toc181301473)

[2.3.3.2.6 Escenario de calidad 6 [30](#_Toc181301474)](#_Toc181301474)

[2.3.3.2.7 Escenario de calidad 7 [31](#_Toc181301475)](#_Toc181301475)

[2.3.3.2.8 Escenario de calidad 8 [31](#_Toc181301476)](#_Toc181301476)

[2.3.3.2.9 Escenario de calidad 9 [31](#_Toc181301477)](#_Toc181301477)

[2.3.3.2.10 Escenario de calidad 10
[31](#_Toc181301478)](#_Toc181301478)

[2.3.3.2.11 Escenario de calidad 11
[32](#_Toc181301479)](#_Toc181301479)

[2.3.3.2.12 Escenario de calidad 12
[32](#_Toc181301480)](#_Toc181301480)

[2.3.3.2.13 Escenario de calidad 13
[32](#_Toc181301481)](#_Toc181301481)

[2.3.3.2.14 Escenario de calidad 14
[33](#_Toc181301482)](#_Toc181301482)

[2.3.3.2.15 Escenario de calidad 15
[33](#_Toc181301483)](#_Toc181301483)

[2.3.3.2.16 Escenario de calidad 16
[33](#_Toc181301484)](#_Toc181301484)

[2.3.3.2.17 Escenario de calidad 17
[33](#_Toc181301485)](#_Toc181301485)

[2.3.4 Atributo calidad 4 [34](#_Toc181301486)](#_Toc181301486)

[2.3.4.1 Característica 1 [34](#_Toc181301487)](#_Toc181301487)

[2.3.4.1.1 Escenario de calidad 1 [34](#_Toc181301488)](#_Toc181301488)

[2.3.4.1.2 Escenario de calidad 2 [34](#_Toc181301489)](#_Toc181301489)

[2.3.4.1.3 Escenario de calidad 3 [35](#_Toc181301490)](#_Toc181301490)

[2.3.4.1.4 Escenario de calidad 4 [35](#_Toc181301491)](#_Toc181301491)

[2.3.4.1.5 Escenario de calidad 5 [35](#_Toc181301492)](#_Toc181301492)

[2.3.4.1.6 Escenario de calidad 6 [36](#_Toc181301493)](#_Toc181301493)

[2.3.4.1.7 Escenario de calidad 7 [36](#_Toc181301494)](#_Toc181301494)

[2.3.4.1.8 Escenario de calidad 8 [36](#_Toc181301495)](#_Toc181301495)

[2.3.4.1.9 Escenario de calidad 9 [36](#_Toc181301496)](#_Toc181301496)

[2.3.4.2 Característica 2 [37](#_Toc181301497)](#_Toc181301497)

[2.3.4.2.1 Escenario de calidad 1 [37](#_Toc181301498)](#_Toc181301498)

[2.3.4.2.2 Escenario de calidad 2 [37](#_Toc181301499)](#_Toc181301499)

[2.3.4.2.3 Escenario de calidad 3 [37](#_Toc181301500)](#_Toc181301500)

[2.3.4.2.4 Escenario de calidad 4 [38](#_Toc181301501)](#_Toc181301501)

[2.3.5 Atributo calidad 5 [38](#_Toc181301502)](#_Toc181301502)

[2.3.5.1 Característica 1 [38](#_Toc181301503)](#_Toc181301503)

[2.3.5.1.1 Escenario de calidad 1 [38](#_Toc181301504)](#_Toc181301504)

[2.3.5.1.2 Escenario de calidad 2 [39](#_Toc181301505)](#_Toc181301505)

[2.3.5.1.3 Escenario de calidad 3 [39](#_Toc181301506)](#_Toc181301506)

[2.3.5.1.4 Escenario de calidad 4 [39](#_Toc181301507)](#_Toc181301507)

[2.3.5.1.5 Escenario de calidad 5 [39](#_Toc181301508)](#_Toc181301508)

[2.3.5.1.6 Escenario de calidad 6 [40](#_Toc181301509)](#_Toc181301509)

[2.3.5.2 Característica 2 [40](#_Toc181301510)](#_Toc181301510)

[2.3.5.2.1 Escenario de calidad 1 [40](#_Toc181301511)](#_Toc181301511)

[2.3.5.2.2 Escenario de calidad 2 [41](#_Toc181301512)](#_Toc181301512)

[2.3.5.2.3 Escenario de calidad 3 [41](#_Toc181301513)](#_Toc181301513)

[2.3.5.2.4 Escenario de calidad 4 [41](#_Toc181301514)](#_Toc181301514)

[2.3.5.2.5 Escenario de calidad 5 [41](#_Toc181301515)](#_Toc181301515)

[2.4 Funcionalidades críticas
[42](#funcionalidades-críticas)](#funcionalidades-críticas)

[**3.** **Tácticas y estrategias**
[44](#tácticas-y-estrategias)](#tácticas-y-estrategias)

[**4.** **Modelo de contexto**
[70](#modelo-de-contexto)](#modelo-de-contexto)

[**5.** **Arquetipo de solución/referencia**
[74](#arquetipo-de-soluciónreferencia)](#arquetipo-de-soluciónreferencia)

[**6.** **Arquitectura de solución/referencia**
[78](#arquitectura-de-soluciónreferencia)](#arquitectura-de-soluciónreferencia)

[**7.** **Línea base arquitectónica**
[83](#línea-base-arquitectónica)](#línea-base-arquitectónica)

[7.1 Línea base arquitectónica de componentes
[83](#línea-base-arquitectónica-de-componentes)](#línea-base-arquitectónica-de-componentes)

[7.1.1 Componente 1 [83](#_Toc181301523)](#_Toc181301523)

[7.1.2 Componente 2 [84](#_Toc181301524)](#_Toc181301524)

[7.1.3 Componente 3 [84](#_Toc181301525)](#_Toc181301525)

[7.1.4 Componente 4 [84](#_Toc181301526)](#_Toc181301526)

[7.1.5 Componente 5 [85](#_Toc181301527)](#_Toc181301527)

[7.1.6 Componente 6 [85](#_Toc181301528)](#_Toc181301528)

[7.1.7 Componente 7 [85](#_Toc181301529)](#_Toc181301529)

[7.1.8 Componente 8 [86](#_Toc181301530)](#_Toc181301530)

[7.1.9 Componente 9 [86](#_Toc181301531)](#_Toc181301531)

[7.1.10 Componente 10 [86](#_Toc181301532)](#_Toc181301532)

[7.1.11 Componente 11 [87](#_Toc181301533)](#_Toc181301533)

[7.1.12 Componente 12 [87](#_Toc181301534)](#_Toc181301534)

[7.1.13 Componente 13 [87](#_Toc181301535)](#_Toc181301535)

[7.1.14 Componente 14 [88](#_Toc181301536)](#_Toc181301536)

[7.1.15 Componente 15 [88](#_Toc181301537)](#_Toc181301537)

[7.1.16 Componente 16 [88](#_Toc181301538)](#_Toc181301538)

[7.2 Estilos y patrones arquitectónicos adoptados
[89](#estilos-y-patrones-arquitectónicos-adoptados)](#estilos-y-patrones-arquitectónicos-adoptados)

[7.2.1 Estilo arquitectónico 1
[89](#estilo-arquitectónico-1)](#estilo-arquitectónico-1)

[7.2.1.1 Nombre [89](#nombre)](#nombre)

[7.2.1.2 Problema [89](#problema)](#problema)

[7.2.1.3 Solución/Motivación
[89](#soluciónmotivación)](#soluciónmotivación)

[7.2.2 Estilo arquitectónico 2
[90](#estilo-arquitectónico-2)](#estilo-arquitectónico-2)

[7.2.2.1 Nombre [90](#nombre-1)](#nombre-1)

[7.2.2.2 Problema [90](#problema-1)](#problema-1)

[7.2.2.3 Solución/Motivación
[90](#soluciónmotivación-1)](#soluciónmotivación-1)

[7.2.3 Patrón arquitectónico 1
[90](#patrón-arquitectónico-1)](#patrón-arquitectónico-1)

[7.2.3.1 Nombre [90](#nombre-2)](#nombre-2)

[7.2.3.2 Problema [90](#problema-2)](#problema-2)

[7.2.3.3 Solución/Motivación
[91](#soluciónmotivación-2)](#soluciónmotivación-2)

[7.2.4 Patrón arquitectónico 2
[91](#patrón-arquitectónico-2)](#patrón-arquitectónico-2)

[7.2.4.1 Nombre [91](#nombre-3)](#nombre-3)

[7.2.4.2 Problema [91](#problema-3)](#problema-3)

[7.2.4.3 Solución/Motivación
[91](#soluciónmotivación-3)](#soluciónmotivación-3)

[7.2.5 Patrón arquitectónico 3
[91](#patrón-arquitectónico-3)](#patrón-arquitectónico-3)

[7.2.5.1 Nombre [91](#nombre-4)](#nombre-4)

[7.2.5.2 Problema [92](#problema-4)](#problema-4)

[7.2.5.3 Solución/Motivación
[92](#soluciónmotivación-4)](#soluciónmotivación-4)

[**8.** **Justificación alternativa de solución**
[92](#justificación-alternativa-de-solución)](#justificación-alternativa-de-solución)

[8.1 Justificación [92](#justificación)](#justificación)

[8.2 Ventajas [93](#ventajas)](#ventajas)

[8.3 Desventajas [94](#desventajas)](#desventajas)

[9. Vistas de arquitectura del sistema
[94](#vistas-de-arquitectura-del-sistema)](#vistas-de-arquitectura-del-sistema)

[9.1 Vista Funcional/Vista de Escenarios/Vista de Casos de Uso
[95](#vista-funcionalvista-de-escenariosvista-de-casos-de-uso)](#vista-funcionalvista-de-escenariosvista-de-casos-de-uso)

[9.2 Vista Lógica [95](#vista-lógica)](#vista-lógica)

[9.3 Vista de Despliegue/Vista de Desarrollo/Vista de Implementación
[95](#vista-de-desplieguevista-de-desarrollovista-de-implementación)](#vista-de-desplieguevista-de-desarrollovista-de-implementación)

[9.3.1 Diagrama de componentes
[96](#diagrama-de-componentes)](#diagrama-de-componentes)

[9.3.1.1 Componente zbank-perfiles-ms
[96](#_Toc181301569)](#_Toc181301569)

[9.3.1.1.1 Diagrama [97](#_Toc181301570)](#_Toc181301570)

[9.3.1.1.2 Documentación [97](#_Toc181301571)](#_Toc181301571)

[9.3.1.2 Componente zbank-divisas-ms
[99](#_Toc181301572)](#_Toc181301572)

[9.3.1.2.1 Diagrama [99](#_Toc181301573)](#_Toc181301573)

[9.3.1.2.2 Documentación [100](#_Toc181301574)](#_Toc181301574)

[9.3.1.3 Componente zbank-categoría-ms
[101](#_Toc181301575)](#_Toc181301575)

[9.3.1.3.1 Diagrama [102](#_Toc181301576)](#_Toc181301576)

[9.3.1.3.2 Documentación [102](#_Toc181301577)](#_Toc181301577)

[9.3.1.4 Componente zbank-registrosfinancieros-ms
[104](#_Toc181301578)](#_Toc181301578)

[9.3.1.4.1 Diagrama [104](#_Toc181301579)](#_Toc181301579)

[9.3.1.4.2 Documentación [104](#_Toc181301580)](#_Toc181301580)

[9.3.1.5 Componente zbank-metas-ms
[106](#_Toc181301581)](#_Toc181301581)

[9.3.1.5.1 Diagrama [107](#_Toc181301582)](#_Toc181301582)

[9.3.1.5.2 Documentación [107](#_Toc181301583)](#_Toc181301583)

[9.3.1.6 Componente zbank-notificaciones-ms
[108](#_Toc181301584)](#_Toc181301584)

[9.3.1.6.1 Diagrama [109](#_Toc181301585)](#_Toc181301585)

[9.3.1.6.2 Documentación [109](#_Toc181301586)](#_Toc181301586)

[9.3.1.7 Componente zbank-logros-ms
[110](#_Toc181301587)](#_Toc181301587)

[9.3.1.7.1 Diagrama [110](#_Toc181301588)](#_Toc181301588)

[9.3.1.7.2 Documentación [111](#_Toc181301589)](#_Toc181301589)

[9.3.2 Diagrama de paquetes
[112](#diagrama-de-paquetes)](#diagrama-de-paquetes)

[9.3.2.1 Componente zbank-\<\<component\>\>-ms
[112](#componente-vapomanager-component-ms)](#componente-vapomanager-component-ms)

[9.3.2.1.1 Diagrama [113](#diagrama)](#diagrama)

[9.3.2.1.2 Documentación [113](#_Toc181301593)](#_Toc181301593)

[9.4 Vista de Procesos [128](#_Toc181301594)](#_Toc181301594)

[9.4.1 Diagrama de secuencia [128](#_Toc181301595)](#_Toc181301595)

[9.4.1.1 Componente Without Return
[128](#_Toc181301596)](#_Toc181301596)

[9.4.1.1.1 Diagrama [129](#_Toc181301597)](#_Toc181301597)

[9.4.1.1.2 Documentación [129](#_Toc181301598)](#_Toc181301598)

[9.4.1.2 Componente With Return [133](#_Toc181301599)](#_Toc181301599)

[9.4.1.2.1 Diagrama [134](#_Toc181301600)](#_Toc181301600)

[9.4.1.2.2 Documentación [134](#_Toc181301601)](#_Toc181301601)

[9.5 Vista Física/Vista de Implantación
[139](#_Toc181301602)](#_Toc181301602)

[9.5.1 Diagrama de despliegue [139](#_Toc181301603)](#_Toc181301603)

[9.5.1.1 Diagrama [139](#_Toc181301604)](#_Toc181301604)

[9.5.1.2 Documentación [140](#_Toc181301605)](#_Toc181301605)

# **Propósito del proyecto**

VapoManager es una aplicación web para la microempresa distribuidora de
vaporizadores que centraliza ventas/pedidos, inventario, clientes y
reportes. Su objetivo es reducir trabajo manual y errores, ofrecer
alertas y métricas clave (quiebres de stock, márgenes, rotación) y
brindar una experiencia simple para asesores, bodega y administrador. El
sistema prioriza seguridad y confiabilidad (roles y permisos,
trazabilidad, consistencia de datos, respaldos) usando herramientas
gratuitas/OSS acordes al contexto académico y de bajo presupuesto.

# **Motivadores de la arquitectura**

La arquitectura de VapoManager prioriza, ante todo, la confiabilidad y
seguridad de la información: ventas, inventario y reportes deben cuadrar
siempre, con trazabilidad y respaldos verificados, control de acceso por
roles y gestión de sesión sólida. En segundo lugar, busca buen
rendimiento percibido y disponibilidad operativa, con flujos ágiles para
registrar pedidos y consultar datos, reportes asíncronos para no
bloquear la operación y continuidad tras reconexiones. También pone
énfasis en la usabilidad por roles (asesores, bodega, administrador),
con mensajes claros y navegación guiada, y en la simplicidad de costos y
mantenimiento, privilegiando herramientas gratuitas/OSS, módulos
separados y APIs claras para facilitar la evolución y el soporte.
Finalmente, incorpora observabilidad mínima (logs y métricas básicas)
para detectar incidentes y latencias, favoreciendo decisiones informadas
y correcciones rápidas.

## Restricciones técnicas

Las restricciones técnicas son condiciones que deben cumplirse durante
el desarrollo y que afectan el diseño e implementación del sistema.

**Tipo: Diseño**\
• **Se debe propender por la aplicación de prácticas basadas en Clean
Architecture.**\
Beneficia al cliente porque separa el núcleo del negocio (ventas,
pedidos, inventario) de la UI y la persistencia, facilitando cambios sin
reescribir todo y reduciendo retrabajo y costos de evolución.

**Tipo: Implementación**\
• **Se debe propender por la aplicación de prácticas relacionadas con
Clean Code.**\
Menos defectos y menor tiempo de soporte: código legible acelera el
onboarding y baja el costo de mantenimiento del sistema.

**Tipo: Diseño**\
• **Se debe propender por la aplicación de patrones de diseño que
promuevan bajo acoplamiento y alta cohesión.**\
Permite que los cambios (por ejemplo, en precios o reservas) afecten
módulos puntuales, haciendo el sistema más extensible y estable para el
negocio.

**Tipo: Implementación**\
• **Se debe propender por la adopción de prácticas de DevOps con
integración continua y entrega continua simple.**\
Entregas pequeñas detectan fallos temprano y permiten mostrar valor en
cada iteración, con despliegues más seguros y rápidos.

**Tipo: Metodológico**\
• **Se debe propender por la adopción de metodologías ágiles ligeras
(Scrum + prácticas XP seleccionadas).**\
Iteraciones cortas con feedback del cliente priorizan valor real (MVP →
mejoras), ajustando alcance según necesidades del negocio sin
burocracia.

**Tipo: Implementación/Operación**\
• **Se debe propender por aplicar los 12 factores de aplicación de forma
selectiva** (configuración por entorno, dependencias declaradas, logs
centralizables).\
Facilita mover el sistema entre desarrollo/pruebas/producción sin
sorpresas y mejora la confiabilidad operativa con bajo costo para el
proyecto.

**Tipo: Diseño**\
• **Se debe propender por la adopción de bloques de construcción
reutilizables** (componentes de UI y módulos de dominio).\
Acelera el desarrollo y mantiene consistencia: reutilizar tablas,
formularios y módulos de catálogo/ventas reduce tiempos y errores.

**Tipo: Metodológico**\
• **Se debe propender por documentación mínima y viva** (README
ejecutable, decisiones de arquitectura breves y especificación de API).\
Garantiza continuidad del proyecto y soporte: cualquier integrante
entiende cómo ejecutar, desplegar y usar la API, reduciendo dependencia
de personas.

## Restricciones de negocio

Las restricciones de negocio son condiciones que debemos cumplir para
alinear el desarrollo con las metas operativas y comerciales
de **VapoManager**.

**Tipo: Humano**\
• **Debe existir Product Owner (PO) titular y suplente con poder de
decisión y SLA de respuesta ≤ 48 h para definiciones clave.**\
Sin decisiones a tiempo, el proyecto se frena; un PO disponible evita
reprocesos y bloqueos.

• **Participación activa de expertos de negocio (ventas, compras,
inventario, finanzas) en refinamiento y UAT de historias críticas.**\
El negocio valida temprano, detecta fallas antes de salir a producción y
asegura que el alcance refleje la realidad operativa.

• **Disponibilidad del PO en sesiones fijas e inamovibles; si no puede
asistir, delega a alguien con decisión informada.**\
Sin PO presente, las definiciones se dilatan y se multiplican los
retrabajos.

• **Capacitación por rol (asesores, bodega, administrador) y manual
corto de operación.**\
Reduce errores y dependencia del equipo técnico; mejora adopción y
soporte.

• **Las decisiones de producto deben estar guiadas por métricas (margen,
costos, ventas).**\
Evita reportes contradictorios y malas decisiones; orienta el backlog a
impacto real.

• **Equipo de desarrollo pequeño (3 devs): se prioriza alcance crítico y
se limita el trabajo en paralelo (WIP).**\
Capacidad limitada implica foco para mantener calidad y tiempos.

• **Seguridad y cumplimiento: el equipo define políticas mínimas
aplicables desde el inicio (OWASP básico, contraseñas, datos
personales).**\
Previene riesgos y auditorías fallidas; protege la confianza del
cliente.

• **Asignar dueños de datos maestros (catálogo, listas de precio,
impuestos) responsables de su calidad.**\
Catálogos sanos evitan errores en ventas y costos; habilitan reportes
confiables.

**Tipo: Proceso**\
• **Reservar stock al registrar pedido con una ventana de tiempo; si no
se paga, el sistema cancela y libera.**\
Evita inventario atrapado y sobreventa.

• **Política de devoluciones clara (≤ 15 días; estado del producto;
motivo y documento soporte).**\
Controla costos y garantiza transparencia con el cliente.

• **Bitácora obligatoria de operaciones sensibles (precios, costos,
inventario, pedidos).**\
Trazabilidad y seguridad: quién hizo qué y cuándo, con exportación para
auditoría.

• **Precio mínimo y descuentos: vender bajo el costo solo con
autorización expresa del Administrador.**\
Protege margen y sostenibilidad del negocio.

• **Frente a defectos en procesos, trabajar de forma incremental con
evaluación frecuente del cliente.**\
Reduce reprocesos y alinea expectativas; mejora el time-to-value.

• **Cierre de día con conciliación por rol; definir los SLOs de soporte
funcional e incidentes.**\
Asegura operación estable y respuesta oportuna ante fallas.

**Tipo: Presupuesto**\
• **Tope de costo operativo (p. ej., hasta 30 M COP/año) sumando
servicios cloud, implementaciones y mantenimiento.**\
Evita sobrecostos; prioriza lo esencial y garantiza viabilidad.

• **El cliente destina recursos y horas; la incertidumbre de definición
no puede poner en riesgo avances.**\
Disciplina en alcance y decisiones; evita retrasos por falta de insumos
del negocio.

**Tipo: Legal / Cumplimiento**\
• **Cumplimiento de privacidad (habeas data) y protección de datos
personales.**\
Los datos de usuarios deben manejarse con protocolos estrictos de
seguridad y consentimiento.

• **Cumplimiento normativo en comunicaciones y publicidad.**\
Las campañas deben ajustarse a la normativa para evitar sanciones por
mensajes engañosos.

• **Auditorías periódicas de seguridad y cumplimiento por terceros
acreditados.**\
Detectan y corrigen vulnerabilidades e incumplimientos, manteniendo la
operación conforme a la ley.

## Atributos de calidad

Para VapoManager, priorizamos atributos que aseguran una operación
confiable y simple para ventas, inventario y reportes, alineados con
nuestro contexto académico y de bajo presupuesto. Estos atributos
orientan decisiones de diseño, pruebas y priorización.

Atributos seleccionados

Seguridad. Control de acceso por roles, gestión de sesión y protección
de datos en tránsito/en reposo. Indicadores: incidentes de seguridad =
0, caducidad de sesión, cobertura de auditoría.

Confiabilidad. Datos siempre consistentes entre
ventas--inventario--reportes, trazabilidad de quién/qué/cuándo y
respaldos verificados. Indicadores: diferencias de cuadres = 0,
restauraciones de prueba exitosas.

Disponibilidad. Servicio estable en horario de atención y recuperación
rápida ante fallos. Indicadores: SLO de disponibilidad, MTTR y
continuidad tras reconexión.

Capacidad para ser mantenido. Código claro y modular (Clean
Architecture/Clean Code) para cambios rápidos sin romper lo existente.
Indicadores: tiempo medio de cambio (lead time), cobertura/linters,
defectos pos-release.

Experiencia de usuario / Usabilidad. Flujos guiados por tarea, mensajes
claros y accesibilidad básica para asesores, bodega y administrador.
Indicadores: tiempo de completar tarea, errores por formulario,
satisfacción (CSAT).

Escalabilidad. Soportar crecimiento moderado de datos y usuarios típicos
del negocio sin replantear la arquitectura. Indicadores: uso de
CPU/memoria bajo carga típica, degradación \< X% al duplicar catálogo.

Rendimiento. Respuestas ágiles en búsquedas y registro de pedidos;
reportes en segundo plano. Indicadores: p95 de consultas, latencia de
registro, tiempos de generación de reportes (asíncronos).

## Escenarios de Calidad

![](media/image1.emf){width="6.652475940507436in"
height="4.642732939632546in"}

![](media/image2.emf){width="6.649463035870516in"
height="3.38492125984252in"}

## Funcionalidades críticas

> ![](media/image3.emf){width="6.198537839020123in"
> height="4.018740157480315in"}

# **Tácticas y estrategias** 

![](media/image4.emf){width="7.199059492563429in"
height="4.511833989501312in"}

# **Modelo de contexto**

![](media/image5.png){width="4.228485345581802in"
height="3.395138888888889in"}

Base de datos

Motivación: Almacenar y gestionar toda la información del negocio, como
datos de clientes, productos, pedidos, inventario y transacciones.

Uso: Proporcionar un almacenamiento estructurado y confiable que permita
registrar y consultar la información de manera rápida y segura.

Justificación: Es esencial para garantizar la integridad y persistencia
de los datos operativos del sistema, evitando pérdidas de información.

Proveedor de identidades

Motivación: Administrar la autenticación y autorización de los usuarios
del sistema, como vendedores y administradores.

Uso: Validar credenciales y gestionar roles para controlar el acceso a
las diferentes funcionalidades.

Justificación: Asegura la protección de la información sensible y
permite una gestión segura de los usuarios.

API Gateway

Motivación: Centralizar y gestionar las solicitudes que llegan a la
aplicación desde los distintos dispositivos.

Uso: Canalizar las peticiones hacia los microservicios correspondientes,
aplicar autenticación y balancear el tráfico.

Justificación: Facilita la comunicación interna del sistema y mejora la
seguridad y escalabilidad de la aplicación.

Componente de logging

Motivación: Registrar los eventos, errores y acciones relevantes del
sistema.

Uso: Permitir la trazabilidad de las operaciones y detectar posibles
fallos o comportamientos anómalos.

Justificación: Facilita el monitoreo y mantenimiento del sistema,
mejorando la confiabilidad.

Message Broker

Motivación: Coordinar la comunicación entre los distintos servicios o
módulos del sistema de forma desacoplada.

Uso: Transmitir mensajes entre procesos como creación de pedidos,
actualización de inventario o notificaciones.

Justificación: Incrementa la robustez y escalabilidad del sistema al
permitir que los componentes trabajen de forma independiente.

WAF (Web Application Firewall)

Motivación: Proteger la aplicación de posibles ataques y
vulnerabilidades web.

Uso: Analizar y filtrar el tráfico entrante, bloqueando solicitudes
maliciosas o sospechosas.

Justificación: Refuerza la seguridad del sistema y protege la
información del negocio y de los clientes.

Service Mesh

Motivación: Gestionar la comunicación segura entre los distintos
microservicios.

Uso: Implementar balanceo de carga, autenticación de servicios y cifrado
en la comunicación interna.

Justificación: Mejora la confiabilidad, seguridad y control de la
infraestructura.

Componente de notificaciones

Motivación: Mantener informados a los usuarios sobre eventos
importantes, como confirmaciones de pedidos o cambios en el estado del
inventario.

Uso: Enviar alertas y mensajes automáticos a través de correo
electrónico o notificaciones del sistema.

Justificación: Mejora la experiencia del usuario y la eficiencia de la
comunicación interna.

Observabilidad

Motivación: Ofrecer visibilidad sobre el rendimiento y estado del
sistema.

Uso: Recopilar métricas, registros y trazas para detectar fallos o
cuellos de botella.

Justificación: Permite la identificación temprana de problemas y
optimiza el rendimiento del sistema.

Baúl de llaves

Motivación: Administrar y proteger las claves, contraseñas y
credenciales utilizadas por los servicios.

Uso: Almacenar de forma segura secretos y datos confidenciales
necesarios para la operación.

Justificación: Aumenta la seguridad al evitar el acceso no autorizado a
información sensible.

Catálogo de parámetros

Motivación: Centralizar la configuración general del sistema.

Uso: Almacenar parámetros de negocio, como límites de descuentos o
tiempos de entrega, sin modificar el código.

Justificación: Permite ajustes dinámicos y reduce errores de
configuración manual.

Catálogo de mensajes

Motivación: Gestionar los mensajes informativos y de error del sistema.

Uso: Centralizar los textos utilizados en la aplicación para asegurar
consistencia y facilitar su modificación.

Justificación: Mejora la claridad de la interfaz y facilita la
traducción o adaptación del sistema.

Sistema de autenticación

Motivación: Validar la identidad de los usuarios que ingresan al
sistema.

Uso: Implementar mecanismos de inicio de sesión y autenticación
multifactor para mayor seguridad.

Justificación: Garantiza que solo usuarios autorizados accedan a la
información y funcionalidades del negocio.

CDN (Content Delivery Network)

Motivación: Acelerar la entrega del contenido web del sistema.

Uso: Distribuir imágenes, scripts y otros recursos estáticos desde
servidores cercanos al usuario.

Justificación: Mejora el rendimiento y la experiencia de uso,
especialmente en dispositivos móviles.

Blob Storage

Motivación: Almacenar archivos e imágenes relacionadas con los productos
o comprobantes de transacciones.

Uso: Guardar archivos de gran tamaño de forma segura y accesible.

Justificación: Proporciona un almacenamiento eficiente y escalable para
contenido multimedia y documentos del sistema.

# **Arquetipo de solución/referencia** 

![](media/image6.png){width="6.1375in" height="1.820138888888889in"}

> Base de datos.
>
> Motivación: Almacenar y gestionar toda la información del negocio,
> incluyendo productos, inventario, clientes, ventas, pedidos y
> proveedores.
>
> Uso: Proveer un almacenamiento estructurado y seguro que permita
> registrar, consultar, actualizar o eliminar datos de forma eficiente.
>
> Justificación: Es esencial para mantener la integridad y
> disponibilidad de la información comercial, garantizando que los
> procesos de gestión y seguimiento de pedidos sean precisos y
> confiables.
>
> API Gateway.
>
> Motivación: Centralizar las solicitudes que llegan al sistema desde el
> frontend u otros servicios.
>
> Uso: Encargarse del enrutamiento hacia los microservicios correctos,
> manejar autenticación, control de acceso, y balanceo de carga.
>
> Justificación: Simplifica la arquitectura, mejora la seguridad y
> permite una comunicación eficiente entre los distintos componentes del
> sistema.
>
> Sistema de autenticación.
>
> Motivación: Garantizar que solo los usuarios autorizados accedan a la
> plataforma y sus funcionalidades.
>
> Uso: Validar credenciales de administradores y empleados, gestionar
> sesiones e implementar roles con diferentes niveles de acceso.
>
> Justificación: Protege la información sensible del negocio y de los
> clientes, evitando accesos no autorizados y manteniendo la seguridad
> de los datos.
>
> Frontend VapoManager.
>
> Motivación: Ofrecer una interfaz de usuario amigable que permita
> realizar de manera sencilla tareas como registrar ventas, consultar
> inventario o generar reportes.
>
> Uso: Desarrollar vistas interactivas y visualmente atractivas para
> facilitar la interacción del usuario con el sistema.
>
> Justificación: Una buena interfaz mejora la experiencia del usuario,
> agiliza las operaciones diarias y facilita la adopción del sistema por
> parte del personal.
>
> Cache.
>
> Motivación: Mejorar el rendimiento del sistema reduciendo el tiempo de
> acceso a la información más consultada.
>
> Uso: Almacenar temporalmente datos como productos, precios o
> configuraciones para acelerar las respuestas del sistema.
>
> Justificación: Disminuye la carga en la base de datos y optimiza la
> experiencia del usuario con respuestas más rápidas y fluidas.
>
> Componente de notificaciones.
>
> Motivación: Mantener informados a los administradores y clientes sobre
> eventos importantes, como nuevos pedidos, confirmaciones o
> actualizaciones de estado.
>
> Uso: Enviar mensajes automáticos a través de correo electrónico o
> notificaciones dentro del sistema.
>
> Justificación: Mejora la comunicación y la transparencia del negocio,
> asegurando que los usuarios estén siempre al tanto de los cambios
> relevantes.
>
> Catálogo de productos.
>
> Motivación: Organizar la información de los productos de manera
> estructurada y accesible.
>
> Uso: Registrar detalles como nombre, descripción, precios, stock y
> proveedor de cada vaporizador o accesorio.
>
> Justificación: Facilita la gestión de inventario y permite
> actualizaciones rápidas en la oferta de productos del negocio.
>
> Catálogo de parámetros.
>
> Motivación: Permitir la configuración dinámica de valores y reglas
> dentro del sistema.
>
> Uso: Definir parámetros como impuestos, descuentos, o límites de stock
> sin necesidad de modificar el código.
>
> Justificación: Incrementa la flexibilidad del sistema y permite
> adaptar las operaciones según las necesidades del negocio.
>
> Componente de logging.
>
> Motivación: Registrar todas las operaciones realizadas dentro del
> sistema para fines de auditoría y diagnóstico.
>
> Uso: Guardar registros de eventos como inicios de sesión,
> modificaciones en el inventario o errores del sistema.
>
> Justificación: Facilita el monitoreo del funcionamiento general, la
> detección de fallas y la trazabilidad de las acciones de los usuarios.
>
> Message Broker.
>
> Motivación: Mejorar la comunicación entre los diferentes
> microservicios del sistema de manera asíncrona.
>
> Uso: Gestionar el envío y recepción de mensajes entre módulos, como el
> de ventas, inventario y notificaciones.
>
> Justificación: Desacopla los servicios, aumentando la escalabilidad y
> la estabilidad del sistema al permitir que cada componente funcione
> independientemente.
>
> Blob Storage.
>
> Motivación: Almacenar archivos e imágenes relacionados con productos o
> comprobantes de venta.
>
> Uso: Guardar y recuperar de forma eficiente imágenes de productos,
> facturas o reportes en un almacenamiento escalable.
>
> Justificación: Centraliza y organiza los archivos del sistema,
> facilitando su acceso y mejorando la presentación visual en el
> frontend.
>
> Baúl de llaves.
>
> Motivación: Proteger las credenciales, claves de API y datos sensibles
> utilizados por el sistema.
>
> Uso: Proveer un entorno seguro para el almacenamiento y la
> recuperación de secretos utilizados en la aplicación.
>
> Justificación: Garantiza la confidencialidad y la integridad de la
> información sensible, reforzando la seguridad general de la
> plataforma.
>
> Microservicios.
>
> Motivación: Dividir las funcionalidades del sistema en módulos
> independientes para mejorar su escalabilidad y mantenimiento.
>
> Uso: Separar componentes como ventas, inventario, usuarios y
> notificaciones para que funcionen de manera autónoma.
>
> Justificación: Aumenta la flexibilidad del desarrollo y facilita la
> actualización o despliegue individual de cada módulo sin afectar el
> resto del sistema.
>
> Observability.
>
> Motivación: Supervisar el estado y rendimiento del sistema en tiempo
> real.
>
> Uso: Implementar métricas y paneles de monitoreo para detectar fallos
> o comportamientos anómalos.
>
> Justificación: Permite actuar proactivamente ante problemas,
> asegurando la disponibilidad y estabilidad de la aplicación.
>
> Service Mesh.
>
> Motivación: Controlar y optimizar la comunicación entre los
> microservicios de VapoManager.
>
> Uso: Gestionar balanceo de carga, enrutamiento y políticas de
> seguridad en las interacciones entre servicios.
>
> Justificación: Mejora la eficiencia y seguridad de la arquitectura,
> garantizando una comunicación confiable entre los distintos módulos.
>
> WAF (Web Application Firewall).
>
> Motivación: Proteger la aplicación de posibles ataques como
> inyecciones SQL, XSS o tráfico malicioso.
>
> Uso: Filtrar y analizar las solicitudes HTTP, bloqueando aquellas que
> representen una amenaza.
>
> Justificación: Refuerza la seguridad general del sistema, protegiendo
> tanto los datos del negocio como la infraestructura.
>
> CDN (Content Delivery Network).
>
> Motivación: Mejorar la velocidad de carga del frontend y los recursos
> estáticos.
>
> Uso: Distribuir imágenes, estilos y scripts en servidores cercanos al
> usuario final.
>
> Justificación: Optimiza el rendimiento del sistema, ofreciendo una
> experiencia más rápida y fluida para los usuarios.

# **Arquitectura de solución/referencia**

![](media/image7.png){width="6.638554243219597in"
height="2.0265693350831144in"}

WAF (Cloudflare WAF).

Motivación: Se eligió Cloudflare WAF por su capacidad para proteger la
aplicación contra ataques comunes, como inyecciones SQL o XSS, sin
afectar el rendimiento.

Uso: Se utiliza para inspeccionar y filtrar el tráfico HTTP antes de que
llegue a la aplicación, bloqueando peticiones maliciosas.

Justificación: Aporta una capa de seguridad esencial para garantizar la
integridad del sistema y proteger los datos sensibles de los usuarios.

CDN (AWS CloudFront).

Motivación: AWS CloudFront fue seleccionado por su red global de
distribución de contenido que mejora la velocidad de carga del frontend.

Uso: Distribuye archivos estáticos del frontend, reduciendo la latencia
y mejorando la experiencia de usuario.

Justificación: Aumenta la disponibilidad y el rendimiento del sistema,
asegurando tiempos de respuesta bajos incluso ante alta demanda.

API Gateway (Kong Gateway).

Motivación: Kong se eligió por su eficiencia en la gestión de
peticiones, autenticación y balanceo de carga hacia los microservicios.

Uso: Redirige las solicitudes de los clientes al microservicio
correspondiente, aplicando políticas de seguridad y control.

Justificación: Centraliza la gestión de APIs y facilita la
escalabilidad, manteniendo la seguridad y consistencia del tráfico
interno.

Sistema de autenticación (Keycloak).

Motivación: Se seleccionó Keycloak por su soporte para autenticación,
autorización y manejo de roles mediante protocolos estándar (OAuth2,
OpenID).

Uso: Gestiona el inicio de sesión de usuarios y controla los accesos
según roles y permisos definidos.

Justificación: Garantiza un control seguro de identidades y reduce la
complejidad de la gestión de usuarios en los microservicios.

Microservicios (Spring Boot).

Motivación: Spring Boot se eligió por su rapidez de desarrollo y
compatibilidad con arquitecturas basadas en microservicios.

Uso: Cada módulo de VapoManager (ventas, pedidos, catálogo,
notificaciones, usuarios) se implementa como un microservicio
independiente.

Justificación: Aumenta la escalabilidad y facilita el mantenimiento,
permitiendo que cada componente evolucione sin afectar al resto.

Base de datos principal (PostgreSQL).

Motivación: PostgreSQL fue seleccionado por su robustez, rendimiento y
soporte para datos relacionales complejos.

Uso: Almacena información estructurada como usuarios, productos, pedidos
y transacciones.

Justificación: Proporciona integridad y consistencia de datos,
fundamentales para la gestión confiable del negocio.

Base de datos de soporte (Redis).

Motivación: Redis se escogió para mejorar el rendimiento del sistema
mediante almacenamiento temporal de datos.

Uso: Guarda en caché resultados de consultas frecuentes y sesiones
activas.

Justificación: Reduce la carga en la base de datos principal y mejora
significativamente los tiempos de respuesta del sistema.

Componente de notificaciones (SendGrid).

Motivación: Se eligió SendGrid por su fiabilidad y capacidad de envío
masivo de correos electrónicos.

Uso: Gestiona el envío de notificaciones automáticas como confirmaciones
de registro o actualización de pedidos.

Justificación: Mejora la comunicación con los usuarios y automatiza
procesos clave del negocio.

Almacenamiento de archivos (AWS S3).

Motivación: AWS S3 se seleccionó por su alta durabilidad y escalabilidad
para manejar archivos no estructurados.

Uso: Almacena imágenes de productos, comprobantes y otros archivos de
soporte.

Justificación: Permite un almacenamiento seguro, accesible y de bajo
costo, asegurando disponibilidad constante.

Monitorización y métricas (Prometheus y Grafana).

Motivación: Se optó por Prometheus y Grafana por su integración sencilla
y su potencia en la observación del sistema.

Uso: Prometheus recolecta métricas de los servicios, y Grafana las
presenta mediante paneles visuales en tiempo real.

Justificación: Permite una observación continua del rendimiento y
facilita la detección temprana de fallos.

Gestión de secretos (HashiCorp Vault).

Motivación: HashiCorp Vault fue seleccionado por su robustez en la
gestión de credenciales y secretos de forma cifrada.

Uso: Almacena claves API, contraseñas y tokens de acceso utilizados por
los microservicios.

Justificación: Garantiza la seguridad de la información sensible,
reduciendo riesgos de exposición o mal uso.

Message Broker (RabbitMQ).

Motivación: RabbitMQ fue escogido para permitir la comunicación
asíncrona entre microservicios.

Uso: Gestiona colas de mensajes para operaciones como envío de correos,
registro de pedidos y notificaciones.

Justificación: Aumenta la resiliencia y desacopla los componentes,
evitando cuellos de botella en el sistema.

# **Línea base arquitectónica**

Es un conjunto de documentos y especificaciones que describen como debe
ser la estructura y el diseño de un sistema o software. Esta línea base
sirve como referencia para asegurarse de que todo los cambios y
desarrollos futuros se realicen de manera coherente y alineada con los
objeticos iniciales del proyecto.

## Línea base arquitectónica de componentes

A continuación, se van a presentar cada uno de los componentes empleados
en la construcción de Zbank, detallando la motivación y descripción del
componente. Este análisis permitirá comprender mejor las decisiones
arquitectónicas y tecnologías que sustentan el desarrollo de Zbank,
asegurando que cada componente cumpla con los objetivos establecidos y
contribuya al funcionamiento eficiente y seguro del sistema.

7.1.1 Componente 1

Nombre: VapoManager

Tipo de componente: Desarrollo propio

Descripción: Componente que contiene toda la lógica de negocio necesaria
para la gestión integral del sistema VapoManager.

Justificación: Este componente es esencial, ya que incluye toda la
funcionalidad principal del sistema: gestión de productos, control de
inventario, registro de ventas y pedidos, manejo de usuarios, generación
de reportes y análisis de rendimiento del negocio.

Categoría: Core

7.1.2 Componente 2

Nombre: Base de datos principal (PostgreSQL)

Tipo de componente: Componente adoptado

Descripción: Componente encargado de almacenar de forma estructurada
toda la información del sistema, incluyendo usuarios, productos,
pedidos, clientes y registros de ventas.

Justificación: Garantiza la integridad, consistencia y disponibilidad de
los datos críticos del negocio, permitiendo operaciones seguras y
consultas eficientes. Además, cumple con los estándares de seguridad y
rendimiento exigidos por el sistema.

Categoría: Genérico

7.1.3 Componente 3

Nombre: Sistema de autenticación (Keycloak)

Tipo de componente: Componente adoptado

Descripción: Componente que gestiona la autenticación y autorización de
los usuarios dentro de VapoManager.

Justificación: Permite controlar los accesos y roles de usuarios,
garantizando un inicio de sesión seguro y una correcta protección de la
información sensible del sistema.

Categoría: Soporte

7.1.4 Componente 4

Nombre: API Gateway (Kong Gateway)

Tipo de componente: Componente adoptado

Descripción: Componente que centraliza y gestiona todas las peticiones
hacia los microservicios del sistema VapoManager.

Justificación: Facilita la comunicación entre el frontend y el backend,
controlando el tráfico, autenticación y enrutamiento de las solicitudes
de manera eficiente y segura.

Categoría: Soporte

7.1.5 Componente 5

Nombre: Componentes de logging

Tipo de componente: Componente adoptado

Descripción: Componente responsable de registrar todas las actividades y
eventos relevantes del sistema.

Justificación: Es fundamental para el monitoreo y auditoría de las
operaciones, permitiendo la detección de errores, trazabilidad de
acciones de los usuarios y análisis del comportamiento del sistema.

Categoría: Soporte

7.1.6 Componente 6

Nombre: WAF (Web Application Firewall - Cloudflare)

Tipo de componente: Componente adoptado

Descripción: Componente de seguridad que protege la aplicación
VapoManager de ataques externos y vulnerabilidades comunes.

Justificación: Mitiga amenazas como inyecciones SQL, XSS o ataques DDoS,
garantizando la integridad de la información de los usuarios y la
disponibilidad del sistema.

Categoría: Genérico

7.1.7 Componente 7

Nombre: Service Mesh

Tipo de componente: Componente adoptado

Descripción: Componente que gestiona la comunicación interna entre los
microservicios de VapoManager, proporcionando seguridad, balanceo y
observabilidad.

Justificación: Asegura que las interacciones entre los servicios (como
pedidos, inventario y notificaciones) sean confiables, seguras y
monitoreadas.

Categoría: Soporte

7.1.8 Componente 8

Nombre: Baúl de llaves (HashiCorp Vault)

Tipo de componente: Componente adoptado

Descripción: Componente que gestiona de manera segura las claves,
contraseñas y secretos del sistema.

Justificación: Protege información sensible como tokens de acceso,
credenciales de base de datos o llaves API, asegurando un manejo cifrado
y controlado.

Categoría: Genérico

7.1.9 Componente 9

Nombre: Catálogo de parámetros

Tipo de componente: Componente adoptado

Descripción: Componente que permite gestionar y modificar parámetros de
configuración del sistema sin alterar el código fuente.

Justificación: Facilita la personalización y adaptación del
comportamiento del sistema, permitiendo ajustar límites de stock,
tiempos de entrega o políticas de descuentos de manera flexible.

Categoría: Soporte

7.1.10 Componente 10

Nombre: Catálogo de mensajes

Tipo de componente: Componente adoptado

Descripción: Componente que centraliza los mensajes y notificaciones
internas del sistema.

Justificación: Permite mantener consistencia en las respuestas y alertas
que se muestran a los usuarios, mejorando la comunicación y experiencia
dentro de la aplicación.

Categoría: Soporte

7.1.11 Componente 11

Nombre: CDN (Content Delivery Network - AWS CloudFront)

Tipo de componente: Componente adoptado

Descripción: Componente encargado de optimizar la entrega de contenido
estático como imágenes, estilos y scripts del frontend.

Justificación: Reduce la latencia y mejora el tiempo de carga de la
aplicación, asegurando una experiencia fluida para los usuarios desde
diferentes ubicaciones.

Categoría: Genérico

7.1.12 Componente 12

Nombre: Almacenamiento de archivos (AWS S3)

Tipo de componente: Componente adoptado

Descripción: Componente utilizado para almacenar archivos no
estructurados como imágenes de productos, comprobantes o reportes.

Justificación: Garantiza la disponibilidad, durabilidad y acceso rápido
a los archivos cargados por los usuarios o generados por el sistema.

Categoría: Genérico

7.1.13 Componente 13

Nombre: Message Broker (RabbitMQ)

Tipo de componente: Componente adoptado

Descripción: Componente que gestiona la comunicación asíncrona entre
microservicios, asegurando el envío y recepción ordenada de mensajes.

Justificación: Desacopla los servicios y mejora la escalabilidad,
permitiendo manejar eventos como confirmaciones de pedidos, envío de
correos o actualizaciones de inventario sin afectar el rendimiento.

Categoría: Soporte

7.1.14 Componente 14

Nombre: Observabilidad (Prometheus y Grafana)

Tipo de componente: Componente adoptado

Descripción: Conjunto de herramientas que recolectan métricas y
registros del sistema, permitiendo monitorear el estado y rendimiento de
los servicios.

Justificación: Facilita la detección temprana de fallos y la toma de
decisiones informadas mediante paneles visuales en tiempo real.

Categoría: Soporte

7.1.15 Componente 15

Nombre: Componente de notificaciones (SendGrid)

Tipo de componente: Componente adoptado

Descripción: Componente encargado de enviar notificaciones por correo
electrónico a los usuarios sobre pedidos, registros o cambios en el
sistema.

Justificación: Mejora la comunicación y experiencia del cliente,
manteniéndolo informado de sus transacciones o actualizaciones
importantes.

Categoría: Genérico

## Estilos y patrones arquitectónicos adoptados

Los estilos y patrones críticos son enfoques y soluciones estructuradas
que se utilizan en el diseño y desarrollo de software para abordar
problemas comunes y mejorar la calidad del sistema. Los estilos críticos
se refieren a los enfoques arquitectónicos que establecen la estructura
general del software. Estos estilos pueden incluir arquitecturas como en
capas, microservicios u orientadas a eventos, que ayudan a organizar el
código y a definir cómo se comunican los diferentes componentes del
sistema. Al elegir un estilo adecuado, se asegura que el proyecto sea
escalable, mantenible y eficiente. Por otro lado, los patrones críticos
son soluciones probadas y reutilizables a problemas específicos que se
presentan durante el desarrollo, estos patrones ayudan a los
desarrolladores a escribir código más limpio y comprensible, evitando la
reinvención de soluciones ya existentes.

## Estilo arquitectónico 1

Estilo arquitectónico que se basa en la creación de aplicaciones como un
conjunto de pequeños servicios independientes, cada uno de los cuales
está diseñado para cumplir una funcionalidad específica.

##  Nombre

Microservicios

##  Problema

El enfoque de microservicios resuelve el problema de la complejidad en
aplicaciones monolíticas, donde todo el código y la funcionalidad están
integrados en una sola base de código. Este tipo de arquitectura es
difícil de escalar, mantener y desplegar, especialmente a medida que el
proyecto crece. Los microservicios son ideales en contextos donde se
requiere una alta disponibilidad, escalabilidad y flexibilidad,
permitiendo a diferentes equipos trabajar de manera independiente en
distintas partes de la aplicación.

##  Solución/Motivación

La solución propuesta por el enfoque de microservicios es descomponer la
aplicación en pequeños servicios independientes, cada uno enfocado en
una funcionalidad específica. Cada microservicio se puede desarrollar,
desplegar y escalar de manera independiente, lo que permite una mayor
agilidad en el desarrollo y la implementación. Además, los
microservicios pueden ser escritos en diferentes lenguajes de
programación y usar diferentes bases de datos, lo que fomenta la
diversidad tecnológica y la innovación.

## Estilo arquitectónico 2

Estilo que promueve la separación de la lógica de negocio de los
detalles de implementación. Esta arquitectura organiza el software en
capas que se comunican a través de interfaces, donde el núcleo del
sistema (la lógica de negocio) es independiente de los componentes
externos como bases de datos, interfaces de usuario y otros servicios.

##  Nombre

Arquitectura Hexagonal (Clean Architecture)

##  Problema

La arquitectura hexagonal aborda el problema de acoplar la lógica de
negocio a detalles de implementación específicos, como bases de datos,
interfaces de usuario y servicios externos. En contextos donde la
aplicación necesita adaptarse a cambios tecnológicos frecuentes o donde
se requiere integrar diferentes interfaces (como móviles y web), este
estilo arquitectónico proporciona una solución clara.

##  Solución/Motivación

La solución de la arquitectura hexagonal es organizar el sistema de
manera que la lógica de negocio esté en el centro y rodeada de
interfaces que permiten la interacción con el mundo exterior. Esto
significa que los detalles de implementación (como frameworks y bases de
datos) están aislados del núcleo del negocio, facilitando la prueba y la
modificación del sistema sin afectar su funcionalidad principal. Esta
estructura modular y flexible permite adaptarse rápidamente a nuevos
requerimientos y tecnologías.

## Patrón arquitectónico 1

Organiza una aplicación en tres componentes principales: el Modelo, que
maneja los datos y la lógica de negocio; la Vista, que presenta la
información al usuario; y el Controlador, que actúa como intermediario
que gestiona la interacción entre el modelo y la vista.

##  Nombre

Modelo-Vista-Controlador (MVC)

##  Problema

El patrón MVC resuelve el problema de la separación de responsabilidades
en aplicaciones interactivas, donde la lógica de negocio, la interfaz de
usuario y el flujo de control deben estar claramente definidos. En
contextos donde las aplicaciones requieren una interacción constante y
dinámica con los usuarios, este estilo facilita la organización del
código.

##  Solución/Motivación

La solución que ofrece el patrón MVC es dividir la aplicación en tres
componentes principales: el Modelo, que maneja la lógica de negocio y
los datos; la Vista, que se encarga de la presentación de la información
al usuario; y el Controlador, que actúa como intermediario entre el
modelo y la vista, gestionando la entrada del usuario. Esta separación
permite un desarrollo más organizado, facilita las pruebas unitarias y
permite que los desarrolladores trabajen en diferentes aspectos de la
aplicación sin interferencias, promoviendo un flujo de trabajo más
eficiente y colaborativo.

## Patrón arquitectónico 2

Diseño creacional que asegura que una clase tenga una única instancia a
lo largo de la aplicación y proporciona un punto de acceso global a esa
instancia. Este patrón es útil en situaciones donde es necesario tener
un control centralizado sobre un recurso compartido, como una
configuración global, un registro de eventos o una conexión a una base
de datos.

##  Nombre

Singleton

##  Problema

El patrón Singleton resuelve el problema de la creación de múltiples
instancias de una clase que debería tener una única instancia a lo largo
de la aplicación. Este contexto de aplicación es crítico en situaciones
donde se necesita un control centralizado sobre recursos compartidos,
como una configuración global, un registro de eventos, o una conexión a
base de datos. Sin el uso del patrón Singleton, se corre el riesgo de
tener múltiples instancias que pueden provocar inconsistencias y
comportamientos inesperados en la aplicación.

##  Solución/Motivación

La solución propuesta por el patrón Singleton es restringir la creación
de instancias de la clase a una sola instancia y proporcionar un punto
de acceso global a esa instancia. Esto se logra mediante un constructor
privado que impide la creación de instancias fuera de la clase y un
método estático que devuelve la instancia única. Esta estrategia
garantiza que todos los componentes de la aplicación que requieren
acceso a ese recurso compartido utilicen la misma instancia, lo que
mejora la gestión de recursos y la coherencia en el estado de la
aplicación. Al aplicar este patrón, se facilita la implementación de
funcionalidades que requieren un control centralizado y se minimizan los
riesgos de error asociados con el manejo de múltiples instancias.

## Patrón arquitectónico 3

Patrón que permite que un objeto (o clase) reciba sus dependencias de
fuentes externas en lugar de crearlas internamente. Esto se logra
mediante la inyección de objetos necesarios en el constructor, en
métodos o a través de propiedades

##  Nombre

Inyección de Dependencias (DI)

##  Problema

El patrón de Inyección de Dependencias resuelve el problema del
acoplamiento fuerte entre componentes en una aplicación. En contextos
donde las clases dependen de otras clases para funcionar, la creación de
instancias dentro de esas clases puede dificultar el mantenimiento, la
prueba y la evolución del sistema. Este patrón es particularmente útil
en arquitecturas complejas, donde el cambio de una dependencia puede
requerir modificaciones significativas en múltiples lugares del código.

##  Solución/Motivación

La solución propuesta por la Inyección de Dependencias es permitir que
un objeto reciba sus dependencias desde el exterior, en lugar de
crearlas internamente. Esto se logra a través de la inyección en el
constructor, en métodos o a través de propiedades. Al hacerlo, se
promueve un bajo acoplamiento y se facilita la reutilización de
componentes, ya que las clases se pueden construir de manera
independiente de sus dependencias. Este enfoque ayuda a mantener un
diseño limpio y modular, alineándose con los principios de arquitecturas
como la Clean Architecture, lo que permite una evolución más sencilla y
flexible del software a lo largo del tiempo.

# **Justificación alternativa de solución**

La justificación de una alternativa de solución es la explicación que
respalda la elección de un enfoque específico para resolver un problema.
Consiste en evaluar diversas opciones y determinar cuál es la más
adecuada según los requisitos del proyecto, las restricciones de diseño
y los objetivos estratégicos. Esta justificación asegura que la solución
no solo aborde el problema de manera efectiva, sino que también sea
sostenible a largo plazo y se alinee con los principios de diseño
deseados.

## Justificación

La alternativa de solución propuesta para Zbank, basada en una
arquitectura hexagonal (clean architecture) integrada con un sistema de
componentes externos como WAF, CDN, API Gateway, y un proveedor de
identidad, es la más adecuada para resolver las necesidades operativas,
de seguridad, y de escalabilidad del sistema, orientado a la gestión de
finanzas personales. Esta arquitectura proporciona una separación clara
de responsabilidades, donde cada capa se encuentra desacoplada,
permitiendo una flexibilidad importante para la incorporación o
modificación de componentes futuros sin afectar el núcleo de la
aplicación. Esto asegura que, a medida que el sistema crece y se adapta
a nuevas funcionalidades o requisitos de los usuarios, el mantenimiento
y la evolución del software puedan realizarse sin comprometer la
estabilidad ni el rendimiento.

Una de las principales razones para optar por esta arquitectura es que
facilita la implementación de altos niveles de seguridad y rendimiento.
La inclusión de un Web Application Firewall (WAF) y un API Gateway
permite proteger el sistema contra amenazas cibernéticas, mientras que
un sistema de autenticación robusto, respaldado por un Identity Provider
externo, fortalece la protección de los datos de los usuarios. Estos
elementos de seguridad son críticos, pues la naturaleza de la
aplicación, que maneja información sensible como datos financieros y
personales, exige los mayores estándares de protección para fomentar la
confianza del usuario en Zbank.

El uso de un Message Broker también representa una ventaja
significativa, pues permite una comunicación asíncrona y eficiente entre
los distintos componentes del sistema, manteniendo la integridad de los
datos y soportando el procesamiento de transacciones en tiempo real.

Esta solución no solo cumple con las restricciones de diseño
identificadas en cuanto a seguridad, escalabilidad y experiencia de
usuario, sino que también alinea las capacidades tecnológicas con la
visión de Zbank de ser una herramienta integral, segura, y eficiente
para la gestión financiera personal.

## Ventajas

**Escalabilidad Modular:** La arquitectura hexagonal permite agregar o
modificar módulos sin interrumpir otros componentes del sistema. Esto es
crucial para Zbank, ya que permite incorporar nuevas funcionalidades o
actualizar componentes de forma ágil, soportando el crecimiento de la
aplicación y el incremento de usuarios.

**Seguridad Integral:** La inclusión de un WAF y un sistema de
autenticación sólido con un Identity Provider externo brinda varias
capas de protección para los datos sensibles. Esto minimiza el riesgo de
ataques cibernéticos, especialmente los que afectan a aplicaciones
financieras, mejorando la confianza de los usuarios.

**Desempeño Optimizado:** Al integrar un CDN y un sistema de caché, el
frontend de Zbank se carga rápidamente en cualquier ubicación,
optimizando la experiencia de usuario incluso durante picos de tráfico.
Esto asegura que la aplicación sea rápida y ágil para todos los
usuarios, independientemente de su ubicación o conexión.

**Eficiencia en la Comunicación:** El uso de un Message Broker asegura
una comunicación asíncrona entre servicios, lo cual es fundamental para
una aplicación de finanzas donde la integridad y la velocidad de
procesamiento de transacciones en tiempo real son clave. Esto facilita
la fluidez en las operaciones sin pérdida de datos ni retrasos.

**Observabilidad y Monitoreo Proactivo:** La integración de un sistema
de observabilidad permite monitorear el estado de cada componente,
facilitando la detección y resolución temprana de problemas. Esto
resulta en menos tiempos de inactividad y asegura que el sistema esté
disponible y operativo en todo momento.

**Independencia Tecnológica:** Gracias al desacoplamiento de los
módulos, es posible elegir y actualizar cada componente (como la base de
datos o el sistema de almacenamiento) según las necesidades del negocio
o los avances tecnológicos sin comprometer el resto del sistema.

## Desventajas

**Complejidad en el Desarrollo:** La integración de múltiples
componentes y servicios (como WAF, API Gateway, Message Broker y
observabilidad) incrementa la complejidad del desarrollo inicial. Esto
puede implicar una mayor inversión de tiempo y recursos para implementar
correctamente cada parte de la solución.

**Costos de Mantenimiento:** La gestión de una infraestructura con
tantos componentes externos y módulos internos implica un esfuerzo de
mantenimiento significativo. Esto se traduce en mayores costos
operativos y en la necesidad de un equipo especializado para gestionar
la infraestructura de Zbank.

**Curva de Aprendizaje Elevada:** La adopción de una arquitectura
hexagonal y la integración de varios servicios requiere que el equipo de
desarrollo esté bien capacitado en estas tecnologías. Esto puede
ralentizar el proceso de desarrollo y requerir capacitación adicional
para asegurar una implementación efectiva.

**Dependencia de Servicios Externos:** El uso de servicios externos,
como el proveedor de identidad y el CDN, puede llevar a depender de su
disponibilidad y rendimiento. Si alguno de estos servicios falla, podría
afectar negativamente la experiencia del usuario en Zbank y comprometer
la disponibilidad de ciertos servicios.

**Posible Latencia en la Comunicación:** En una arquitectura de
microservicios, la comunicación entre servicios puede introducir
latencias adicionales. Esto podría afectar la experiencia del usuario,
especialmente en transacciones que requieren respuestas rápidas, como
las operaciones financieras en tiempo real.

**Complejidad en la Observabilidad:** Mantener el sistema de
observabilidad actualizado y optimizado es un desafío, especialmente con
múltiples servicios interactuando. Esto requiere un monitoreo continuo y
ajustes frecuentes para evitar errores en la detección de problemas o en
el análisis del rendimiento.

# Vistas de arquitectura del sistema

Las vistas de diseño del sistema permiten a los desarrolladores y
arquitectos de software entender y comunicar cómo está construido el
sistema, cómo funcionan sus componentes y cómo interactúan entre sí.

## Vista Funcional/Vista de Escenarios/Vista de Casos de Uso

La vista funcional es una representación enfocada en describir las
funciones esenciales que el sistema debe realizar, mostrando cómo se
organizan en módulos o componentes que interactúan para cumplir con los
requisitos. Su motivación principal es asegurar que tanto el equipo de
desarrollo como los stakeholders tengan una comprensión común de las
actividades clave, facilitando la planificación y minimizando los
malentendidos durante la implementación. En el diseño del sistema, esta
vista aporta una estructura clara y modular, donde cada función puede
desarrollarse, probarse y actualizarse de forma independiente. Esto no
solo permite construir un sistema escalable y adaptable a cambios
futuros, sino que también facilita el mantenimiento, asegurando que el
sistema pueda evolucionar de acuerdo con nuevas necesidades sin
comprometer su estabilidad o rendimiento.

## Vista Lógica

La vista lógica es una representación que organiza y estructura los
elementos del sistema desde una perspectiva de software, enfocándose en
los componentes y sus interacciones sin entrar en detalles físicos o de
implementación. Su motivación principal es clarificar cómo se agrupan y
relacionan los componentes en función de sus roles y responsabilidades,
facilitando una comprensión clara de la arquitectura del sistema para el
equipo de desarrollo y otros stakeholders. En el diseño del sistema,
esta vista aporta una estructura bien definida que permite una
separación clara de responsabilidades y dependencias, lo que facilita el
mantenimiento, la reutilización de componentes y la escalabilidad del
sistema, asegurando que el desarrollo y la evolución sean coherentes y
eficientes.

## Vista de Despliegue/Vista de Desarrollo/Vista de Implementación

La vista de despliegue, también llamada vista de desarrollo o de
implementación, es una representación que muestra cómo y dónde se
desplegarán los componentes del sistema en la infraestructura física,
como servidores, contenedores o máquinas virtuales. Su motivación
principal es asegurar que todos comprendan cómo el sistema se distribuye
y funciona en el entorno físico, considerando factores como rendimiento,
disponibilidad y escalabilidad. En el diseño del sistema, esta vista
aporta una comprensión clara sobre la disposición de los recursos,
permitiendo planificar un despliegue óptimo que aproveche la
infraestructura disponible, minimice tiempos de respuesta y facilite el
mantenimiento, asegurando que el sistema esté bien configurado para
cumplir con sus requisitos técnicos y operativos.

## Diagrama de componentes

Un diagrama de componentes es una representación visual en la
arquitectura de software que muestra cómo los distintos módulos o
componentes del sistema interactúan entre sí. Cada componente representa
una unidad de software independiente que cumple una función específica
dentro del sistema.

**Motivación.**

La principal motivación para usar un diagrama de componentes es
descomponer el sistema en partes manejables y autónomas. Esta
representación facilita la comprensión de la estructura interna del
sistema, lo que ayuda a los equipos a identificar cómo interactúan las
diferentes partes y cómo se pueden desarrollar, probar, mantener y
desplegar de manera independiente.

**Aportación al diseño del sistema.**

- **Claridad en la arquitectura**: Define de manera explícita qué hace
  cada componente y cómo se integra en el sistema, ayudando a visualizar
  el flujo y organización de la lógica.

- **Facilita modularidad**: Al mostrar los componentes y sus
  interacciones, permite diseñar un sistema modular, en el cual las
  partes pueden desarrollarse y desplegarse de forma independiente,
  reduciendo la complejidad general.

- **Mejor gestión de dependencias**: Al ver cómo los componentes
  dependen entre sí, es posible gestionar y reducir las dependencias,
  facilitando un diseño más limpio y minimizando el acoplamiento.

- **Facilita el mantenimiento y la escalabilidad**: Ayuda a localizar
  componentes específicos para cambios o mejoras, y permite planificar
  de forma efectiva futuras expansiones o integraciones, asegurando que
  el sistema puede crecer sin comprometer la estructura inicial.

9.3.1.1 Componente vapo-manager-ms

Descripción del componente:

Componente microservicio desarrollado que concentra la lógica de negocio
de VapoManager: gestión de productos, control de inventario, registro y
confirmación de pedidos, facturación básica, gestión de clientes y
generación de reportes operativos.

Motivación del diagrama:

El diagrama muestra los componentes tecnológicos y dependencias
necesarias para ejecutar el microservicio vapo-manager-ms, distinguiendo
componentes adoptados (tecnologías externas) y desarrollados (jar del
servicio).

9.3.1.1.2 Documentación

Componente: vapo-manager-ms

Tipo: Desarrollado

Depende de:

• Spring Boot 3.x

• Java (JRE 17/21)

• Spring Cloud (config/discovery)

• PostgreSQL

Es usado por:

• Frontend (VapoManager UI)

• API Gateway

• Otros microservicios (notificaciones, reportes)

Descripción componente: Microservicio principal que implementa los casos
de uso del dominio: creación y confirmación de pedidos, descuento de
inventario, control de reservas, conciliaciones básicas y exposición de
APIs para la interfaz de usuario y otros servicios.

Componente: Java (JRE 17/21)

Tipo: Adoptado

Depende de:

Es usado por:

• Spring Boot

• Spring Cloud

• vapo-manager-ms

• PostgreSQL

Descripción componente: Plataforma de ejecución que sirve como base para
las aplicaciones desarrolladas en Spring Boot. Proporciona el entorno
necesario para garantizar compatibilidad y rendimiento en la ejecución
del sistema.

Componente: Spring Boot 3.x

Tipo: Adoptado

Depende de:

• Java (JRE 17/21)

Es usado por:

• vapo-manager-ms

Descripción componente: Framework que acelera la construcción de
aplicaciones Java, facilita la configuración y el empaquetado en
archivos ejecutables, permitiendo exponer servicios REST de manera
rápida y ordenada.

Componente: Spring Cloud (config/discovery)

Tipo: Adoptado

Depende de:

• Spring Boot

• Java (JRE 17/21)

Es usado por:

• vapo-manager-ms

Descripción componente: Conjunto de herramientas que permite gestionar
la configuración distribuida, el descubrimiento de servicios y la
comunicación entre microservicios, simplificando la gestión de entornos
y despliegues en la nube.

Componente: PostgreSQL

Tipo: Adoptado

Depende de:

• Java (driver JDBC)

Es usado por:

• vapo-manager-ms

Descripción componente: Motor de base de datos relacional encargado de
almacenar información del sistema, como catálogos de productos, pedidos,
clientes e inventario. Garantiza transacciones seguras y coherencia en
los datos.

9.3.1.2 Componente vapo-catalogo-ms

Descripción del componente:

Componente encargado de gestionar la información de los productos
disponibles en VapoManager, incluyendo sus características, precios y
existencias. Brinda soporte a otros microservicios mediante la
administración centralizada de los catálogos de productos.

Motivación del diagrama:

Diagrama encargado de mostrar todos los componentes involucrados en el
microservicio de catálogos y su relación.

9.3.1.2.2 Documentación

Componente: vapo-catalogo-ms

Tipo: Desarrollado

Depende de:

• Spring Boot 3.x

• Java (JRE 17/21)

• PostgreSQL

• Spring Cloud (config/discovery)

Es usado por:

• vapo-manager-ms

• API Gateway

Descripción componente: Microservicio encargado de administrar la
información de los productos y catálogos del sistema. Permite registrar,
actualizar, consultar y eliminar productos, así como gestionar precios y
disponibilidad de inventario.

Componente: Java (JRE 17/21)

Tipo: Adoptado

Depende de:

Es usado por:

• Spring Boot

• vapo-catalogo-ms

• Spring Cloud

• PostgreSQL

Descripción componente: Entorno de ejecución base utilizado para
ejecutar aplicaciones desarrolladas en Java. Garantiza la compatibilidad
y estabilidad del sistema.

Componente: Spring Boot 3.x

Tipo: Adoptado

Depende de:

• Java (JRE 17/21)

Es usado por:

• vapo-catalogo-ms

Descripción componente: Framework que permite acelerar el desarrollo del
microservicio, proporcionando herramientas para la creación de
aplicaciones empresariales independientes, configuradas y desplegables
fácilmente.

Componente: PostgreSQL

Tipo: Adoptado

Depende de:

• Java (driver JDBC)

Es usado por:

• vapo-catalogo-ms

Descripción componente: Sistema de gestión de bases de datos encargado
de almacenar la información del catálogo de productos, incluyendo
detalles, precios y estado del inventario.

Componente: Spring Cloud (config/discovery)

Tipo: Adoptado

Depende de:

• Spring Boot

• Java (JRE 17/21)

Es usado por:

• vapo-catalogo-ms

Descripción componente: Conjunto de herramientas que facilita la
configuración distribuida y la integración del microservicio dentro del
ecosistema de VapoManager, garantizando comunicación eficiente entre los
diferentes servicios.

## Diagrama de paquetes

**Descripción del componente:**

**Componente encargado de representar la estructura lógica del proyecto
VapoManager, organizado en paquetes que reflejan la arquitectura
hexagonal y la separación de responsabilidades entre capas. Este
diagrama permite comprender cómo se dividen y relacionan los elementos
principales del sistema, favoreciendo la mantenibilidad y escalabilidad
del proyecto.**

**Motivación del diagrama:**

**Mostrar la organización de paquetes dentro de VapoManager,
evidenciando cómo se distribuyen los módulos de dominio, aplicación,
infraestructura y presentación, junto con sus dependencias y relaciones
internas.**

## Componente vapomanager-\<\<component\>\>-ms

**Descripción componente:** Modelo de estructuración y comunicación de
paquetes del componente \<\<component\>\> Este modelo describe las
interacciones de los paquetes que constituyen el componente
\<\<component\>\>, detallando cómo se comunican y colaboran para cumplir
con las responsabilidades en la arquitectura de VapoManager.

## Diagrama

![](media/image8.png){width="6.1375in" height="3.282638888888889in"}

9.3.1.4 Componente vapomanager-paquetes

Descripción del componente:

Componente encargado de representar la estructura lógica del proyecto
VapoManager, organizado en paquetes que reflejan la arquitectura
hexagonal y la separación de responsabilidades entre capas. Este
diagrama permite comprender cómo se dividen y relacionan los elementos
principales del sistema, favoreciendo la mantenibilidad y escalabilidad
del proyecto.

Motivación del diagrama:

Mostrar la organización de paquetes dentro de VapoManager, evidenciando
cómo se distribuyen los módulos de dominio, aplicación, infraestructura
y presentación, junto con sus dependencias y relaciones internas.

9.3.1.4.1 Documentación

Componente: vapomanager-paquetes

Tipo: Desarrollado

Depende de:

• java23

• springboot 3.3.4

• springcloud 4.1.3

• postgresql

Es usado por:

• vapomanager-users-ms

• vapomanager-orders-ms

• vapomanager-products-ms

Descripción componente: Componente principal que define la estructura
modular del sistema, facilitando la implementación de buenas prácticas
de arquitectura hexagonal y promoviendo la independencia entre capas.

Componente: java23

Tipo: Adoptado

Depende de:

(Ninguno)

Es usado por:

• springboot 3.3.4

• vapomanager-paquetes

• springcloud 4.1.3

• postgresql

Descripción componente: Stack base de desarrollo sobre el cual se
construye el sistema, proporcionando compatibilidad con los frameworks y
librerías empleadas en VapoManager.

Componente: springboot 3.3.4

Tipo: Adoptado

Depende de:

• java23

Es usado por:

• vapomanager-paquetes

Descripción componente: Framework que acelera el desarrollo de
microservicios y aplicaciones empresariales, ofreciendo herramientas que
permiten construir sistemas modulares y escalables.

Componente: postgresql

Tipo: Adoptado

Depende de:

• java23

Es usado por:

• vapomanager-paquetes

Descripción componente: Sistema de gestión de bases de datos SQL
utilizado para almacenar de forma persistente la información relacionada
con usuarios, productos, pedidos y ventas.

Componente: springcloud 4.1.3

Tipo: Adoptado

Depende de:

• springboot 3.3.4

• java23

Es usado por:

• vapomanager-paquetes

Descripción componente: Conjunto de herramientas que facilita la
comunicación entre microservicios, la configuración distribuida y la
gestión de servicios en entornos cloud o locales.
