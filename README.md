# Sehoai-Molemi-Farmer-Advisory
Proposal: Voice-First FarmerAdvisory in
Sesotho
Nov 12, 2026 · @Palo Mosahoeshoe
Summary
By scaling its existing Agrivisory chatbot, the Ministry ofAgriculture, Food Security and
Nutrition can give 50,000 farmers advice in Sesotho by phone within 18 months. The
estimated cost is US$0.57–1.10 million.
Decision requested: endorse the pilot in principle, name a ministry focal person, agree
the pilot districts, and authorise approaches to funders.
Background and problem
Most Lesotho farmers never get advice from an extension officer, and half the country is
offline. A voice service in Sesotho can reach them on the phones they already have.
Item Detail
Lead ministry Agriculture, Food Security and Nutrition, with
MICSTI
What it does Farm and livestock advice in Sesotho and English
by toll-free voice line, SMS, USSD and WhatsApp
Builds on Agrivisory, the open-source chatbot built with ITU
and FAO and field-tested in Berea
Where Berea plus three more districts chosen with the
ministry
Duration 18 months, with a stop-or-scale gate at month 9
Cost US$0.57–1.10 million (planning estimate)
Headline target 50,000 farmers reached, about 22% of agricultural
holders
Proposal: Voice-First Farmer Advisory in Sesotho
Page 1 of 6
Why now
Policies validated. In 2025, more than 100 stakeholders validated Lesotho's Artificial
Intelligence, Data Management, and Broadband and Shared Infrastructure policies
(TechAfrica News).
Strategy under way. In August 2026, MICSTI and the United Nations began drafting a
National AI Strategy (Government of Lesotho). Deputy Prime Minister Justice
Nthomeng Majara asked that safeguards, infrastructure and skills come before AI
spending scales. This pilot is small, staged and gated to meet that test.
A base already exists. ITU and FAO built Agrivisory, an open-source chatbot in
Sesotho and English on WhatsApp and SMS. It answers only from verified Ministry of
Agriculture manuals and is being field-tested in Berea (ITU; ITU project page).
Government is upgrading computing at the Mohale's Hoek Data Centre to support it
(AF.NET).
The problem
Few farmers get advice. Only about 20,800 of Lesotho's 228,000 agricultural holders
(about 9%) reported receiving farm advice in the 2019/2020 agricultural census (FAO
census report).
Livestock is most of farming, but not yet in the chatbot. About 84% of holders keep
animals: 26.8% livestock-only and 56.7% mixed farming. The prototype answers from
crop manuals and crop calendars.
Text-only misses half the country. 68.5% of Basotho live in rural areas. Mobile
connections equal 92.7% of the population, but only 48% use the internet
(DataReportal, Digital 2026). Voice and USSD reach basic phones; WhatsApp does
not.
Design
One answer engine, fed only by ministry-approved content, serves four channels.
Extension officers handle what it cannot answer.
1. One engine, four channels. A farmer calls a toll-free line and asks in Sesotho. Speech
is turned into text, Agrivisory finds the answer in approved content, and a Sesotho
voice reads it back. The same engine serves WhatsApp (text and voice notes), SMS
and a USSD menu.
2. More content. Add livestock health, wool and mohair, rangeland care, seasonal
forecasts from Lesotho Meteorological Services, input-subsidy rules and market
prices. Ministry experts and vets sign off every document before it is loaded.
Proposal: Voice-First Farmer Advisory in Sesotho
Page 2 of 6
3. Extension officers stay in charge. Questions the system cannot answer confidently
go to the district extension officer. A simple dashboard shows officers which pests,
diseases and questions are rising in each area, giving an early outbreak signal.
4. Sesotho speech built locally. Train speech models with the National University of
Lesotho's Sesotho word bank (Government of Lesotho), open Sesotho speech data
such as Mozilla Common Voice and Next Voices-ZA, and new recordings of farmers in
the pilot districts.
5. Safe by design. Answers come only from approved content and name their source
manual. When unsure, the system says so and refers the farmer. It stores only phone
number, district and question, with consent.
6. Photo diagnosis later. Diagnosing disease from a photo (WhatsApp only) is a secondphase option, decided at the month-9 gate.
7. Built to be reused. The Sesotho speech engine is owned by government, so other
ministries can reuse it, for example for a Home Affairs helpline.
Phasing
The pilot runs for 18 months in three phases. It moves to four districts only if it passes a
review at month 9.
The month-9 decision rests on answer quality, repeat use and running cost per farmer. If
the pilot misses, it stops or is redesigned before more money is spent.
Budget range
The 18-month pilot is estimated at US$572,000–1,100,000, including 10% contingency.
proposed phasing · 3 phases, 1 gate
Proposal: Voice-First Farmer Advisory in Sesotho
Page 3 of 6
These are planning estimates. They will be firmed up after operator quotes and a scoping
session with the ministry.
Risks and mitigations
The biggest risk is wrong advice, so every answer comes from approved content and is
audited.
Line item (US$ thousands) Low High Basis
Sesotho speech recognition and
voice
80 150 Data collection with NUL, model
tuning
Platform: voice line, USSD, SMS,
WhatsApp, officer dashboard
150 250 Builds on open-source Agrivisory
Content: livestock, wool and mohair,
weather, prices, expert review
40 80 Ministry and vet experts
Telecom: toll-free minutes, SMS,
USSD sessions
60 150 Rates to negotiate with operators
Hosting and computing 40 100 Government cloud or Mohale's Hoek
Data Centre
Rollout: officer training, farmer
outreach, radio
50 100 Four districts
Monitoring and independent
evaluation
40 70 Includes answer-quality audits
Project management 60 100 Local team
Contingency (10%) 52 100
Total 572 1,100
Risk Mitigation
Wrong advice harms crops or animals Approved content only; vets review
livestock answers; expert audit of 500
random answers each quarter
Speech recognition fails on rural accents or
noisy calls
Local recordings; the system repeats the
question back to confirm; fall back to a
keypad menu
Proposal: Voice-First Farmer Advisory in Sesotho
Page 4 of 6
Success measures
By month 18, the pilot should reach 50,000 farmers with answers experts rate correct and
safe at least 90% of the time.
Targets are proposals, to be agreed with the ministry.
Risk Mitigation
Telecom costs grow with use Negotiated toll-free and zero-rated USSD
rates; monthly cost cap; cost per farmer
tracked
Duplicates ITU and FAO work Co-design with the Agrivisory team; keep
one open-source codebase owned by
government
Farmers do not trust or use it Launch through extension officers, chiefs,
farmer associations and community radio
No money after the pilot Running costs worked out by month 9;
ministry budget line requested from year 2
Measure Target by month 18 How measured
Farmers who used the service 50,000 (about 22% of
holders)
Unique phone numbers
Users who came back 3 or more
times
40% Platform data
Answers graded correct and safe
by experts
90% or more Quarterly random audit
Sessions by voice or USSD 40% or more Shows reach beyond
internet users
Escalated questions answered by
an officer within 72 hours
80% or more Dashboard data
Users reporting a change in
farming practice
30% or more Phone survey at month 15
Running cost per active farmer per
year
Measured and reported
at month 9
Finance and platform
data
Proposal: Voice-First Farmer Advisory in Sesotho
Page 5 of 6
Governance, funding and next steps
A steering group under MICSTI, with the Ministry ofAgriculture, reviews the pilot at
month 9. AI only advises; extension officers and farmers make the decisions.
Safeguards
Data protection. The Data Protection Act 2011 (Act No. 5 of 2012) applies, but its Data
Protection Commission has not yet been appointed (DataProtection.Africa). The pilot
runs its own data protection impact assessment and keeps data in Lesotho.
Hosting. The government private cloud or the Mohale's Hoek Data Centre.
Local skills. Engineers from NUL and local firms build alongside any outside vendor,
with a handover plan from month 1. The code is open source and owned by
government.
Funding partners
Next steps
Partner Why they fit
ITU and FAO Built the Agrivisory prototype with government
UNDP and the UN in Lesotho Supporting the AI strategy and the Sesotho word
bank
Mobile operators Toll-free voice and zero-rated USSD as an in-kind
contribution
Government of Lesotho Staff time, hosting, and running costs after the
pilot
Brief the Principal Secretary forAgriculture and MICSTI's AI strategy team
Name a ministry focal person and agree the three extra districts
Meet the ITU and FAO Agrivisory team to agree how to build on the prototype
Meet NUL's Sesotho word bank team on speech data
Get quotes from mobile operators for toll-free voice, SMS and USSD
Turn this proposal into a funder concept note
Proposal: Voice-First Farmer Advisory in Sesotho
Page 6 of 6
