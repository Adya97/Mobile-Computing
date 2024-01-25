**BRING YOUR OWN PAPER & PEN!**  
No MCQs, only open questions  
No "trick" questions; go straight to the point  
No programming challenges

* * *

## Project mgmt: "how to design software from a company perspective?"

- **Requirements analysis**: *understanding organizational / stakeholder needs and objectives*:
    - Identify and prioritize functional and non-functional requirements of the software
    - Document and validate requirements to ensure alignment with the company's strategic objectives
- **Architectural design**:
    - Must align with the company's strategy and scalability requirements
    - Consider data security, integration with already existing systems and potential future expansion possibilities
    - Align with the company's technical stack and long-term vision
- **Implementation**:
    - Must adhere to company's standards and best practice (to ensure maintainability and readability of the codebase)
    - Focus on collaboration among potential multiple dev teams, following **agile** methodologies to adapt to constantly evolving requirements
    - Regularly update stakeholders on the progress and address any emerging issues as soon as they arise
- **Testing**:
    - Implement a comprehensive testing strategy, that covers **unit testing, integration testing** and **system (end-to-end) testing**
    - Develop test cases based on both functional and non-functional requirements to validate software's performance, security & reliability.
    - Conduct UAT (**User Acceptance Testing**) involving key stakeholders, ensuring the software meets company's and end-users' expectations
- **Maintenance and iteration**
    - Plan ongoing maintenance to address bugs, security vulnerabilities, potentially evolving user needs
    - Implement a feedback loop to gather insights from users and stakeholders for continuous improvement
    - Prepare for iterative development cycles to include updates and enhancements, based on company's evolving goals

> Multifaceted process, integrating various PM principles; requires a collaborative and iterative approach, always focusing on the company's strategic objectives.  
> Software design must always be aligned with organizational goals, so PMs can contribute to the successful development and deployment of software contributing to the business

* * *

## Agile project management:

- Iterative and flexible approach to project management
- Prioritizes **adaptability, collaboration** and **customer satisfaction**
- Focus on **continuous improvement** and the ability to **respond to change throughout the entire project's life cycle**
- **Iterative** development: breaking the project into small, manageable units called **iterations** or **sprints**, usually lasting 2-4 weeks each, during which a functional piece of software is developed, tested and delivered
- **Customer collaboration**: involving customers and stakeholders for continuous feedback, ensuring the product meets their expectations; changes can be accomodated at any time during the development process
- **Adaptive** planning: as project requirements may change, plans need to be flexible. Focus on adapting to evolving circumstances (rather than following a rigid, fixed plan)
- **Cross-functional teams**, that includes members with diverse skills necessary for all aspects of the project's development.
- **Continuous delivery and integration**: ensures that code changes are integrated into the main code base regularly, reducing the risks of conflicts and identifying issues early.
- **Open and transparent communication** (daily stand-ups...)
- **Empirical process control**, constantly reflecting performance to adjust processes accordingly; feedback loops are used to measure progress and identify room for improvement.

> Flexibility, collaboration, customer-satisfaction first; iterative, adaptable (response to change) -> Scrum, Kanban methods...

* * *

## QA (Quality Assurance):

A systematic process focused on ensuring that a software {project/product} meets specific quality standards & requirements. Includes activities, methodologies focusing on preventing defects, identifying and fixing issues early on, and ensuring the final deliverables meet user's expectations.

- **Quality planning**: planning the quality standards, processes and metrics for the dev's life cycle, defining a roadmap to maintain / improve the quality of the software throughout the project
- **Requirements analysis**: reviewing & validating the project's requirements to ensure they're clear, complete and testable, in order to identify potential issues early on and ensure alignment between requirements & user expectations.
- **Process audits**: regularly reviewing and auditing dev's processes to ensure compliance with quality standards, identifying and rectifying defined processes, improving consistency & efficiency
- **Test planning & execution**: define a test plan outlining the strategy, test cases and execution schedule. Systematically & continuously verify that the software works as intended, identifying & solving defects before deployment
    - **Automated testing**: implementing automated testing tools & frameworks to execute repetitive and complete test cases; aims at increasing test efficiency, coverage and repeatability, particularly in large-scale projects
- **Defect tracking & management**: track, manage, prioritize defects identified during testing or reported by users, addressing them promptly and efficiently
- **Continuous improvement:** assessing QA regularly to identify areas for potential improvement, enhancing global dev/test processes, leading to higher quality software and more efficient {project/product} delivery
- **User Feedback and Acceptance Testing**: feedback loop from users, incorporating their input into the dev process, aligning with user expectations and real-life scenarios
- **Documentation**: creating comprehensive docs that include test {plans/cases} & QA processes, providing a clear ref. to stakeholders and ensuring transparency in QA activities
- **Collaboration & Communication**: fostering efficient comm/collab among teams (dev, testers, PMs...), minimizing misunderstandings, addressing issues promptly, ensuring a cohesive approach to the quality of the project

