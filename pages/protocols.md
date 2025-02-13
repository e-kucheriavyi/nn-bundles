# Protocols

<v-click>

## HTTP/1

> Один большой файл лучше нескольких файлов поменьше

<br>

</v-click>

<v-click>

## HTTP/2

> Несколько файлов поменьше лучше одного большого

<br>

</v-click>

<v-click>

## HTTP/3 (HTTP-over-QUIC)

> Как HTTP/2, но решает некоторые проблемы и ускоряет TLS-handshake

</v-click>

---
transition: fade
---

# Self-hosting файлов

```mermaid
sequenceDiagram
	Client ->> DNS: Resolve fonts.google.com
	DNS -->> Client: x.x.x.x;
	Client ->> fonts.google.com: GET;
	fonts.google.com -->>Client: Montserrat.woff;
```

---

# Self-hosting файлов

```mermaid
sequenceDiagram
	Client ->> larana.tech: GET;
	larana.tech -->> Client: Montserrat.woff;
	Client ->> larana.tech: GET;
	larana.tech -->> Client: favicon.ico;
```
