# Secure Development Guideline

This guideline is meant to aid developers when writing code, to help “build security in”. 
It is based on some existing company practices as well as generally accepted best practice for
secure development processes. We have taken care to make the guideline technology agnostic where 
possible.

# Secure development principles
Security needs to be built in from the start of the product and follow its lifecycle until the 
end. The key practices we want to follow as developers are:

- Keep user’s personal data safe from prying eyes, including internal eyes. Store the data in a secure way, and ensure that only the information that is required is collected. See Appendix D - GDPR Summary for further requirements on this from the General Data Protection Regulation.
- Treat untrusted resources and data with care. If the software accesses files or information over the internet or other networks, or reads files that have an unknown origin, software must properly sanitize and validate the data. This is in practice always the case.
- Protect data in transit. When information is transmitted over networks, it must be done in a safe and secure way to avoid unauthorized access to or modification of the data while in transit.
- Verify the authenticity of data wherever possible. Perform anomaly checks and verify signatures where they are used.
- Use threat modeling to connect potential security incidents to business impact and credibility. See Appendix A (Threat Modeling) for details on threat modeling.

For each operation on the codebase take care to:

- Avoid exploitable coding flaws by following best practice for development and quality assurance.
- Update your risk model continuously to ensure the potential business impact of an exploit is understood.
- Reuse trusted components and APIs. Software typically becomes more reliable over time – rewriting components that provide validated security features out of the box is almost never a good idea.

**Note**
In this document, "software component" is taken to mean any software artefact that can be reused 
or referenced, such as a library, a class or a function.

How to use this document
This document is meant to serve two purposes:

1. Provide an introduction to secure development practices and the Sportradar approach to security for new hires
2. Be a point of reference for more experienced developers

## Injecting security in the agile workflow
In this section, we focus on the recommended workflow process for developing secure software. 
The methodology described is based on agile project structures and borrows part of its approach 
from a methodology developed for safety critical systems by SINTEF called 
SAFEScrum. It also uses insights from Nicolaysen et. al.<sup>[1](#ref:nicolaysen)</sup>.

![Image](../secdevflow.png?raw=true)

# References and footnotes
<a name="ref:nicolaysen">1</a>: Nicolaysen, T., Sassoon, R., Line, M. B., & Jaatun, M. G. (2012). Agile Software Development: The Straight and Narrow Path. Security-Aware Systems Applications and Software Development Methods, 1

# Appendix A: Threat modeling methodology

