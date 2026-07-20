# Draft RTS — cross-border information exchange between FIUs

> Source: **Draft RTS — cross-border information exchange between Financial Intelligence Units** (AMLA), legal basis **Article 31(3) AMLD6** (Directive (EU) 2024/1640) — draft RTS out for public consultation
> (6 July 2026 – 6 October 2026; Open). Interinstitutional context: EU AML Package (AMLR/AMLA/AMLD6).
> **Working transcription, not an official text** — operative text only (background, consultation questions
> and the cost-benefit annex are omitted); verify against the committed PDF
> [`../../sources/amla/RTS-fiu-cross-border-art31-3_consultation-paper_2026-07-06.pdf`](../../sources/amla/RTS-fiu-cross-border-art31-3_consultation-paper_2026-07-06.pdf) and the [AMLA consultation page](https://www.amla.europa.eu/policy/public-consultations/consultation-draft-rts-cross-border-information-exchange-between-financial-intelligence-units_en).
> When AMLA publishes the final instrument, add a sibling `..._final.md` so `git diff` against this draft is
> meaningful. See [`../../NOTICE`](../../NOTICE).

**Analysis:** [`../../docs/amla-pipeline.md`](../../docs/amla-pipeline.md)

---

COMMISSION DELEGATED REGULATION (EU) …/…
of XXX
supplementing Directive (EU) No 2024/1640 of the European Parliament and of the Council with regard to regulatory technical standards specifying the relevance and selection criteria when determining whether a report submitted pursuant to Article 69(1), first subparagraph, point (a), of Regulation (EU) 2024/1624 concerns another Member State
(Text with EEA relevance)
THE EUROPEAN COMMISSION,
Having regard to the Treaty on the Functioning of the European Union,
Having regard to Directive (EU) 2024/1640 of the European Parliament and of the Council of 31 May 2024 on the mechanisms to be put in place by Member States for the prevention of the use of the financial system for the purposes of money laundering or terrorist financing, amending Directive (EU) 2019/1937, and amending and repealing Directive (EU) 2015/849, and in particular Article 31(3), first subparagraph thereof,

### <a id="recitals"></a>Recitals

(1) Pursuant to Article 31(3) of Directive (EU) 2024/1640, the Anti-Money Laundering Authority (hereinafter referred to as the "AMLA") is required to specify the relevance and selection criteria for determining whether a report of suspicions concerns another Member State, as referred to in Article 31(1) of Directive (EU) 2024/1640.

(2) For the purposes of ensuring consistent and effective cross‑border cooperation and facilitating effective information exchange between FIUs, it is necessary to lay down harmonised rules governing the structure and application of the relevance and selection criteria for the transmission of cross‑border reports (XBRs) and cross‑border disseminations (XBDs), so as to support timely and uniform exchanges among FIUs across the Union.

(3) Clear and objective selection criteria are essential to guarantee that XBRs and XBDs are transmitted promptly and accurately to the competent FIU of the other Member State. These criteria should provide a common framework for identifying links between reports of suspicions and other Member States, thereby reducing delays and improving the efficiency of cross-border information exchange.

(4) The selection criteria should cover different types of connections, including links to natural persons, legal persons and financial assets associated with another Member State. These criteria should be applied in an automatable manner and should not involve any discretionary assessment, in order to ensure consistency, accelerate the identification of such connections and enable the prompt transmission of the report to the FIU of the concerned Member State.

(5) To ensure that the transmission of XBDs is proportionate and limited to cases demonstrating a sufficiently substantiated cross‑border link, the application of the selection criteria should follow a tiered structure. Such a system enables FIUs to distinguish between primary and ancillary selection criteria and to identify, with legal certainty, the Member States to which an XBD must be transmitted. In this context, a full positive hit generated through the Ma³tch functionality should also be considered a relevant selection criterion. This approach mitigates the risk of oversharing and ensures that exchanges of information remain necessary and appropriate for the fulfilment of FIU functions.

(6) In order to ensure effective harmonisation in the application of the selection criteria for the transmission of XBDs, it is appropriate to require that the Ma³tch functionality be used by each FIU, following its implementation within their respective systems.

(7) To ensure that XBDs are likely to be of real interest to the receiving FIU, relevance criteria should complement the application of selection criteria. However, as the assessment of the actual relevance of an XBD can be carried out more effectively and is more appropriately performed by the receiving FIU, responsibility for applying relevance criteria should rest with the receiving FIU, while the transmitting FIU should apply only the selection criteria.

(8) To ensure a clear allocation of responsibilities in cross border exchanges, the FIU that sends an XBR should remain the sole point of contact with the reporting entity, while the FIU receiving the XBR should retain responsibility for managing the report and providing the relevant information associated with any corresponding XBD. This distinction ensures coherent communication flows and preserves the operational integrity of both reporting and analysis functions.

(9) In order to facilitate a consistent baseline approach to the assessment of the relevance of XBDs, a scorecard mechanism should be made available within FIU.net. At the same time, this should not prevent FIUs from developing and applying their own scoring tools, where such tools are better suited to national specificities and operational needs.

(10) This Regulation is based on the draft regulatory technical standards submitted to the Commission by the Authority for Anti-Money Laundering and Countering the Financing of Terrorism.

(11) The Authority for Anti-Money Laundering and Countering the Financing of Terrorism has conducted open public consultations on the draft regulatory technical standards on which this Regulation is based and analysed the potential related costs and benefits.

HAS ADOPTED THIS REGULATION:

### <a id="article-1"></a>Article 1 — Subject Matter

1. This Regulation specifies the relevance and selection criteria when determining whether a report of suspicions, submitted pursuant to Article 69 of Regulation (EU) 2024/1624, concerns another Member State. It defines the nature, function and the rules of application of these criteria, which shall ensure the prompt transmission of such reports to the FIU of that other Member State, in accordance with Article 31(1), third subparagraph, of Directive (EU) 2024/1640.

### <a id="article-2"></a>Article 2 — Definitions

1. For the purpose of this Regulation, in addition to the definitions set out in Article 2 of Regulation (EU) 2024/1624, Article 2 of Directive (EU) 2024/1640 and Article 2 of Commission Delegated Regulation (EU) [yyyy/No] [^r1], the following definitions shall apply:

   (a) 'transmitting FIU' means the FIU that forwards an XBD or an XBR to the FIU of another Member State.

   (b) 'receiving FIU' means the FIU that receives an XBD or an XBR from an FIU of another Member State.

   (c) 'primary subject' means any subject mentioned in the report of suspicions who meets at least one of the following characteristics:

       1. is explicitly identified, in the report, as covering the role of 'victim' or 'alleged perpetrator' by the reporting entity; or
       2. on the basis of the information contained in the report, holds an account at the reporting entity; or
       3. has a financial ranking, where applicable, equal to or greater than 3 pursuant to annex I.

[^r1]: Implementing technical standards adopted pursuant to Article 31(2) of Directive (EU) 2024/1640.

### <a id="article-3"></a>Article 3 — Application of Selection Criteria

1. The transmitting FIU shall identify the selection criteria set out in Articles 4 and 5 for the purpose of assessing whether a report of suspicions concerns another Member State.

2. The selection criteria shall be based on different types of links between a report of suspicions and any Member State other than the Member State to which the report has been transmitted by the obliged entity.

### <a id="article-4"></a>Article 4 — Selection Criteria for the transmission of XBRs

1. A report of suspicions shall be transmitted as an XBR from the FIU which received it by the reporting entity to the FIU of another Member State by using the template specified in Annex V of the Commission Implementing Regulation (EU) 202../xxx [^r1].

2. For the purposes of this Article, the Member State receiving the XBR shall be identified on the basis of the location of the customer of the reporting entity. The location of the customer shall correspond to the usual place of residence or other information as stipulated in Article 22(1), points (a)(iv), of Regulation (EU) 2024/1624 in the case of natural persons, and to the place where the business takes place in the case of legal persons.

3. Where information on the residence of the customer or of the attempted customer cannot be established, the transmitting FIU shall identify the Member State receiving the XBR by applying, in relation to the customer, one of the following criteria in order of priority:

   (a) nationality/ies;
   (b) country of birth.

4. Where, in relation to legal entities, the information on the place where the business takes place cannot be established, the transmitting FIU shall identify the Member State receiving the XBR by applying, in relation to the customer or the attempted customer, one of the following criteria in order of priority:

   (a) country where the address or the official office of the legal entity is registered or other information as stipulated in Article 22(1), points (b)(ii), of Regulation (EU) 2024/1624;
   (b) country of creation.

5. Where the applicable selection criterion corresponds to more than one Member State, the XBR shall be transmitted to the FIU of the Member State that is also identified on the basis of the application of the other relevant selection criteria. Where no single Member State can be determined on that basis, the XBR shall be transmitted to the FIUs of all Member States corresponding to the applicable selection criterion.

6. An XBR may be transmitted to more than one Member State where the report of suspicions concerns at least two subjects, all of whom are customers or attempted customers of the reporting entity, which operates in different Member States.

7. When transmitting an XBR, the transmitting FIU shall, where the selection criteria laid down in Article 5 are also fulfilled, transmit the corresponding key information as an XBD to the FIUs of the other concerned Member States. All receiving FIUs shall be informed that the information has also been shared with other FIUs and shall be provided with an indication of the FIU that received the XBR.

### <a id="article-5"></a>Article 5 — Selection Criteria for the transmission of XBDs

1. A report of suspicions shall be deemed to meet the applicable selection criteria, and the information therein shall be transmitted as XBD to another Member State, where any primary subject or any assets related to a primary subject are linked to that Member State.

2. Where the primary subject is a natural person, the selection criteria shall be deemed to be fulfilled where the link with the other Member State is indicated in at least one of the following data points:

   a. country of usual place of residence or other information as stipulated in Article 22(1), points (a)(iv), of Regulation (EU) 2024/1624;
   b. country where the natural person is subject to criminal investigation;

3. Where the criteria set out in paragraph 2 cannot be established, the following criteria will apply:

   a. nationality/ies
   b. country of birth;
   c. country where the identity document, passport or equivalent was issued.

4. Where the criteria set out in paragraphs 2 or 3 are met, the XBD shall be transmitted to the receiving FIU only where at least one of the following data concerning the primary subject is available in the report of suspicions:

   a. account number;
   b. date of birth;
   c. number of the identity document, passport or equivalent;
   d. usual place of residence or other information as stipulated in Article 22(1), points (a)(iv), of Regulation (EU) 2024/1624.

5. Where the primary subject is a legal person, the selection criteria shall be deemed to be fulfilled where the link with the other Member State is indicated in at least one of the following data points:

   a. country where the business of the legal person takes place;
   b. country where the address or the official office of the legal entity is registered or other information as stipulated in Article 22(1), points (b)(ii), of Regulation (EU) 2024/1624;
   c. country where the legal person is subject to a criminal or administrative investigation.

6. Where the selection criteria set out in paragraph 5 cannot be established, the criteria based on the country of creation will apply.

7. Where the criteria set out in paragraphs 5 or 6 are met, the XBD shall be transmitted to the receiving FIU only where at least one of the following data concerning the primary subject is available in the report of suspicions:

   a. account number;
   b. chamber of Commerce number / registration number;
   c. VAT/Tax identification number;
   d. address of the registered or official office.

8. The selection criteria shall be also deemed to be fulfilled where one or more financial assets related to a primary subject are linked to another Member State, different from the Member State identified under paragraphs 2, 3, 5 and 6, on the basis of the country where accounts or other assets are held.

9. Notwithstanding the previous paragraphs, the selection criteria shall be deemed to be fulfilled where a full positive hit is identified through an automated process within FIU.net, whereby the data made available by an FIU are cross-matched, on a hit/no-hit basis, with the data made available on that system by other FIUs as stipulated in Article 30(4) Directive (EU) 2024/1640. Member States shall ensure that their FIUs implement and make use of the Ma³tch functionality for the purposes of this process by no later than 10 July 2028.

10. Where, following the application of the selection criteria, a connection exists to more than one Member State, the XBD shall be transmitted to all those Member States.

### <a id="article-6"></a>Article 6 — Relevance Criteria

1. In order to identify the XBDs of interest, the receiving FIU shall apply relevance criteria deemed necessary, including those related to the domestic risk-based approach based on National Risk Assessment and, as appropriate, the elements set out in the non-exhaustive list referred to in Article 7(3) of this Regulation, which shall contribute to the establishment of the risk scorecard.

2. Where, after applying the criteria pursuant to paragraph 1, the receiving FIU determines that an XBD is of relevance to its functions, it shall submit a request for information to the transmitting FIU in order to obtain all the relevant information, including any data relating to every subject mentioned in the report.

3. Where, in relation to the same report of suspicions, the transmitting FIU has also transmitted the information as an XBR to another Member State, pursuant to Article 4(6) of this Regulation, the FIU that received the XBD shall address the request to obtain all the relevant information exclusively to the FIU of the Member State that received the XBR.

4. Any such request and the corresponding response, containing the complete set of relevant data relating to the XBD, shall be sent through FIU.net and using the templates for requests and responses provided in the Implementing Technical Standards adopted by the Commission Implementing Regulation (EU) 202../xxx [^r1].

### <a id="article-7"></a>Article 7 — Risk scorecard

1. For the assessment of the relevance criteria applicable to XBDs, the receiving FIU shall assign a risk value to each XBD and may, for that purpose, use a scorecard mechanism based on national information.

2. The scoring mechanism shall be implemented within FIU.net and may, where appropriate, be used, adapted and developed by each receiving FIU outside FIU.net on the basis of the structured key data contained in the received XBDs.

3. The scorecard shall also take into account one or more of the following elements, including but not limited to:

   a. match hits with other FIUs;
   b. number of subjects involved;
   c. predicate offence type;
   d. threshold on transaction amount;
   e. presence of indicators or tags;
   f. negative open-source intelligence;
   g. destination country of money flow;
   h. linkage with ongoing investigations or sanctioned individuals.

### <a id="article-8"></a>Article 8 — Entry into force

1. This Regulation shall enter into force on the twentieth day following that of its publication in the Official Journal of the European Union.

2. It shall apply from 10 July 2027.

3. This Regulation shall be binding in its entirety and directly applicable in all Member States.

Done at Brussels,

For the Commission
The President

### <a id="annex-i"></a>ANNEX I — Financial ranking

This financial ranking is calculated for each structured subject in the report using two indicators:

- the percentage of the number of transactions associated with each subject.
- the percentage of total transaction amount linked to each subject

The algorithm then takes the maximum value from these two indicators and maps it onto a scale ranging from 1 to 5, as outlined in the table below:

| % | Financial Ranking |
|---|---|
| 0 – 10% | 1 |
| 10% – 25% | 2 |
| 25% – 50% | 3 |
| 50% – 75% | 4 |
| > 75% | 5 |
