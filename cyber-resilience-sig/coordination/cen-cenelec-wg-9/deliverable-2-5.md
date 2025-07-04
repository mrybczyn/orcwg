---
SIG: Cyber Resilience SIG
Document Type: Deliverable
Number: 2.5
Status: 🚀 Submitted
Group: CEN/CENELEC WG 9
Subgroup: PT 1
Date: 2025-06-12
---

# Comments to CEN/CENELEC PT 1 Standard

## Request

As part of its process, CEN/CENELEC WG 9 PT 1 requested comments on its [Horizontal standard on General principles for cyber resilience (JT013089)][JT013089] from its working group participants (note this was not a public call for comments).

## Goals

1. Prevent the open source ecosystem from having to purchase standards to comply to the CRA
    * Prevent requirements placed on stewards, open source projects, and maintainers in CEN/CENELEC standards as these standards aren't freely available.
2. Avoid placing unnecessary demands on the open source ecosystem
    * Prevent requirements placed on manufacturers that rely on stewards, open source projects, or maintainers performing certain actions they have no obligations to perform.
    * Prevent requirements that might lead manufacturers to expect the same interactions with stewards, open source projects, or  maintainers as they have with their suppliers.
3. Maintain a leveled playing field
    * Prevent requirements placed on manufacturers which unfairly favor proprietary software (such as mandating security by obscurity, for example).
4. Maintain Europe's ability to leverage open source
    * Prevent requirements that unreasonably burden manufacturers integrating open source components.

## Comments

We identified two sections of the [Horizontal standard on General principles for cyber resilience (JT013089)][JT013089] that were concerning given the goals stated above and submitted comments for them:

**Clause 5.5** describes a required consultation process when integrating third-party components, including open source software, that would require manufacturers to build a 1:1 relationship with open source maintainers in order to integrate open source components.

**Clause 6.12** essentially describes due diligence requirements for third-party components and includes a number of requirements that are concerning given the above-mentioned goals.

We submitted [our comments](./eclipse-foundation-JT013089-comments.docx) on June 12, 2025 using the requested docx template.

<details>
   <summary>See detaileds comments</summary>

| Line number | Clause / Subclause | Paragraph / Figure / Table | Type of comment | Comments | Proposed change |
|---|---|---|---|---|---|
| 332 | 5.5 | | ge | There are no requirements on open source maintainers nor on open source software stewards to engage in consultations with their users. Open source projects might provide information that helps integrators exercise due diligence, and there even might be a security attestation program in the future facilitating this further, but that is the extent of the information integrators should expect. Clause 5.5 needs to reflect this reality and cannot assume a two-way consultation between open source projects and the integrators. | Be upfront that neither open source maintainers nor open source software stewards are relevant stakeholders in this consultation process, and that when integrating open source components integrators must rely on other stakeholders to carry out this assessment. Alternatively, exempt open source components from this process altogether or define a specific process for the integration of open source components. Additionally, note that when integrating open source components, integrators might need to carry out this assessment throughout the component's dependency tree, as they cannot rely on a supplier for having carried out this due diligence for them. |
| 1097 | 6.12.2 | | te | Not all of the documents outlined in 5.5.4 are relevant (or even possible to obtain) for open source components. | This paragraph should be updated to reflect the expected output of 5.5.4 for open source components. |
| 1101 | 6.12.3 | | te | Open source components might not state their intended purpose. | Limit the requirement to fitness for purpose. |
| 1104 | 6.12.3 | | te | It might be entirely feasible to assess that a component meets risk-based requirements without having to assess the process used to arrive at that result. This is particularly true for open source components whose code is open and easily auditable by the manufacturer. | Assessing that third-party components <del>has been designed, developed and produced in such a way that they</del> ensure an appropriate level of cybersecurity based on the risks. |
| 1106 | 6.12.3 | | ge | Unclear what part of clause 5 this requirement implies. | Please be more specific about what part of the risk assessment this clause is referring to. |
| 1108 | 6.12.3 | | ge | Open source components do not have a supplier. Make sure that this doesn’t exclude properly documented open source components. | Integrating the component according <ins>to </ins>the instructions of the component<del>s supplier</del> and treating integration related risks; |
| 1111 | 6.12.3 | | ge | Open source components do not have a supplier. Make sure that this doesn’t exclude properly documented open source components. | Providing measures for maintaining the components cybersecurity based on the instructions of the component<del>s supplier</del>, e.g. vulnerability handling and incident management. |
| 1116 | 6.12.3 | | te | Clarify that implementing controls also apply to open source components and that relevant industry best practices should be used in that case (as these might differ from closed source components). | Implementing appropriate cybersecurity controls, based on the risk and considering, but not limited to integrity, confidentiality, authentication, encryption and traceability based on <ins>relevant </ins>industry best practices for third-party components <ins>including commercial, free and open-source components </ins>and services used in the product. |
| 1117 | 6.12.3 | | te | Open source components don’t necessarily provide end-of-life information. | Account for lack of information on EOL in open source components. |
| 1122 | 6.12.3 | | ge | Requirement is ambiguous about whether the audits should target the manufacturer’s product itself or every single component and their dependencies individually. Clarify that the audits are focused on the product itself. | Ensuring audit activities <ins>of the product with digital elements </ins>and procedures to address cybersecurity risks of third-party components and services. |
| 1125 | 6.12.3 | | te | Clarify what kind of monitoring is expected. | |
| 1125 | 6.12.3 | | te | Manufacturers routinely include thousands of open source components in their products, the large majority of which do not provide lifecycle information. This requirement would not be reasonably fulfillable. Suggest adapting to industry best practices once the nature of the requirement is clarified per previous comment. | Clarify requirements and adapt it to industry best practices for integrating open source components. |
   
