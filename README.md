# 13Grid-BienesRaices
* 13 Grid Layout  Bienes Raíces. Custom Properties. Uso de variables

```javascript
.header .barra {
    display: grid;
    grid-template-rows: repeat(2, auto);
    gap: 2rem;   
}
.header .menu {
    display: grid;
    /* posible que tenga mas menus se agrega auto-fit */
    grid-template-columns: repeat(auto-fit, minmax(107px, 1fr) );  
}
@media screen and (min-width: 768px) {
    .header .barra {
        /* 1fr queda en el medio para la separacion del logo y menú */
        grid-template-columns: 30% 1fr 50%;
        /* al inspeccionar debajo se encuentra el row definido para movil, se debe quitar */
        grid-template-rows: unset;      
    } 
    .header .menu {
        grid-column: 3/4;
        display: grid;
        align-items: center;
    }
}

/* Nosotros */ 
.nosotros {
    text-align: center;
    margin-top: 1rem;
}
.contenido-nosotros {
    display: grid;
    /* align-items: center; */
    /* alinea verticalmente */
    align-content: center;
}
@media screen and (min-width:768px){
    .nosotros {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        gap: 1rem;
        text-align: left;
    }
}
/* Venta */
.venta {
    display: grid;
    /* Móvil */
    grid-template-columns: repeat(2,1fr);
    grid-template-rows: repeat(3, auto);
    gap: 1rem;
}
.venta img{
    width: 100%;
}
/* clase destacada será grid para tomar img y class card */
.destacada {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-column: 1 / 3;
    /* gap para separar img y texto */
    /* gap: 1rem; */
}

/* media desktop 3 columnas*/
@media screen and (min-width:768px) {
    .venta {
        grid-template-columns: repeat(3, 1fr);
        grid-template-rows: repeat(2,auto);
    }
}

* Footer */
.footer {
    background-color: var(--primario);
    margin-top: var(--padding2);
    padding-top: var(--padding2);
    color: var(--blanco);
}

@media screen and (min-width:768px) {
    .footer .contenedor {
        display: grid;
        grid-template-columns: 30% 20% 2fr;
        gap: 1rem;
    }
}
.footer .widget h3 {
    margin-bottom: 2rem;
}
.contenedor .navegacion a {
    display: block;
    color: var(--blanco);
    font-size: 1.4rem;
    margin-bottom: 1rem;
    text-decoration: none;
}

.widget .contenedor-casas {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    grid-template-rows: repeat(2, auto);
    gap: 1rem;
}

.footer .contenedor-casas .casa {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 1rem;
}
```
