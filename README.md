## Yurii Shchehliuk

**I build the integrations that logistics runs on.**

Load tenders, status messages and invoices moving between systems that were never
designed to talk to each other — EDI on one side, a TMS on the other, .NET in the
middle. Right now that's 500+ transactions a day for a Chicago freight company.

Seven years of commercial development. The through-line is systems that have to
talk to each other and can't afford to be wrong:

| Domain | What that meant |
|---|---|
| **Freight & logistics** | EDI ANSI X12 (204 / 210 / 214 / 997), CargoWise and TMW integration, carrier compliance via Highway and RMIS, WMS and yard management |
| **Manufacturing** | OPC UA interfaces for real-time production line monitoring, under ISO 9001 |
| **Healthcare** | DICOM and HL7 integration for medical imaging, under HIPAA |

Based in Chicago. I work through **DIS IT LLC** (Illinois).

---

### Things I've built

**[edi-x12-toolkit](https://github.com/yurii1exe/edi-x12-toolkit)** — parse,
validate and generate ANSI X12 freight EDI in .NET.
Reads all four delimiters from the ISA rather than assuming `*` and `~`, handles
ISA11 correctly across 4010 and 5010, and ships a `dotnet` CLI. `netstandard2.0`
and `net8.0`, because plenty of the 3PL world is still on .NET Framework.

**[fmcsa-carrier-check](https://github.com/yurii1exe/fmcsa-carrier-check)** —
carrier vetting from a DOT or MC number.
Operating authority, insurance filings, safety rating and inspection history,
straight from the FMCSA QCMobile API. A missing safety rating is reported as
information rather than a red flag, and out-of-service rates are suppressed below
five inspections — because 1-of-2 is a 50% rate and means nothing.

**[ECommerce-Restaurant](https://github.com/yurii1exe/ECommerce-Restaurant)** —
four .NET services, Redis-backed basket, two EF Core databases, Serilog to Seq,
behind nginx, with an Angular front end. The whole stack comes up under Compose.

**[Playbook](https://github.com/yurii1exe/Playbook)** — a data pipeline that
scrapes 16 leagues across 14 countries, 108 data points per match, with layered
selector fallbacks and idempotent writes. Structurally the same problem as an
EDI feed: a source you don't control, a format that changes without notice.

---

### Stack

`C#` · `.NET 6/7/8` · `ASP.NET Core` · `Angular` · `TypeScript` · `RxJS` · `Next.js`
`Azure` · `Docker` · `SignalR` · `OPC UA` · `EF Core` · `SQL Server` · `MongoDB`
`RabbitMQ` · `Redis` · `CI/CD`

---

### Open to contract work

.NET and Angular, freight and logistics integration especially. Corp-to-corp
through DIS IT LLC, or W2 — whichever suits the client. Remote or Chicago area.

If a trading partner is rejecting your files and the error doesn't say why, send
me the interchange and I'll tell you which segment is wrong.

📧 yshchehliuk@gmail.com · 💼 [LinkedIn](https://www.linkedin.com/in/yurii1exe/) · 🌐 [disit.tech](https://disit.tech)
