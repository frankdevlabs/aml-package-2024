# Draft ITS — format for reporting suspicions and providing transaction records

> Source: **Draft ITS on the format for reporting suspicions and providing transaction records** (AMLA), legal basis **Article 69(3) AMLR** (Regulation (EU) 2024/1624) — draft ITS out for public consultation
> (2 July 2026 – 20 September 2026; Open; public hearing 9 September 2026). Interinstitutional context: EU AML Package (AMLR/AMLA/AMLD6).
> **Working transcription, not an official text** — operative text only (background, consultation questions
> and the cost-benefit annex are omitted; Annexes I and II are separate data-point documents not reproduced here);
> verify against the committed PDF
> [`../../sources/amla/ITS-reporting-format-art69-3_consultation-paper_2026-07-02.pdf`](../../sources/amla/ITS-reporting-format-art69-3_consultation-paper_2026-07-02.pdf) and the [AMLA consultation page](https://www.amla.europa.eu/policy/public-consultations/consultation-draft-its-format-reporting-suspicions-and-providing-transaction-records_en).
> When AMLA publishes the final instrument, add a sibling `..._final.md` so `git diff` against this draft is
> meaningful. See [`../../NOTICE`](../../NOTICE).

**Analysis:** [`../../docs/amla-pipeline.md`](../../docs/amla-pipeline.md)

---

COMMISSION IMPLEMENTING REGULATION (EU) …/...
of XXX
laying down implementing technical standards for the application of Regulation (EU) 2024/1624 of the European Parliament and of the Council with regard to the format to be used for the reporting of suspicions and the provision of transaction records
(Text with EEA relevance)
THE EUROPEAN COMMISSION,
Having regard to the Treaty on the Functioning of the European Union,
Having regard to Regulation (EU) 2024/1624 of 31 May 2024 of the European Parliament and of the Council on the prevention of the use of the financial system for the purposes of money laundering or terrorist financing, and in particular Article 69(3) thereof,

### <a id="recitals"></a>Recitals

1. For the purpose of enhancing uniformity and therefore lesser the difficulties experienced by obliged entities regarding AML/CFT compliance and improve the quality of the data shared and the analysis capacities of Financial Intelligence Units (FIUs), these Implementing Technical Standards (ITS) specify the format to be used by obliged entities for the reporting of suspicions and for the provision of transaction records to FIUs.

2. The format to be used for the reporting of suspicions and the provision of transaction records should comprise both their content, namely the data points required by this Regulation, and their technical specifications, namely the manner in which those data points are to be provided.

3. The list of data points as well as their respective definition and treatment should be annexed to this Regulation.

4. To facilitate their adaptation over time and their understanding, the structure and technical specifications of the data points should be provided in a separate interpretative note published by AMLA, along with, where necessary, a guidance for filling them in.

5. To ensure adequacy and interoperability with the national reporting platforms, the structure provided by this Regulation for the reporting of suspicions should allow for flexibility in the way the data points are technically implemented at a national level.

6. As for transaction records, the format provided by this Regulation should be prescriptive and provided in a machine-readable format decided by FIUs to ensure interoperability with their respective data analysis systems or reporting systems.

7. To enhance information sharing among stakeholders, to promote harmonisation and convergence across the European Union, and to address the difficulties experienced in their AML/CFT compliance by obliged entities that have a cross-border presence or operations, this Regulation should aim, to the maximum extent possible, at reaching convergence between the formats used across the European Union for the reporting of suspicions and the provision of transaction records.

8. Notwithstanding the convergence objective, harmonised templates should accomodate for national specificities and therefore provide for adapted data points where they cannot be used by all FIUs. Such FIU-required data points should be limited to situations where their use or absence would lead to disproportionate adaptation costs or pose a risk to FIUs' analysis capacities.

9. To ensure efficiency and accuracy of the reporting of suspicions and the provision of transaction records while facilitating the reporting process for the obliged entities, the formats should be adapted to the specificities of the various obliged entities and to the type of suspicion they report. Therefore, this Regulation differentiates the information to be provided depending on the activity of the reporting obliged entity and the suspicion reported through data points identified as "dependent" and "mandatory if available". Consequently, the data model and the reporting platforms should ensure that only the necessary and relevant data points are required from the reporting obliged entity, depending on its type and on the suspicion reported. Additionally, the information should be requested only where necessary and relevant to support the reported suspicion.

10. Obliged entities and FIUs always remain subject, when collecting and transmitting data for the implementation of the ITS, to their applicable data protection regimes, with particular attention to the purpose limitation and data minimisation principles to ensure not encroaching in the fundamental rights of those affected by the measure.

11. To foster quality of analyses and information exchanges, obliged entities shall ensure that the data reported meet the quality requirements set by FIUs.

12. To strive for the highest possible harmonisation of the reporting formats, a two-phase process should be established.

13. The annexes set out before these two phases should be considered as a core data set to be used as a common basis for further harmonisation.

14. The first phase should consist of the assessment by FIUs of the completeness and accuracy of the data points referred to as forming the core data set, as per recital 13. This assessment should include a gap analysis between data points already used by FIUs and the data points set out in the annexes to this Regulation under a process coordinated by AMLA, followed by a collective decision-making process coordinated by AMLA to adapt, where necessary, these annexes, with the objective of defining and finalising harmonised templates applicable, to the extent possible, across all FIUs.

15. The second phase should be dedicated to the technical implementation of this Regulation and its annexes into FIUs' and obliged entities' reporting systems. It should be initiated starting from the end of the first phase referred to in Recital 14.

16. Furthermore, a periodic review mechanism should be established in order to ensure a consistent and structured approach for addressing future needs for adaptation once harmonised formats have been fully implemented.

17. A dedicated permanent working group composed of FIU representatives and AMLA staff shall be permanently responsible for discussing the changes to be applied to the annexes before their approval by the General Board of AMLA, and for discussing and deciding the changes to be applied to the interpretative note.

18. To allow for flexibility in cases of emergencies, of emerging trends or of adaptation to EU or national laws where it cannot await the next planned periodic review, a mechanism allowing FIUs to temporarily add a data point before completing the periodic review process should be provided by way of derogation from the periodic review process.

19. Such addition or change for emergency reason should be duly justified and respect the applicable data protection regimes of FIUs, with particular attention to the purpose limitation and data minimisation principles.

20. To aim at convergence in the use of these data points even before they are submitted to the periodic review process, this mechanism should include the communication of this information, by the concerned FIU, to the dedicated working group.

21. The national systems for reporting of suspicions as formatted by this Regulation will be assessed by 10 July 2032 pursuant to Article 87(a) of Regulation (EU) 2024/1624. This assessment may lead to the identification of obstacles and opportunities to establish a single reporting system at Union level.

22. Due to the customer due diligence obligations laid down by Chapter III of Regulation (EU) 2024/1624 and the technical standards deriving from them, obliged entities should collect various information from their customers, business relationships, occasional or linked transactions. This Regulation takes into account the collected information stemming from this obligation to determine some of the characteristics of the data points to be used for reporting suspicions.

23. Simplification is a core component of the mandate of the Authority. By introducing standardised formats, the instrument reduces reporting differences across the European Union, facilitates cross-border businesses across the EU and enhances the efficiency of cooperation among FIUs.

24. This Regulation specifies the format for the provision of transaction records by credit institutions and financial institutions where required by an FIU pursuant to article 69(1) paragraph (b) of Regulation (EU) 2024/1624, as stated by Recital 140 of Regulation (EU) 2024/1624. To adapt to the different information available to different types of institutions, different templates have been developed for various activities, including banking and payment activities, money remittance flows, crypto assets accounts and correspondent services activities.

25. The transaction records provided by the credit institutions and financial institutions should include all necessary information related to each of the transactions carried out to or from an account on the period requested by the FIU.

26. Considering the technical and practical implications of the implementation of the format set by this Regulation, sufficient adaptation time should be allocated to FIUs and obliged entities.

27. This Regulation is based on the draft implementing technical standards submitted to the Commission by the Authority for Anti-Money Laundering and Countering the Financing of Terrorism.

28. The Authority for Anti-Money Laundering and Countering the Financing of Terrorism has conducted open public consultations on the draft implementing technical standards on which this Regulation is based and analysed the potential related costs and benefits,

HAS ADOPTED THIS REGULATION:

## CHAPTER 1 — GENERAL PROVISIONS

### <a id="article-1"></a>Article 1 — Subject matter

This Regulation lays down implementing technical standards on reports of suspicions and transaction records by specifying the format to be used by the obliged entities for the reporting of suspicions pursuant to Article 69, paragraph 1, point (a) of Regulation (EU) 2024/1624, and for the provision of transaction records pursuant to Article 69, paragraph 1, point (b) of Regulation (EU) 2024/1624. This format will be used as a uniform basis throughout the Union, pursuant to Recital 139 of Regulation (EU) 2024/1624.

### <a id="article-2"></a>Article 2 — Definitions

For the purposes of this Regulation the following definitions shall apply:

1. "reporting of suspicions" means the reporting without a prior request, by an obliged entity, of any knowledge or suspicion that funds or activities, including transactions and any type of behaviour, and regardless of the amount involved, are the proceeds of criminal activity or are related to terrorist financing or criminal activity, in accordance with Article 69(1)(a) of Regulation (EU) 2024/1624.

2. "transaction record" means the details of operations which have been carried out during a defined period through a specified payment account, as defined in Article 2, point (5), of Regulation (EU) No 260/2012 of the European Parliament and of the Council, or a bank account identified by IBAN, as defined in Article 2, point (15), of that Regulation, or the details of transfers of crypto-assets, as defined in Article 3, point (10), of Regulation (EU) 2023/1113 of the European Parliament and of the Council, or through a money or value transfer services provider. At the request of the FIU or upon voluntary basis, those operations may relate to completed, scheduled, attempted, rejected, cancelled, suspended, refrained or frozen transactions.

3. "obliged entities" means any entity pursuant to Article 3 of Regulation (EU) 1624/2024 and any entity to which a Member State decides to apply Article 69 of Regulation (EU) 1624/2024, pursuant to Article 3 paragraph 1 of Directive (EU) 2024/1640.

4. "data point" means the designation of any digital representation of acts, facts or information and any compilation of such acts, facts or information to which refers Art. XX of this Regulation.

5. "attribute" means the form under which a data point shall be reported.

6. "value" means the reported information for a data point.

7. "template" means a structured set of definitions that specifies the concepts, attributes, and relationships to be included in a report, ensuring consistent interpretation, representation, and usage of information across the report content.

The data points formatted by Article 3 and Article 4 of this Regulation are defined in Annex I and II.

### <a id="article-3"></a>Article 3 — Format for the reporting of suspicions

1. The format to be used for the reporting of suspicions pursuant to Article 69(3)(a) of Regulation (EU) 1624/2024 shall be understood as the following elements framing the reporting of the required data points:

   a. Their definitions and their "mandatory", "mandatory if available", "optional", "dependent", or "FIU-required" nature, specified in Annexe I.
   b. The attributes and values, where specified in the interpretative note referred to in Article 3, paragraph 7, under which they must be reported, and the data structure governing their transmission.

2. When reporting suspicions, obliged entities shall report the information requested in their corresponding template provided in Annex I of this Regulation.

3. This template is composed of data points common to all obliged entities as well as data points adapted to the activity performed by the reporting obliged entity, represented in separate templates in Annex I.

4. Data points shall be requested by FIUs depending on the activity carried out by the reporting obliged entity as well as on the type of suspicion being reported on the basis of the treatment provided in Annexe I.

5. The data points listed in Annex I shall be reported by obliged entities to FIUs either on a mandatory, mandatory if available, or optional basis.

   a. Data points referred to as "mandatory" shall be required by FIUs and provided by obliged entities in a systematic manner. Among them, data points referred to as "technically required" are mandatory data points whose absence breaks the validation rules and checks set out by FIUs and therefore shall prevent the submission of a report of suspicions.
   b. Data points referred to as "mandatory if available" shall be required by FIUs and provided by obliged entities where the information is available to the obliged entity at the time of reporting.
   c. Data points referred to as "optional" shall be provided to FIUs on a voluntary basis where they are considered by obliged entities as relevant to better substantiate the reported suspicion.

6. In addition to the treatment mentioned in paragraph 5, data points can be of dependent and FIU-required nature:

   d. Data points referred to as dependent shall be required by FIUs and provided by obliged entities only when a specific parent data point or circumstance is present. Where the relevant condition is met, the treatment to be applied to such datapoints shall be specified (mandatory, mandatory if available, optional).
   e. Datapoints referred to as FIU-required may be required by FIUs only if they are required under national legislation or specific national circumstances. Obliged entities shall report them if they are required to by the FIU, which decides the treatment to be applied. FIUs not applying them may decide not to implement them in their national reporting systems.

7. Technical specifications of each data point that may be used by FIUs are included in an interpretative note published by AMLA, including proposed corresponding validation rules, attributes and values, and definitions.

8. Reports of suspicions shall be transmitted electronically in a machine-readable format through the reporting platforms of the FIU. In case of emergency or of impossibility to use the usual reporting channels and file formats, FIUs may accept a different secure transmission format, in accordance with national regulations.

9. The information related to the reporting obliged entity and its registration and submission process such as its identity, the related contact details, or the authentication or signature of the report, shall be set and collected by FIUs as technical reporting requirements that are not covered by this Regulation.

10. While FIUs decide the technical implementation of the data points into their reporting platforms, the technical specifications shall strive to align with the specifications set in the interpretative note. AMLA may provide further detailed data model and data exchange technical format specifications and related submission procedures, which may be used by FIUs for the accepted data exchange formats.

### <a id="article-4"></a>Article 4 — Format for providing transaction records

1. When providing transaction records upon request pursuant to Article 69(1) paragraph (b) of Regulation (EU) 2024/1624, credit institutions and financial institutions shall report the information requested in the templates provided by this Regulation in Annex II and provide all requested information that is in their possession.

2. Credit and financial institutions shall use the template corresponding to the type of activity they are reporting.

3. Transaction records shall be transmitted electronically in a machine-readable format specified by FIUs through the reporting platforms of the FIUs or upon request through the most adequate channel specified by the FIU. In case of duly justified emergency or of impossibility to use the usual reporting channels and file formats, FIUs may accept a different secure transmission format, in accordance with national regulations.

### <a id="article-5"></a>Article 5 — Other characteristics

1. The formats for the reporting of suspicions and for the provision of transaction records shall be filled in the language used or requested by the FIU to which it is reported.

2. The labels of the data points as provided in the templates shall correspond to the exact definition and scope provided in this Regulation.

### <a id="article-6"></a>Article 6 — Attachments

Obliged entities shall attach any available supporting document to their report of suspicion in the following situations:

1. Upon request or general instruction from FIUs;
2. On a spontaneous basis, where they identify that documents in their posession may be of interest to support the report of suspicion.

### <a id="article-7"></a>Article 7 — Periodic review

1. The data points provided in Annexes I and II may be reviewed every four years starting from the achievement of the technical implementation as referred to in Article 10.

2. The review shall be coordinated by AMLA through a dedicated permanent working group composed of FIUs' representatives and AMLA staff and permanently responsible for elaborating an opinion on the review of the Annexes before its approval by the General Board of AMLA.

3. FIUs may propose the addition or deletion of data points, as well as amendments to their name and treatment.

4. The review of a data point shall be proposed where one or more of the following conditions are met:

   a) An existing data point is used only to a very limited extent by obliged entities or provides very limited value to the FIU's financial intelligence.
   b) A new data point with potential to enhance financial intelligence is identified through the results of threat assessments or strategic analyses conducted pursuant to Article 5(m) of Regulation (EU) 2024/1620.
   c) A new data point is identified through its use in a partnership for information sharing established in accordance with Article 75 of Regulation (EU) 2024/1624.
   d) A new data point is identified in the context of national or supranational risk assessments carried out under Article 7 of Directive (EU) 2024/1640, following an opinion issued by the Authority.
   e) Technological and legal developments indicate the need to introduce new data points or to collect existing data points using different methods or formats.