</details>

At a high-level, our comments centered around the folllowing four concerns:

### 1. Incorrect assumption that manufacturers should expect similar relationships with open source maintainers and stewards as they have with commercial suppliers

The standard operates from the perspective that every component has a supplier that manufacturers are expected to have a direct contractual relationship with. That’s particularly obvious in clause 5.5 which requires a "consultation" to happen between manufacturer and supplier notably leading to "documentation containing agreement to responsibility distribution" (5.5.4).

Open source maintainers and stewards are not suppliers for the software they provide for free.

As the CRA recognizes, there are no requirements on open source maintainers nor on open source software stewards to engage in consultations with users of their software, nor to provide documentation beyond what is required of stewards in Article 24(1). Manufacturers shouldn't be led to believe that this is the case, as it will cause already overburdened open source maintainers to have to field consultation requests from well-meaning manufacturers or deal with demands for responsibility distribution instead of focusing on securing their software. Open source projects might make freely available information that helps manufacturers exercise due diligence, and a future security attestation program might facilitate this further (possibly for a fee), but that is the extent of the relationship manufacturers should expect. The standards need to reflect this reality and should not expect open source maintainers or stewards to enter into a direct relation with the manufacturers that chose to integrate their software.

### 2. Incorrect assumption that open source maintainers and stewards exercise due diligence of their own dependencies

Because of the incorrect assumption that open source maintainers and stewards are suppliers, the standard implicitly assumes that open source maintainers and stewards are required to exercise due diligence for their own dependencies as if they were themselves manufacturers. Of course, this isn't the case as neither open source maintainers nor stewards are subject to due diligence obligations. Manufacturers will need to exercise their due diligence requirements for both their open source components, and the dependencies of those components, recursively. In particular, the second part of Clause 6.12.3, is focused on the requirements of manufacturers to the components themselves, and doesn't seem to consider that manufacturers are responsible for the dependencies of those components and the dependencies of those dependencies, recursively. Concretely, dependencies of open source components might require different treatment of associated risks, different controls, dedicated monitoring and review procedures, etc. than the components themselves. The standards need to reflect the reality of the recursive component structure of open source software and acknowledge that the responsibility of manufactures extends across that whole supply chain and not just to the layer that is directly visible to them.

### 3. Requirements for third-party components doesn't account for the security benefits of open source transparency
Contrary to industry best practices, section 6.12.3 treats all components the same regardless of whether or not they are open source. As open source components can be easily audited by manufacturers or third parties due to the transparency of their codebases, manufacturers can independently assess their fitness for purpose, the presence of appropriate controls, the security of the code base, etc. regardless of how they were developed or what documentation is provided. The transparency of open source provides security guarantees that the industry understands and knows how to leverage. By failing to account for this, the standard is making it unreasonably difficult for manufacturers to leverage open source. The standards should acknowledge the security benefits provided by open source transparency and account for industry best practices for consuming open source software in the requirements it specifies.

### 4. Pass/fail structure of requirements risk dis-incentivising investments in open source security
The pass/fail structure of the first section of 6.12.3, means that the vast majority of open source projects will fall to the second part of the section regardless of any improvements they might be able to make to their security posture. If improving the security of open source projects doesn't lighten the compliance burden of manufacturers integrating them (or only does so marginally), this risks dis-incentivising investments from said manufacturers to improve the security of the open source projects they rely on. The standards should consider open source components specifically and take care not to dis-incentivize investments to improve their security postures, as more cyber resilient open source components directly benefit EU citizens and businesses.

## Acknowledgments

The following people have contributed to this document either directly or indirectly (e.g. by raising questions):

Juan Rico,
Lars Francke,
Timo Perälä,
and Tobie Langel.

If you have contributed to this document and aren't properly acknowledged or if you want to edit or remove your name, please let us know by [opening an issue](https://github.com/orcwg/orcwg/issues/new) and we will fix this right away.

[CEN/CENELEC WG 9 PT 1]: ../#cen-cenelec-wg-9
[JT013089]: https://github.com/orcwg/cra-hub/blob/main/standards.md#milestone-1---horizontal-standards-due-august-30-2026
