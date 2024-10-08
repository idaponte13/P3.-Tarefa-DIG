# P3.-Tarefa-DIG

***1.Realiza unha consulta "dig danielcastelao.org" e identifica cada parte da resposta (IN, CNAME, A, QUERY SECTION, ANSWER SECTION, AUTHORITY SECTION, etc)***

Despois de executar o comando `dig danielcastelao.org`, veremos diferentes partes como o header, a seccion de consultas ou question section, a sección de respostas ou answer section e as sección de estadisticas ou stadistics. A continuación se mostrará o que aparece en cada una de ela.

**Header:**  
; <<>> DiG 9.18.28-0ubuntu0.22.04.1-Ubuntu <<>> danielcastelao.org  
;; global options: +cmd  
;; Got answer:  
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 4566  
;; flags: qr rd ra; QUERY: 1, ANSWER: 1, AUTHORITY: 0, ADDITIONAL: 1

**Question Section:**  
;; QUESTION SECTION:  
;danielcastelao.org.		IN	A

**Answer Section:**  
;; ANSWER SECTION:    
danielcastelao.org.	900	IN	A	178.211.133.37  
**danielcastelao.org**: é o dominio solicitado  
**900**: é o tempo de vida en segundos onde a resposta é valida ata que deba consultarse outra vez o DNS  
**in**: é o tipo ou clase de rexistro, neste caso internet  
**A**: é o tipo de rexistro, neste caso direción IPv4.  
**178.211.133.37**: é a direción IPv4 do dominio.

**Statistics:**  
;; Query time: 165 msec  
;; SERVER: 127.0.0.53#53(127.0.0.53) (UDP)  
;; WHEN: Fri Oct 04 21:04:13 CEST 2024  
;; MSG SIZE  rcvd: 63

No meu caso non hai o apartado de AUTHORITY SECTION.  

***2.Realiza consutas dos seguintes nomes e identifica as diferencias: moodle.danielcastelao.org, www.danielcastelao.org***  

Ao realizar as consultas especificadas as diferencias vense reflexadas no apartado de AUTHORITY SECTION. Neste caso aparece o seguinte:  
**;; AUTHORITY SECTION:**    
**danielcastelao.org.	300	IN	SOA	ns1.hover.com. dnsmaster.hover.com. 1720467415 1800 900 604800 300**  

A diferencia é que no moodle aparece o tipo de rexistro "NS" que indica os servidores autoritativos.

***3.Averigua o nome e IP dos servidores de DNS autoritativos de www.danielcastelao.org, por qué soen ser 2 servidores autoritativos?***

***4.Realiza as consultas de nomes inversas: 130.206.164.68 e de outras dúas IPs que se che ocorran.***

***5.A qué servidor DNS estás consultando? Cómo o podes cambiar sen tocar os ficheiros de configuración do sistema?***

***6.Obtén o rexistro SOA (Start of Authority) do dominio  moodle.danielcastelao.org preguntándolle ó servidor DNS de google e logo preoguntándollo directamente ó servidor primario do dominio danielcastelao.org.*** 

***7.Consulta a IP de www.elpais.com. Cánto tempo queda almaceado o rexistro de recurso no DNS local?, se preguntas ó DNS local por este recurso, qué observas no TTL do rexistro?***

***8.Busca o TTL de distintos nomes de dominio de servicios que escollas, a qué se poden deber as diferencias?***

***9.Determina o TTL máximo (original) dun nome de dominio.***

***10.Averigua cántas máquinas con distintas IPs están detrás do dominio web www.google.es, sempre son as mesmas e na mesma orde? por qué?***

***11.Pregunta o mesmo a un server raiz (J.ROOTSERVERS.NET por exemplo) e comproba na resposta se o server acepta o modo recursivo***

***12.Se queremos ver tóda-las queries que fai o servidor de DNS, qué opción temos que usar? averigua a IP de www.timesonline.co.uk, especifica os pasos dados***

***13.Usando a información dispoñible a traveso do DNS especifica a máquina (nome e IP) ou máquinas que actúan como servers de correo do dominio danielcastelao.org***

***14.Podes obter os rexistros AAAA de www.facebook.com? a qué corresponden?***