5. The General Board of AMLA shall approve the amendments to be submitted by AMLA to the European Commission, including the amended Annexes and a statement of reasons for the proposed updates, in accordance with paragraph 3.

6. The decision of the General Board of AMLA shall include the treatment to be applied to each new data point except for FIU-required data points. It shall include the addition of FIU-required data points where no harmonisation could be achieved.

7. Notwithstanding paragraphs 1 and 2, the working group referred to in Article 7, paragraph 2, is permanently responsible for proposing the changes to be applied to the technical specifications set out in the interpretative note referred to in Article 3, paragraph 7 of the data points set out in the Annexes to this Regulation. Those proposals shall be adopted by the General Board of AMLA or a relevant representative body chosen by it.

### <a id="article-8"></a>Article 8 — Adaptation to emerging trends or urgent and unforeseen circumstances

1. Where an exceptional and unforeseen event, such as a threat to State security, the emergence of new trends or an EU or national legislation creates the need to collect additional information from all or part of the obliged entities which cannot await the next planned periodic review, FIUs may add data points to their national reports of suspicions. These data points shall remain applicable until a decision is taken pursuant to paragraph 4 of this Article.

2. In such cases, FIUs shall promptly inform the working group referred to in Article 7, paragraph 2, of this addition with a detailed explanation of the rationale.

