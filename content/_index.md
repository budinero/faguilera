---
# Leave the homepage title empty to use the site title
title: ''
date: 2024-01-10
type: landing

sections:
  - block: about.biography
    id: about
    content:
      title: Biography
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin
  - block: markdown
    id: SkillsN
    content:
      title: Skills
      subtitle: '[Wider list](https://www.linkedin.com/in/facundoaguilera/details/skills/)'
      text: |2- 
        | **Software** | **Languages** | **Soft**  | 
        |----------|----------|----------|
        | MATLAB/Simulink      | C         | Problem-solving   |  
        | Code Coposer Studio  | C++       | Teamwork  |  
        | Vivado               | Qt        | Teaching  |
        | Git                | VHDL/Verilog | Critical thinking  |  
       
         
      design:
       columns: '1'
 # - block: skills
 #   content:
 #     title: Skills
 #     text: ''
      # Choose a user to display skills from (a folder name within `content/authors/`)
 #     username: admin
 #   design:
 #     columns: '2'
  - block: experience
    content:
      title: Experience
      # Date format for experience
      #   Refer to https://docs.hugoblox.com/customization/#date-format
      date_format: Jan 2006
      # Experiences.
      #   Add/remove as many `experience` items below as you like.
      #   Required fields are `title`, `company`, and `date_start`.
      #   Leave `date_end` empty if it's your current employer.
      #   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
      items:
        - title: Assistant Researchr
          company: CONICET
          company_url: 'https://iitema.conicet.gov.ar/gea/'
          company_logo: ''
          location: Río Cuarto, Córdoba, Argentina
          date_start: '2018-11-01'
          date_end: ''
          description: |2-
              Research topics include:
              * Fault tolerant electric traction drives
              * Energy management in electrical microgrids
              
              Responsibilities include:
              * Applied research: theory, hardware implementation, validation and publication
              * Research project management
              * Supervision of postgraduate and undergraduate students
        - title: Professor of Programmable Logic Device, Digital Signal Processing and Control
          company: Universidad Nacional de Río Cuarto
          company_url: 'https://www.ing.unrc.edu.ar'
          company_logo: 
          location: Río Cuarto, Córdoba, Argentina
          date_start: '2015-05-01'
          date_end: ''
          description: |2-
            Programs in which I am involved:
              * Doctorate in Engineering Sciences
              * Electrical Engineering    
              * Telecommunications Engineering
    design:
      columns: '2'
  #- block: accomplishments
  #  content:
      # Note: `&shy;` is used to add a 'soft' hyphen in a long heading.
  #    title: 'Accomplish&shy;ments'
  #    subtitle:
      # Date format: https://docs.hugoblox.com/customization/#date-format
  #    date_format: Jan 2006
      # Accomplishments.
      #   Add/remove as many `item` blocks below as you like.
      #   `title`, `organization`, and `date_start` are the required parameters.
      #   Leave other parameters empty if not required.
      #   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
  #    items:
  #      - certificate_url: https://www.coursera.org
  #        date_end: ''
  #        date_start: '2021-01-25'
  #        description: ''
  #        icon: coursera
  #        organization: Coursera
  #        organization_url: https://www.coursera.org
  #        title: Neural Networks and Deep Learning
  #        url: ''
  #      - certificate_url: https://www.edx.org
  #        date_end: ''
  #        date_start: '2021-01-01'
  #        description: Formulated informed blockchain models, hypotheses, and use cases.
  #        icon: edx
  #        organization: edX
  #        organization_url: https://www.edx.org
  #        title: Blockchain Fundamentals
  #        url: https://www.edx.org/professional-certificate/uc-berkeleyx-blockchain-fundamentals
  #      - certificate_url: https://www.datacamp.com
  #        date_end: '2020-12-21'
  #        date_start: '2020-07-01'
  #        description: ''
  #        icon: datacamp
  #        organization: DataCamp
  #        organization_url: https://www.datacamp.com
  #        title: 'Object-Oriented Programming in R'
  #        url: ''
  #  design:
  #    columns: '2'
  - block: collection
    id: posts
    content:
      title: Recent Posts
      subtitle: ''
      text: ''
        # Choose how many pages you would like to display (0 = all pages)
      count: 5
        # Filter on criteria
      filters:
        folders:
          - post
        author: ""
        category: ""
        tag: ""
        exclude_featured: false
        exclude_future: false
        exclude_past: false
        publication_type: ""
      #  Choose how many pages you would like to offset by
      offset: 0
      Page order: descending (desc) or ascending (asc) date.
      order: desc
    design:
        # Choose a layout view
      view: compact
      columns: '2'
  #- block: portfolio
  #  id: projects
  #  content:
  #    title: Projects
  #    filters:
  #      folders:
  #        - project
  #    # Default filter index (e.g. 0 corresponds to the first `filter_button` instance below).
  #    default_button_index: 0
  #    # Filter toolbar (optional).
  #    # Add or remove as many filters (`filter_button` instances) as you like.
  #    # To show all items, set `tag` to "*".
  #    # To filter by a specific tag, set `tag` to an existing tag name.
  #    # To remove the toolbar, delete the entire `filter_button` block.
  #    buttons:
  #      - name: All
  #        tag: '*'
  #      - name: Deep Learning
  #        tag: Deep Learning
  #      - name: Other
  #        tag: Demo
  #  design:
  #    # Choose how many columns the section has. Valid values: '1' or '2'.
  #    columns: '1'
  #    view: showcase
  #    # For Showcase view, flip alternate rows?
  #    flip_alt_rows: false
  #- block: markdown
  #  content:
  #    title: Gallery
  #    subtitle: ''
  #    text: |-
  #      {{< gallery album="demo" >}}
  #  design:
  #    columns: '1'
  #- block: collection
  #  id: featured
  #  content:
  #    title: Featured Publications
  #    filters:
  #      folders:
  #        - publication
  #      featured_only: true
  #  design:
  #    columns: '2'
  #    view: card
  #
  - block: collection
    id: publications
    content:
      title: Recent Publications
      text: |-
        {{% callout note %}}
        Quickly discover relevant content by [filtering publications](./publication/).
        {{% /callout %}}
      filters:
        folders:
          - publication
        exclude_featured: true
    design:
      columns: '2'
      view: citation
  #- block: collection
  #  id: talks
  #  content:
  #    title: Recent & Upcoming Talks
  #    filters:
  #      folders:
  #        - event
  #  design:
  #    columns: '2'
  #    view: compact
  #- block: tag_cloud
  #  content:
  #    title: Popular Topics
  #  design:
  #    columns: '2'
  - block: contact
    id: contact
    content:
      title: Contact
      subtitle:
      text: ''
      # Contact (add or remove contact options as necessary)
      email: gea@gmail.com
      phone: +54 0358 4676255 / +54 9358 5084033
      appointment_url: ''
      address:
        street: Ruta Nac. 36 - Km. 601
        city: Río Cuarto
        region: Córdoba
        postcode: 'X5804BYA'
        country: Argentina
        country_code: AR
      directions: Grupo de Electrónica Aplicada, Facultad de Ingeniería, Universidad Nacional de Río Cuarto
      #office_hours: 
      #  - 'Monday to Friday 8:00 to 20:00 (CMT-3)'  
      # Choose a map provider in `params.yaml` to show a map from these coordinates
      coordinates:
        latitude: '-33.111632'
        longitude: '-64.300459'  
      contact_links:
        - icon: whatsapp
          icon_pack: fab
          name: WhatsApp
          link: 'https://web.whatsapp.com/send?phone=5493585084033'
      # Automatically link email and phone or display as text?
      autolink: true
      # Email form provider
      form:
        provider: ''
        formspree:
          id:
        netlify:
          # Enable CAPTCHA challenge to reduce spam?
          captcha: true
    design:
      columns: '2'
---