> Multifacet process including planning, testing, defect management and continuous improvement for high-qual. software delivery that meets user expectations, adheres to specific requirements and is free of critical defects.

* * *

## Whitepaper skeleton:

*Explaining the "structure" / "construction" of a product (bigger picture), rather than just the backbone code*

- Provides the **value of a software** as an asset of an IT company
- Describes the **purpose** of the application, helps to understand the software in general
- Structure: is made of **components**, **activities**, a **layout** and **interfaces**
- **Testing** (of *components*):
    - **Unit tests**: ensures the quality of a single component
    - **Integration tests**: tests the integration of the components
    - **End-to-end tests**: starts from the beginning (GUI), tests if **all use-cases** are indeed working -> most challenging, final part

### Software pieces:

- **Components**:
    
    - Modular, reusable and self-contained pieces of software, encapsulating a set of functionalities
    - Independent, allowing for easy maintenance, testing and scalability
    - Interoperability: they communicate with each other through **interfaces**, facilitating the development of complex systems from independently developed components
- **Interfaces**:  
    Serve as a **contract** defining a set of methods/functionalities that a class/component must integrate. Establishes communication boundary between components, allowing them to interact without exposing the detail of their implementation.
    
    - Abstract the implementation details, provide a clear, standardized way for components to communicate
        
        > Example (in Python): a basic interface for a data storage component might include methods like `read()`, `write()` and `delete()`.
        
    - Enforce a "contract" ensuring that classes/components implementing them adhere to a specific set of rules/functionalities
        
        > Example: class(es) implementing an interface for a database connection component should provide methods such as `connect()`, `query()`, `disconnect()`
        
    - A class can implement multiple interfaces, inheriting and providing implementations for various functionalities.
        
        > Example: a cloud storage service class could implement interfaces for file management AND authentication, so that class could integrate with multiple part of the global system.
        
    - **Loosely coupling** components; interfaces allow them to evolve independently without affecting each other's internal design.
        
        > Ex.: for a user authentification component, interfaces would be `login()`, `logout()`. Other components could interact with this interface without needing to know how the authentication process is implemented internally.
        
    - **Scalability / maintainability**: interfaces enhance the scalability/maintainability of a system software, providing a structured and standardized way for components to communicate.
        
        > Ex.: in a system with various data processing components, each component should adhere with a common data processing interface, facilitating the addition of new components or the replacement / improvement of existing ones, without disrupting the way the system works overall.
        
    - **Provided** interfaces: refer to the **set of functionalities/methods that a class/component make available to other classes/components**. They define what services/operations a class can offer to the external parts of the system.
        - Implemented by classes, that provide concrete implementation of the methods declared in the interface. The interface represents the *"outgoing"* contract specifying what other parts of the software can expect from the class.
            
            > Ex.: a `DatabaseConnection` class providing methods like `connect()`, `disconnect()` and `query()`; these methods collectively form the provided interface of the `DatabaseConnection` class.
            
    - **Required** interfaces: refer to the **set of functionalities/methods that a class need to function properly**. Defines the expectations a class has from other classes/components it interacts with.
        - When a class depends on a required interface, it implies that it relies on other classes to provide specific functionalities through that interface. The class using that *required* interface expects certains behaviors from the classes that implement it.
            
            > Ex.: `PaymentProcessor` class requires a `PaymentGateway` interface, with methods such as `processPayment()`, `refundPayment()`. This class depends on the presence of these methods in the class that implements the `PaymentGateway` interface.
            
    - Classes with **provided interfaces** collaborate with classes having **required interfaces** to achieve specific functionalities. Allows for building complex systems by connecting different classes with compatible interfaces.
    
    - **Loose coupling** between classes; a class can **change its internal implementation without affecting the classes depending on its/their provided interface(s)** *(as long as the interface remains consistent)*
    
    > Ex.: If a `PaymentProcessor` class requires a `PaymentGateway` interface and various classes (like `CreditCardGateway` and `PayPalGateway`) implement this interface, the `PaymentProcessor` class remains unaffected by changes in the internal implementations of these gateway classes.
    

> All in all, **interfaces play a crucial role in software design by facilitating modularization, encapsulation and flexibility**. They enable devs to build scalable and maintainable systems while promoting code re-usage and separation of concerns. Allows to create robust and adaptable solutions.

- **Components diagram**: UML *(Unified Modeling Language)* diagram used to illustrate the organization of components and their relationships within a system; provides a visual representation of how components interact to form a coherent software architecture
    
    - Includes **components**, **provided and required interfaces**, **dependencies between components**, and **association relationships.**