3. The working group referred to in Article 7, paragraph 2, shall agree on the name and the technical specifications to be used before these data points are submitted to the periodic review process.

4. The additional data points shall be submitted by the working group referred to in Article 7, paragraph 2, to the General Board of AMLA for approval of their inclusion in one of the Annexes of this Regulation through the next review carried out pursuant to article 7 of this Regulation.

### <a id="article-9"></a>Article 9 — Data quality

When submitting to FIUs the data referred to in Articles 3 and 4 of this Regulation, obliged entities shall ensure that such data are complete and address the validation rules verifying their technical accuracy, data quality checks ensuring consistency and completeness of the information reported, and plausibility checks put in place by FIUs.

### <a id="article-10"></a>Article 10 — Adaptation period

1. The application of the provisions related to the format for the reporting of suspicions shall follow a two-phase process.

2. The first phase shall be carried out as follows:

   a. Within two years following the publication of this Regulation, FIUs shall carry out an assessment of the completeness and the accuracy of the Annexes, including a gap analysis between the Annexes and the data points they already use, and an assessment of the impact of the implementation of the Annexes in their national reporting platforms and analysis platforms. It shall form the basis on which AMLA shall, in cooperation and mutual agreement with FIUs, review the Annexes to this Regulation with the aim of developing a harmonised reporting format and seeking for converging the data collection methods where possible. It shall accommodate national specificities through data points referred to as FIU-required, but shall limit them to situations where their use or absence would lead to disproportionate adaptation costs or pose a risk to FIUs' analysis capacities.
   b. The General Board of AMLA shall adopt decisions on that review, including the addition, removal, merging, or amendment of the data points set out in the Annexes.
   c. The General Board of AMLA shall submit the reviewed Annexes to the Commission for adoption.

3. The second phase shall be carried out as follows:

   a. Within [...] years following the adoption referred to in paragraph 2, subparagraph c, FIUs shall implement the requirements laid down in the Annexes into their national reporting systems.
   b. Where not using FIUs' reporting platforms for generating their reports, obliged entities shall implement the requirements laid down in the Annexes into their internal systems within [...] years following the decision of the General Board referred to in paragraph 2, subparagraph b.

### <a id="article-11"></a>Article 11 — Entry into force and application

This Regulation shall enter into force on the twentieth day following that of its publication in the Official Journal of the European Union.

It shall apply from […].

However, Article 3 shall apply from […] and article 4 shall apply from [...].

This Regulation shall be binding in its entirety and directly applicable in all Member States.

Done at Brussels,

For the Commission
The President

### <a id="annexes"></a>Annexes

**Annex I** — [see separate document — Report of suspicions pursuant to Article 3 of this Regulation]

**Annex II** — [see separate document — Transaction records pursuant to Article 4 of this Regulation]
