## Yurii Shchehliuk

**Full-stack engineer — .NET, Angular, Next.js. Based in Chicago.**

Seven years building systems that have to talk to each other and can't afford to
be wrong. Most of my work sits where two things meet: an API and a legacy
database, a web app and a piece of factory equipment, a modern front end and a
protocol from 1985. That's the part most people would rather not do, and it's the
part I'm good at.

I've shipped in four domains, and the constraint is what changes — not the craft:

| | |
|---|---|
| **Freight & logistics** | EDI ANSI X12, TMS integration (CargoWise, TMW), carrier compliance, WMS and yard management. Currently ~500 transactions/day |
| **Healthcare** | DICOM and HL7 integration for medical imaging, under HIPAA |
| **Manufacturing** | OPC UA interfaces for real-time production monitoring, under ISO 9001 |
| **E-commerce** | Microservices, payments, catalogue and pricing integrations |

---

### Selected work

**[freight-dispatch-board](https://github.com/yurii1exe/freight-dispatch-board)**
· *.NET 8 · Angular · real-time state machine*
A dispatch board driven by a stateful workflow over multi-stop routes, with EDI
in and out. Every state transition emits a message that's parsed straight back to
prove it's valid — and the human view sits next to the wire format on screen.

![dispatch board](https://github.com/yurii1exe/freight-dispatch-board/raw/main/docs/board-demo.gif)

**[edi-x12-toolkit](https://github.com/yurii1exe/edi-x12-toolkit)**
· *C# · netstandard2.0 + net8.0 · dotnet CLI*
A parser and validator for a fixed-width-then-delimited binary-ish text format
where the delimiters are declared inside the first segment that uses them. Zero
dependencies, 64 tests, and a CLI whose every documented transcript is
regression-tested against the real binary.

![edix12 cli](https://raw.githubusercontent.com/yurii1exe/edi-x12-toolkit/main/docs/edix12-demo.gif)

*Same command, two files — one delimited with `*` and `~`, the other with `|`
and newlines. Both read correctly, because the delimiters come out of the ISA
segment rather than an assumption.*

**[fmcsa-carrier-check](https://github.com/yurii1exe/fmcsa-carrier-check)**
· *Next.js 15 · React 19 · TypeScript*
Server-side API integration with real failure handling — including an upstream
that returns 404 for "bad credential" and 404 for "not found", which most clients
get wrong. 103 tests.

**[ECommerce-Restaurant](https://github.com/yurii1exe/ECommerce-Restaurant)**
· *.NET · microservices · Docker*
Four services, Redis-backed basket, two EF Core databases, Serilog to Seq, behind
nginx, with an Angular front end. The whole stack comes up under Compose.

**[Playbook](https://github.com/yurii1exe/Playbook)**
· *.NET · Puppeteer · MongoDB*
A resilient scraping pipeline — 16 sources, layered selector fallbacks,
idempotent writes, and a retry budget, because the sites change without warning
and the job still has to finish.

---

### Stack

**Backend** `C#` · `.NET 6/7/8` · `ASP.NET Core` · `EF Core` · `Node.js` · `REST` · `SignalR` · `RabbitMQ`
**Frontend** `Angular` · `TypeScript` · `RxJS` · `React` · `Next.js` · `SCSS`
**Data** `SQL Server` · `T-SQL` · `PostgreSQL` · `MongoDB` · `Redis`
**Platform** `Azure` · `Docker` · `CI/CD` · `OPC UA` · `EDI X12` · `DICOM/HL7`

---

### Open to work

Full-time or contract — .NET, Angular, Next.js. Remote or Chicago area.
Corp-to-corp available through **DIS IT LLC** (Illinois).

📧 yshchehliuk@gmail.com · 💼 [LinkedIn](https://www.linkedin.com/in/yurii1exe/) · 🌐 [disit.tech](https://disit.tech)
