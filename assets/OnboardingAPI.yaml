alps:
  version: '1.0'
  title: "Onboarding API"
  doc: 
    type: "markdown"
    value: "This is the ALPS document for BigCo's **Onboarding API**"

  descriptor:
    # vocabulary properties
    - id: "identifier" 
      type: "semantic"
      text: "Unique identifier for this record"
      ref: "https://schema.org/identifier"
      
    - id: "companyName" 
      type: "semantic"
      text: "Company's lega; name"
      ref: "https://schema.org/legalName"
    
    - id: "email" 
      type: "semantic"
      text: "Company's primary email account"
      ref: "https://schema.org/email"
      
    - id: "telephone" 
      type: "semantic"
      text: "Company's phone number"
      ref: "https://schema.org/telephone"

    - id: "address"
      type: "semantic"
      text: "Company's business address"
      ref: "https://schema.org/address"
      
    - id: "status" 
      type: "semantic"
      text: "Account status (active inactive suspended)"
      ref: "https://schema.org/status"
      
    - id: "maxValue" 
      type: "semantic"
      text: "Account's maximum spending limit"
      ref: "https://schema.org/maxValue"
      
    - id: "discount" 
      type: "semantic"
      text: "Account's default sales discount (as a percentage)"
      ref: "https://schema.org/discount"

    - id: "division"
      type: "semantic"
      text: "BigCo's department in which the company holds an account"
      ref: "https://schema.org/department"
     
    # reference grouping
    - id: "wip"
      type: "group"
      descriptor: 
        - href: "#identifier"
        - href: "#companyName"
        - href: "#email"
        - href: "#telephone"
        - href: "#status"
        - href: "#maxValue"
        - href: "#discount"

    # actions
    - id: "startOnboarding"
      type: "unsafe"
      rt: "wip"

    - id: "collectCompanyData"
      type: "safe"
      rt: "wip"
      descriptor: 
        - href: "#identifier"
        - href: "#companyName"
        - href: "#address"
        - href: "#email"
        - href: "#telephone"
        - href: "#status"

    - id: "SaveToWIP"
      type: "idempotent"
      rt: "wip"
      descriptor:
        - href: "#identifier"
        - href: "#companyName"
        - href: "#email"
        - href: "#telephone"
        - href: "#status"
        - href: "#maxValue"
        - href: "#discount"

    - id: "collectAccountData"
      type: "safe"
      rt: "wip"
      descriptor:
        - href: "#identifier"
        - href: "#division"
        - href: "#discount"
        - href: "#maxValue"

    - id: "completeOnboarding"
      type: "idempotent"
      rt: "wip"
      descriptor:
        - href: "#identifier"

    - id: "abandonOnboarding"
      type: "idempotent"
      rt: "wip"
      descriptor:
        - href: "#identifier"

    - id: "goHome"
      type: "safe"