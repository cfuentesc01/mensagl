# MensAGL 🔥 LosCowboysDelInfierno 🔥

Un servidor de comunicaciones unificadas que incluye mensajería instántanea, llamadas y videoconferencia.
Creado en AWS (Amazon Web Service) pensado para uso cotidiano y con la posibilidad de ser escalable.

![Screenshot]

## Introducción 📝
El sistema se compone de 4 redes en su totalidad, siendo 2 de ellas redes publicas para usar un proxy como balanceo de carga en las redes privadas.
En cada red privada se crean 2 instancias iguales, utilizando el proxy publico como balanceo de carga de solicitudes de los mismos y en cada red, utilizando diferentes tecnologias para la preservación de datos.
Hay tanto un sistema de mensajería como un sistema de resolución de incidencias.

El servicio de mensajería se compone de:
- Proxy publico con dominio dinámico (DDNS) `DuckDNS`. 🌐
- Clúster de mensajeria instantánea `XMPP Prosody`, llamadas y videoconferencia `Jitsi`. 💬 🔊
- Instancia EC2 `MySQL` para el servicio de mensajería, con otra instancia tipo NAS como copia de seguridad. 🏗️

El servicio de incidencias se compone de:
- Proxy publico con dominio dinámico (DDNS) `DuckDNS`. 🌐
- Clúster CMS `Wordpress` coon sistema de tickets / resolución de incidencias. 👷
- Instancia `RDS MySQL` AWS como base de datos flexible para el clúster CMS. 🚩

## Instalación 🔧

### AWS CLI

1. Clona el repositorio ♻️

```bash
git clone https://github.com/cfuentesc01/mensagl.git
cd mensagl
```
##  🚨 Still in development 🚧
![z37wrt6awmkd1](https://github.com/user-attachments/assets/3cadc2d4-bcfc-4751-bde9-c74307269490)
