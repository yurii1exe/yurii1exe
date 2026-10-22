## Yurii Shchehliuk

**Senior Full-Stack Engineer · C# / .NET · Angular · Next.js · Azure — Chicago, IL**

I build the integration layer: the code that sits between systems that were never
designed to talk to each other, and has to be right every time. Mostly freight
EDI, industrial OPC UA, and the .NET and Angular apps around them.

Everything below is written from public specs. It has tests and CI, and the top
project runs in your browser.

**Open to** senior full-time or contract roles — .NET, Angular, Next.js. Remote or Chicago.
Corp-to-corp via **DIS IT LLC**.
📧 yshchehliuk@gmail.com · 💼 [LinkedIn](https://www.linkedin.com/in/yurii1exe/) · 🌐 [disit.tech](https://disit.tech)

---

### Open source

#### [edi-x12-toolkit](https://github.com/yurii1exe/edi-x12-toolkit) — [**▶ try it in your browser**](https://yurii1exe.github.io/edi-x12-toolkit/)
*C# · netstandard2.0 + net8.0 · WebAssembly · zero dependencies · MIT*

A .NET parser and validator for ANSI X12, the EDI format US freight runs on. Most
X12 code hardcodes `*` and `~` and breaks on the first partner that uses pipes.
This one reads the delimiters from the ISA header the way the standard intends,
and reports envelope errors such as a wrong SE01 segment count (a common reason
a partner rejects a file) as named diagnostics. It ships as a library, a
`dotnet` CLI tool, and a playground that runs the same parser compiled to
WebAssembly.

<a href="https://yurii1exe.github.io/edi-x12-toolkit/"><img src="https://raw.githubusercontent.com/yurii1exe/edi-x12-toolkit/main/docs/playground-demo.gif" alt="The X12 playground reading the delimiters from two versions of the same document and flagging an SE01 segment-count error" width="720"></a>

#### [freight-dispatch-board](https://github.com/yurii1exe/freight-dispatch-board)
*.NET 8 minimal API · Angular · xUnit · CI*

The loop every freight brokerage runs, built end to end: a load tender (EDI 204)
comes in and gets acknowledged, a dispatcher works the load stop by stop, every
status change emits the 214 that reports it, and an invoice closes it out. Every
outbound document is re-parsed before it's shown, so the board never displays a
file that a trading partner would reject.

<img src="https://raw.githubusercontent.com/yurii1exe/freight-dispatch-board/main/docs/board-demo.gif" alt="Dispatch board: a load tender arrives, the load moves across a multi-stop route, and each status change generates its EDI 214" width="720">

#### [opc-ua-monitor](https://github.com/yurii1exe/opc-ua-monitor)
*.NET 8 · SignalR · Angular · OPC UA*

Live monitoring for industrial equipment. A .NET service subscribes to an OPC UA server and streams node values to a live Angular
dashboard. When a connection drops, it keeps showing the last values but marks
them as stale, so nobody reads old data as current.

#### Also

- **[fmcsa-carrier-check](https://github.com/yurii1exe/fmcsa-carrier-check)** — Next.js 15 / React 19 carrier vetting on the public FMCSA API: authority, insurance, safety rating, inspections. 188 tests.
- **[ECommerce-Restaurant](https://github.com/yurii1exe/ECommerce-Restaurant)** — .NET microservices with MassTransit/RabbitMQ, Redis, EF Core, JWT and Angular, all running under one Docker Compose file.

---

### Stack

**Backend** C# · .NET 8 / 6 · ASP.NET Core · EF Core · REST · SignalR · RabbitMQ / MassTransit · Node.js
**Frontend** Angular · RxJS · TypeScript · React · Next.js
**Data** SQL Server · T-SQL · PostgreSQL · MongoDB · Redis
**Cloud & DevOps** Azure (App Service, Functions, Event Hub, IoT Hub, Key Vault) · Docker · CI/CD · GitHub Actions
**Integration** EDI ANSI X12 · CargoWise · TMW · OPC UA · DICOM · HL7
