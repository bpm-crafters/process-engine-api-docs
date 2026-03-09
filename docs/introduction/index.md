## Why we did it?

The motivation for this project arises from recent shifts in the process automation market. With the release of Camunda 8, a new API was introduced that differs
significantly from Camunda 7. At the same time, the end-of-life (EoL) for Camunda 7 Community and Enterprise versions have been announced, prompting many
organizations to re-evaluate their long-term strategies.

This situation has led to the emergence of several Camunda 7 forks, such as CIB7 and Operaton, alongside established alternatives like Flowable. Many of our
customers are now navigating these changes and seeking ways to adapt their solutions without being locked into a single vendor's evolution path. Our goal is to
provide a stable foundation amidst these developments.

## What is our vision?

We envision a future where process application developers can focus on delivering business value without being burdened by the complexities of vendor-specific
APIs. By providing a vendor-independent Process Engine API, we address the current uncertainty among customers and allow them to delay final technology
decisions until they are truly necessary.

Our approach enables organizations to combine several process automation technologies while remaining uniform towards the business application. By
applying better architectural patterns learned from years of experience, we aim to significantly raise the quality of software.

Ultimately, we aim to simplify the integration of process engines into applications, ensuring that developers can choose the best-suited engine for their
needs without sacrificing flexibility or portability. Our goal is to empower developers to build robust, scalable, and future-proof process applications
that are resilient to changes in underlying technology.

## What is our suggestion?

Instead of learning and using of vendor-specific APIs to build your process applications, you should focus on delivering business value. Construction
of scalable, robust and future-proof applications is straightforward, if system components are designed to fulfill clear goals and have clear responsibilities.
This kind of architecture is called [Clean architecture](clean-architecture.md), and we propose to follow it in general situations. In doing so, technology is
hidden inside adapters, and the business and domain logic stays technology-agnostic and independent.

## Is there more?

Beyond simple abstraction, we offer unique added value designed to address common real-world challenges in process automation. Our solution focuses on:

- **Seamless data handling**: Effortlessly manage complex data access and conversion scenarios, ensuring your business logic remains clean and efficient.
- **Scalable process landscapes**: Build large-scale, enterprise-ready process architectures with ease, utilizing centralized components like unified user task management.
- **Resilient distributed environments**: Tackle the inherent complexities of distributed systems, including fault tolerance and transactional consistency, with robust, built-in patterns.