- **Artifacts**: tangible deliverables produced during various stage of the software development life-cycle. Capture essential info about design, implementation, testing and maintenance of the system.
    
    - Requirements document
    - Design documents: detail the architecture, components specs and system design of the software; aims at guiding devs in the implementation process
    - Components specs: specify the functionalities, interfaces and interactions of individual software components
    - Codebase
    - Test cases / plans: outline test cases, scenarios and plans for checking the functionality of the software
    - Components diagram
    - User manuals: documentation for end-users
    - Change requests: modifications / additions to the software after the initial development phase
    - Project plans: schedules, milestones, resource allocation
    - Release notes: changes, enhancement, bug fixes summaries of a specific software release

> Wide range of docs and deliverables contributing to planning, design, implementation, testing and maintenance of a software. Valuable tools for communication, collaboration and documentation throughout the software's dev. life-cycle.

* * *

## Writing use-cases based on specific user-scenarios:

- Development process should revolve around meeting the needs & expectations of end-users
- Use-cases provide a clear understanding of how different components of an IT system should work together to deliver the desired functionalities from an user-perspective
- Communication & Collaboration: use-cases serve as a communication tool between stakeholders (PMs, devs, testers & designers); provide a common/shared understanding of the expected behavior of the system
- Form basis for test-case development (end-to-end testing) that align on real-world user scenarios, contributing to the overall QA process
- Scope definition: by identifying and detailing user scenarios, use-cases help defining the scope of the project, making it clear what needs to be developed to meet user requirements  
      
    
- User personas: define what types of users will interact with the system
- Anticipate different user behaviors, include alternate paths; helps addressing potential edge cases
- Connect user stories with stakeholders, making sure the use-cases scenarios meet their expectations and requirements
- Iterative process: as the project progresses, revisit and update use-cases based on evolving requirements & feedback loop  
      
    
- Example Use-Case:

**Use-Case Title:** User Authentication  
**Scenario:**

1.  Actor: Registered User
2.  Goal: Log in to the system to access personalized content.
3.  Main Flow:
    - User enters username and password.
    - System validates credentials.
    - If credentials are valid, the system grants access and displays the user's dashboard.
4.  Alternate Flow:
    - If credentials are invalid, the system displays an error message, prompting the user to retry.

* * *

## Cryptography topics:

- **Private/public keys**:
    
    - Key pair: a pair of two mathematically connected keys; private a public one.  
        Private key is kept secret and known only to the owner, while the public one can be shared openly with anyone.
    - Encryption/decryption (**cipher**): data encrypted with a public key can be decrypted with the corresponding private key, **and vice-versa**. Is the basis of asymmetric cryptography; provides a secure way for two parties to communicate without needing to share a secret key. **Only secure way to exchange keys is in person** to avoid *man-in-the-middle attacks* (describe above) -> **PKI** (Public Key Infrastructure)
- Algorithms:
    
    - Asymmetric: **RSA** {2048 / 4096}
    - Symmetric (Caesar's Cipher, Vigenère): **AES**.  
        Less time/resource consuming, but just a **single key** for both parties
    
    > If Alice wants to send a confidential msg to Bob, she uses Bob's public key to encrypt the message; only Bob, with his private key, should be able to decrypt and read the message.
    
- **Certificates**:
    
    - **Certificate Authorities** (CAs): 3rd-party entities (Let's Encrypt, DigiCert, Symantec...) that issue **digital certificates**.  
        Those **verify the ownerwship of public keys**, associating it with the certificate holder.
        
    - **Digital Signatures**: cryptographic techniques to verify the authenticity of a message/document.  
        The sender **uses his private key to create a digital signature** (via a **hash function** - MD5 function for example), and the recipient **uses the sender's public key to verify it** (its validity) by **verifying it** (also done with a hash function - both hash values must be the exact same ones).  
        These certificates can have an *expiration date*.  
        ![39a9d23488a0b710c60ba8e3a06c9a28.png](:/9c2e8a6e60de4e1faecef35cca5fed1b)
        
    - Mallory (**Man-in-the-Middle**):
In the *Alice&Bob* scenario, Mallory is a malicious actor that would intercept and alter communication between two parties without their approval / knowledge.  
It may look (eavesdropping - *"Eve"*) or modify messages, or even impersonate one of the parties (Alice or Bob), compromising the security of the communication.  
The whole point of encryption and authentication is to **mitigate the risk of Man-in-the-Middle attacks**.  
Secure (*encrypted*) communication protocols (such as HTTPS/TLS/SSL) are designed to protect against this kind of threats.

* * *

## Blockchain topic:
- Refer to the prof's slides and most importantly, **read the [Bitcoin Whitepaper](https://bitcoin.org/bitcoin.pdf)!**
