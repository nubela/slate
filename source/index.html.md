---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - python

search: true

---

# Proxycurl

Proxycurl is a distributed crawling service that helps to circumvent most (if not all) rate-limiting techniques employed by complex websites.



## Proxycurl

**Rate limit**

There is no rate limit to our API.



**Authentication**

Proxycurl's API uses bearer tokens to authenticate users. Each user is assigned a randomly generated secret key under the [API section in the dashboard](https://nubela.co/proxycurl/dashboard).



The bearer token is injected in the `Authorization` header

```python
import requests

api_endpoint = 'https://nubela.co/proxycurl/api/v2/linkedin'
linkedin_profile_url = 'https://www.linkedin.com/in/williamhgates'
api_key = 'YOUR_API_KEY'
header_dic = {'Authorization': 'Bearer ' + api_key}

response = requests.get(api_endpoint,
                        params={'url': linkedin_profile_url},
                        headers=header_dic)
```



**Credits**

Each valid request requires at least `1` credit to be processed. A credit is consumed if and only if the request returns successfully.

A success request is a request that returns with a `200` HTTP status code.



## Linkedin Person Profile API



```python
import requests

api_endpoint = 'https://nubela.co/proxycurl/api/v2/linkedin'
linkedin_profile_url = 'https://www.linkedin.com/in/williamhgates'
api_key = 'YOUR_API_KEY'
header_dic = {'Authorization': 'Bearer ' + api_key}

response = requests.get(api_endpoint,
                        params={'url': linkedin_profile_url},
                        headers=header_dic)
```



`GET https://nubela.co/proxycurl/api/v2/linkedin`



**URL Parameters**

| Parameter | Required | Description                                                  | Input                | Example                                       | Default value |
| --------- | -------- | ------------------------------------------------------------ | -------------------- | --------------------------------------------- | ------------- |
| `url`     | yes      | URL of the Linkedin Profile to crawl. URL should be in the format of `https://www.linkedin.com/in/<unique_li_id>` | Linkedin Profile URL | `"https://www.linkedin.com/in/williamhgates"` |               |
| `src`     | no       | Includes the raw HTML source code that is fetched and parsed | The string "include" | `include`                                     | N/A           |

### Response




```json
{
 'accomplishment_courses': [],
 'accomplishment_honors_awards': [{'description': 'Nanyang Scholarship '
                                                  'recognizes students who '
                                                  'excel academically, '
                                                  'demonstrate strong '
                                                  'leadership potential, and '
                                                  'possess outstanding '
                                                  'co-curricular records.\n',
                                   'issued_on': {'day': None,
                                                 'month': None,
                                                 'year': 2015},
                                   'issuer': 'Nanyang Technological University',
                                   'title': 'NANYANG Scholarship'},
                                  {'description': 'Awarded to students with '
                                                  'exceptional results in '
                                                  'Physics and Mathematics',
                                   'issued_on': {'day': None,
                                                 'month': None,
                                                 'year': 2015},
                                   'issuer': 'Defence Science & Technology '
                                             'Agency',
                                   'title': 'Young Defence Scientist Programme '
                                            '(YDSP) Academic Award'},
                                  {'description': 'An annual competition to '
                                                  'encourage the study and '
                                                  'appreciation of Physics as '
                                                  'well as highlight Physics '
                                                  'talent.',
                                   'issued_on': {'day': None,
                                                 'month': None,
                                                 'year': 2012},
                                   'issuer': 'Institute of Physics Singapore',
                                   'title': 'Singapore Junior Physics Olympiad '
                                            '(Main Category) Honourable '
                                            'Mention'},
                                  {'description': 'Certificate awarded to '
                                                  'student who topped the '
                                                  'cohort in all aspects of '
                                                  'Science.',
                                   'issued_on': {'day': None,
                                                 'month': None,
                                                 'year': 2010},
                                   'issuer': 'Xinmin Secondary School',
                                   'title': 'Certificate of Excellence - Top '
                                            'in Science'},
                                  {'description': None,
                                   'issued_on': {'day': 1,
                                                 'month': 9,
                                                 'year': 2018},
                                   'issuer': 'Nanyang Technological University',
                                   'title': "Dean's List FY17/18"},
                                  {'description': 'This competition requires '
                                                  'students to construct a '
                                                  'model car powered on '
                                                  'chemicals. \n'
                                                  'The car which moves closest '
                                                  'to the set distance (at '
                                                  'least 10m) will win the '
                                                  'competition.\n'
                                                  'Students will need to apply '
                                                  'scientific principles in '
                                                  'order to design the car and '
                                                  'find out how much chemicals '
                                                  'to use for each set '
                                                  'distance.',
                                   'issued_on': {'day': None,
                                                 'month': None,
                                                 'year': 2011},
                                   'issuer': 'Ngee Ann Polytechnic',
                                   'title': 'Ngee Ann Polytechnic Chemical '
                                            'Powered Car Competition Champion'},
                                  {'description': 'https://devpost.com/software/affilichain\n'
                                                  '\n'
                                                  'Disrupting a USD$6 billion '
                                                  'affiliate marketing '
                                                  'industry by cutting '
                                                  'middlemen and replacing '
                                                  'them with a '
                                                  'BlockChain-based payment '
                                                  'platform.\n'
                                                  '\n'
                                                  '- B2B distributed and '
                                                  'permissions database '
                                                  'between affiliates and '
                                                  'merchants for consistency '
                                                  'in records\n'
                                                  '\n'
                                                  '- reduce processing and '
                                                  'verification time of '
                                                  'transactions\n'
                                                  '\n'
                                                  '- fraud detection (e.g. '
                                                  'Resellers)',
                                   'issued_on': {'day': None,
                                                 'month': 10,
                                                 'year': 2017},
                                   'issuer': 'iNTUition + BlackRock',
                                   'title': 'iNTUition 2017 Hackathon - Best '
                                            'Financial Hack'}],
 'accomplishment_organisations': [],
 'accomplishment_patents': [],
 'accomplishment_projects': [{'description': 'For Course CZ1003 - Introduction '
                                             'to Computational Thinking\n'
                                             '\n'
                                             "Built a food (NTU's McDonald) "
                                             'pre-ordering Telegram bot that '
                                             'incorporates Payment using '
                                             'Telegram API. Topped the cohort '
                                             'of more than 100 teams.\n'
                                             'Language used: Python, MySQL\n'
                                             'Server used: Heroku, Raspberry '
                                             'Pi3\n'
                                             '\n'
                                             'Adrian Goh JW (Me) - Software '
                                             'Developer\n'
                                             'Loh Zhen Guang - Product '
                                             'Testing\n'
                                             'Zachary Tan, Er Jia Chin - '
                                             'Documentation',
                              'ends_at': {'day': None,
                                          'month': 10,
                                          'year': 2017},
                              'starts_at': {'day': None,
                                            'month': 8,
                                            'year': 2017},
                              'title': "MaiDanLiao - NTU McDonald's "
                                       'Pre-ordering Telegram Bot',
                              'url': None}],
 'accomplishment_publications': [],
 'accomplishment_test_scores': [{'date_on': {'day': None,
                                             'month': 9,
                                             'year': 2012},
                                 'description': 'Higher Mother Tongue (A2)\n'
                                                'Elementary Mathematics (A1)\n'
                                                'Advanced Mathematics (A1)\n'
                                                'Physics (A1)\n'
                                                'Chemistry (A1)\n'
                                                'Combined Humanities (Social '
                                                'Studies and Geography) (A1)',
                                 'name': 'GCSE O Level',
                                 'score': '3'},
                                {'date_on': {'day': None,
                                             'month': 11,
                                             'year': 2014},
                                 'description': 'H1 General Paper (C)\n'
                                                'H2 Mathematics (A)\n'
                                                'H2 Chemistry (A)\n'
                                                'H2 Physics (A)\n'
                                                'H2 Economics (A)\n'
                                                'H1 General Paper (A)',
                                 'name': 'GCE A Level',
                                 'score': '87.5/90'}],
 'birth_date': None,
 'certifications': [{'authority': 'SMU - Singapore Management University',
                     'display_source': None,
                     'ends_at': None,
                     'license_number': None,
                     'name': 'Citi-SMU Financial Literacy Programme for Young '
                             'Adults',
                     'starts_at': {'day': None, 'month': 6, 'year': 2013},
                     'url': None},
                    {'authority': 'QLC',
                     'display_source': 'google.com',
                     'ends_at': None,
                     'license_number': None,
                     'name': 'Business Development',
                     'starts_at': {'day': None, 'month': 12, 'year': 2017},
                     'url': 'https://docs.google.com/document/d/1E-gm2qUkZtw8MmCj3BAojdBvdsqSMaRgnwRyKacIjmM/edit?usp=drivesdk.'}],
 'city': None,
 'country': 'sg',
 'country_full_name': 'Singapore',
 'education': [{'degree_name': 'O Level',
                'description': None,
                'ends_at': None,
                'field_of_study': None,
                'school': [],
                'starts_at': None},
               {'degree_name': 'High School',
                'description': None,
                'ends_at': None,
                'field_of_study': 'Physics, Chemistry, Mathematics, Economics',
                'school': [],
                'starts_at': None},
               {'degree_name': 'Bachelor’s Degree',
                'description': 'NANYANG Scholarship\n'
                               'iNTUition 2017 Hackathon - Best Financial '
                               'Award '
                               '(https://devpost.com/software/affilichain)',
                'ends_at': None,
                'field_of_study': 'Computer Science with Minor in Business',
                'school': 'Nanyang Technological University',
                'starts_at': None},
               {'degree_name': 'PSLE',
                'description': None,
                'ends_at': None,
                'field_of_study': None,
                'school': [],
                'starts_at': None}],
 'experiences': [{'company': 'PetsLobang',
                  'company_linkedin_profile_url': None,
                  'company_urn': 'urn:li:fsd_company:13391052',
                  'description': 'Sell pet food',
                  'ends_at': {'day': None, 'month': 1, 'year': 2018},
                  'location': 'Singapore',
                  'starts_at': {'day': None, 'month': 6, 'year': 2017},
                  'title': 'Owner'},
                 {'company': 'NodeFlair',
                  'company_linkedin_profile_url': 'https://www.linkedin.com/company/nodeflair/',
                  'company_urn': 'urn:li:fsd_company:13705849',
                  'description': 'Firefighting',
                  'ends_at': None,
                  'location': 'Singapore',
                  'starts_at': {'day': None, 'month': 3, 'year': 2018},
                  'title': 'Co-Founder'},
                 {'company': 'ShopBack',
                  'company_linkedin_profile_url': 'https://www.linkedin.com/company/shopback-com/',
                  'company_urn': 'urn:li:fsd_company:3804922',
                  'description': 'Tech - Database:\n'
                                 '1) Financial Due Diligence for Fund Raising\n'
                                 '2) Built financial DB and automated monthly '
                                 'generation of financial figures - Reduce '
                                 'time taken to < 3 days\n'
                                 '3) Revenue provisioning of all countries and '
                                 'top merchants with Data Team\n'
                                 '\n'
                                 'Tech Stack: Python, MySQL\n'
                                 '\n'
                                 'Others:\n'
                                 '1) Led Sensitive Analysis project on Payment '
                                 'and presented to CEO and management\n'
                                 '2) Prepared a Quarterly Investor Update on '
                                 'new partnerships, product development '
                                 'marketing success\n'
                                 '\n'
                                 'Tools used: Microsoft Excel VBA',
                  'ends_at': {'day': None, 'month': 8, 'year': 2017},
                  'location': '77 Ayer Rajah Crescent #03-23, 139954',
                  'starts_at': {'day': None, 'month': 1, 'year': 2017},
                  'title': 'Business Process Management'},
                 {'company': 'ShopBack',
                  'company_linkedin_profile_url': 'https://www.linkedin.com/company/shopback-com/',
                  'company_urn': 'urn:li:fsd_company:3804922',
                  'description': 'Qualitative Research:\n'
                                 '1) Conducted >20 User Testing to understand '
                                 "app's usability\n"
                                 "2) Head dogfooding for app's V2\n"
                                 '3) Gathered insights by interacting with '
                                 "ShopBack's Facebook community\n"
                                 '\n'
                                 'Quantitative Research:\n'
                                 '1) Performance comparison of the app across '
                                 'different versions using MySQL\n'
                                 '\n'
                                 'Empowering stakeholders:\n'
                                 '1) Revamped data collection with Engineering '
                                 'Team  to empower Marketing with in-house '
                                 'analytical tools by defining the parameters '
                                 'of every app actions (clicks, scrolls etc.)\n'
                                 '2) Educated APAC teams by creating lessons '
                                 'on the in-house tools created \n'
                                 "3) Presented analysis of app's performance "
                                 'to APAC teams\n'
                                 '\n'
                                 'Technical:\n'
                                 '1) Live configuration of the app to '
                                 'integrate new merchants\n'
                                 "2) Created links for customized app's "
                                 'onboarding flows\n'
                                 '\n'
                                 'Market Research:\n'
                                 '1) Explore product opportunities by doing '
                                 'analysis on the different verticals of '
                                 'e-commerce markets\n'
                                 '\n'
                                 'Tech stack: MySQL, MongoDB\n'
                                 'Tools used: Confluence, JIRA',
                  'ends_at': {'day': None, 'month': 8, 'year': 2018},
                  'location': 'Singapore',
                  'starts_at': {'day': None, 'month': 5, 'year': 2018},
                  'title': 'Product (Mobile)'},
                 {'company': 'City Fellows Consortium',
                  'company_linkedin_profile_url': 'https://www.linkedin.com/company/city-fellows-consortium/',
                  'company_urn': 'urn:li:fsd_company:6642965',
                  'description': 'The City Fellows Consortium is an '
                                 'innovation-centered private league for Los '
                                 "Angeles' top undergraduate engineering "
                                 'fellows, selected from the region’s most '
                                 'elite universities. \n'
                                 '\n'
                                 '- interacting, learning and building new '
                                 'ties with top local innovation leaders and '
                                 'VC on a monthly basis',
                  'ends_at': {'day': None, 'month': None, 'year': 2018},
                  'location': 'Singapore',
                  'starts_at': {'day': None, 'month': 9, 'year': 2016},
                  'title': 'Consortium Fellow'}],
 'first_name': 'Adrian',
 'headline': 'Co-founder at NodeFlair | code() at where you love',
 'languages': ['Chinese', 'English'],
 'last_name': 'Goh Jun Wei',
 'occupation': 'Co-founder at NodeFlair | code() at where you love',
 'profile_pic_url': 'https://media-exp1.licdn.com/dms/image/C5103AQEIacaKtddOqg/profile-displayphoto-shrink_800_800/0?e=1603324800&v=beta&t=a5xQPRi2XqT9TaIo9k3V7IaJ8hgPLS0b_VLMaiLJhVk',
 'public_identifier': 'adriangohjw',
 'skills': ['Data Analysis',
            'React.js',
            'Leadership',
            'Flask',
            'Product Management',
            'Ruby on Rails',
            'Entrepreneurship',
            'SQL',
            'Python',
            'Project Management',
            'Java',
            'Start-ups',
            'Microsoft Excel'],
 'state': None,
 'summary': 'www.nodeflair.com',
 'volunteer_work': []}
```



| Key                          | Description                                                  | Example                                                      |
| ---------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| public_identifier            | The public id of the profile.                                | `"williamhgates"`                                            |
| profile_pic_url              | URL to the user's profile picture.                           | `"https://media-exp1.licdn.com/dms/image/C5603AQHv9IK9Ts0dFA/profile-displayphoto-shrink_800_800/0?e=1597276800&v=beta&t=QN-3KjvC5KHvT3joe12sE3mlGLEwiBU0KSi2OJSap_U"` |
| first_name                   | First name of the user                                       | `"Bill"`                                                     |
| last_name                    | Last name of the user                                        | `"Gates"`                                                    |
| occupation                   | Self declared occupation of the user                         | `"Co-chair, Bill & Melinda Gates Foundation"`                |
| headline                     | Self declared headline of the user                           | `"Co-chair, Bill & Melinda Gates Foundation`"                |
| summary                      | Self declared summary of the user                            | `"Co-chair of the Bill & Melinda Gates Foundation. Microsoft Co-founder. Voracious reader. Avid traveler. Active blogger."` |
| country                      | Two-letter country code / country abbreviation ISO-3166-1 ALPHA-2 | `"us"`                                                       |
| country_full_name            | Full name of the country                                     | `"Singapore"`                                                |
| city                         | Full name of the City                                        | `"Portland"`                                                 |
| state                        | Full name of the State                                       | `"Oregon"`                                                   |
| experiences                  | List of work experiences                                     | ```{"company":"PetsLobang","company_linkedin_profile_url":null,"company_urn":"urn:li:fsd_company: 13391052","description":"Sell pet food","ends_at":{"day":null,"month":1,"year":2018},"location":"Singapore","starts_at":{"day":null,"month":6,"year":2017},"title":"Owner"}``` |
| education                    | List of education background                                 | `{"degree_name":"Bachelor’s Degree","description":"NANYANG Scholarship","ends_at":null,"field_of_study":"Computer Science with Minor in Business","school":"Nanyang Technological University","starts_at":null}` |
| languages                    | List of languages that the user is versatile in              | `["English","Hindi"]`                                        |
| accomplishment_organisations | List of organisations that the user is a member of           |                                                              |
| accomplishment_publications  | List of publications that the user published                 | `[{"description":"some description","name":"nubela-publication","published_on":{"day":2,"month":3,"year":2016},"publisher":"nubela-publisher"}]` |
| accomplishment_honors_awards | List of honors and awards that the user has posted on his profile | `[{"description":"honour-desc","issued_on":{"day":null,"month":2,"year":2018},"issuer":"some-issuer","title":"some-honour"}]` |
| accomplishment_patents       | List of organisations that the user is a member of           | `[{"application_number":null,"description":"some patent desc","issued_on":{"day":3,"month":2,"year":2016},"issuer":"sg","patent_number":"123","title":"nubela-patent","url":"http: //nubela.co/patent"}]` |
| accomplishment_courses       | List of organisations that the user is a member of           | `[{"name":"some course name","number":"123"}]`               |
| accomplishment_projects      | List of organisations that the user is a member of           | `[{"description":"some project","ends_at":{"day":null,"month":1,"year":2070},"starts_at":{"day":null,"month":4,"year":2017},"title":"some project","url":"https: //nubela.co"}]` |
| accomplishment_test_scores   | List of organisations that the user is a member of           | `[{"date_on":{"day":null,"month":2,"year":2013},"description":"nailed-it","name":"cs1101s","score":"A"}]` |
| volunteer_work               | List of organisations that the user is a member of           | `[{"cause":"CHILDREN","company":"Interact Club","company_linkedin_profile_url":null,"company_urn":null,"description":null,"ends_at":{"day":null,"month":12,"year":2007},"location":null,"starts_at":{"day":null,"month":1,"year":2006},"title":"Ex-co"},{"cause":"CHILDREN","company":"Make-A-Wish Foundation® (Singapore) Ltd","company_linkedin_profile_url":"https://www.linkedin.com/company/make-a-wish-sg/","company_urn":"urn:li:fsd_company:13329983","description":null,"ends_at":null,"location":null,"starts_at":{"day":null,"month":10,"year":2015},"title":"Wish Granter"}]` |
| skills                       | List of organisations that the user is a member of           | `["Marketing","Public Relations","Competitive Analysis","Marketing Communications","Product Marketing","Entrepreneurship","Event Management","Sales","Marketing Strategy","Teamwork","Social Media","Market Research","Fundraising","Social Media Marketing","Online Marketing","Start-ups","Product Development","Leadership","Business Strategy","New Business Development"]` |
| certifications               | List of organisations that the user is a member of           | `[{"authority":"Emergenetics International","display_source":"emergenetics.com","ends_at":null,"license_number":null,"name":"Emergenetics","starts_at":{"day":null,"month":7,"year":2017},"url":"https://www.emergenetics.com/"}]` |
| birth_date                   | Month and year of the user's birthday (Dependent on profile's privacy settings) | `{"month":12,"day":13,"year":null}`                          |
| html_src                     | (Optional) HTML source of this Linkedin Profile. To have this value shown, please include `src=include` in the Proxycurl request. | `<html>....</html>`                                          |

## Linkedin Company Profile API



```python
import requests

api_endpoint = 'https://nubela.co/proxycurl/api/linkedin/company'
linkedin_profile_url = 'https://www.linkedin.com/company/8m-real-estate-singapore/about'
api_key = 'YOUR_API_KEY'
header_dic = {'Authorization': 'Bearer ' + api_key}

response = requests.get(api_endpoint,
                        params={'url': linkedin_profile_url},
                        headers=header_dic)
```



`GET https://nubela.co/proxycurl/api/linkedin/company`



**URL Parameters**

| Parameter | Required | Description                                                  | Input                        | Example                                                      | Default value |
| --------- | -------- | ------------------------------------------------------------ | ---------------------------- | ------------------------------------------------------------ | ------------- |
| `url`     | yes      | URL of the Linkedin Company Profile to crawl. URL should be in the format of `https://www.linkedin.com/company/<unique_li_id>` | Linkedin Company Profile URL | `"https://www.linkedin.com/company/8m-real-estate-singapore/about"` |               |
| `src`     | no       | Includes the raw HTML source code that is fetched and parsed | The string "include"         | `include`                                                    | N/A           |



### Company Profile Response


```json
{
   "description":"8M is a specialized real estate investment & operating company with more than S$700M AUM.  We employ creative, repositioning strategies across multiple asset classes in Singapore to unlock long-term value & build community.  \n  \n8M creates lifestyle destinations with a sustainable drive by readapting existing real estate with purposeful design and best-in-class partnerships to re-energize Singapore communities.  We are a business at the forefront of an evolving landscape, presenting an unrivaled portfolio of real estate across the city's most desirable districts.  \n\nIn our pursuit to evolve the way people live, work & play in Singapore, 8M Collective was formed in 2018 as the umbrella brand and management company of 8M Real Estate's rapidly accommodation business.  8M Collective is transforming Singapore stays through the conception & development of flexible-living concepts that aim to transform the way people stay in Singapore.\n\nIn just 5 years, we have been instrumental in the re-invigoration of prime areas including Amoy Street & Keong Saik Road and have launched popular boutique living concepts including Base Residences, Ann Siang House and K\u0113Sa House.",
   "website":"http://8mrealestate.com",
   "industry":"Real Estate",
   "company_size":[
      11,
      50
   ],
   "company_size_on_linkedin":44,
   "hq":{
      "country":"SG",
      "geographic_area":null,
      "city":"Singapore",
      "postal_code":"069907",
      "line_1":"88a Amoy St",
      "is_hq":true
   },
   "company_type":"PRIVATELY_HELD",
   "founded_year":2014,
   "specialities":[
      "Acquisitions",
      "Asset Management",
      "Property Management",
      "Real Estate Finance",
      "Leasing",
      "Hospitality",
      "Alternative Accommodation",
      "Property Development",
      "Portfolio Management",
      "Deal Sourcing",
      "Development",
      "Hospitality Management",
      "Owner/Operator",
      "place making",
      "Re-adaptive Use",
      "Refurbishment"
   ],
   "locations":[
      {
         "country":"SG",
         "geographic_area":null,
         "city":"Singapore",
         "postal_code":"069907",
         "line_1":"88a Amoy St",
         "is_hq":true
      }
   ],
   "name":"8M",
   "tagline":"A SPECIALIZED REAL ESTATE INVESTMENT & OPERATING CO.\n",
   "universal_name_id":"8m-real-estate-singapore",
   "profile_pic_url":"https://media-exp1.licdn.com/dms/image/C510BAQGSRz4mjWcjxg/company-logo_400_400/0?e=1603929600&v=beta&t=yJgQGG-jGRnP1IkFjMF_wJv4fdYlp5o6SaAbtXkFBQo",
   "background_cover_image_url":"https://media-exp1.licdn.com/dms/image/C511BAQHp0169DoUyWQ/company-background_200/0?e=1596193200&v=beta&t=pZfzSUUsYbqBZ9fgrliGhH-eu5HN26wpL-bUFZwkPeg",
   "funding_data":null,
   "phone":"+65 6323 0454"
}
```



| Key                        | Description                                                  | Example                                                      |
| -------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| description                | The overview section in the About page                       | `"8M is a specialized real estate investment & operating company with more than S$700M AUM.  We employ creative, repositioning strategies across multiple asset classes in Singapore to unlock long-term value & build community."` |
| website                    | The listed website on the profile                            | `"http://8mrealestate.com"`                                  |
| industry                   | Industry of the company                                      | `"Real Estate"`                                              |
| company_size               | Listed range of company headcount                            | `[11, 50]`                                                   |
| company_size_on_linkedin   | Total employees on Linkedin that declared themselves to be staff of said company | `39`                                                         |
| hq                         | Address of company's headquarters                            | `"[{'city': 'Singapore',<br/>                'country': 'SG',<br/>                'geographic_area': None,<br/>                'is_hq': True,<br/>                'line_1': '88a Amoy St',<br/>                'postal_code': '069907'}]" |
| company_type               | Enumerator of company type. Could be PUBLICLY_HELD or PRIVATELY_HELD | `"PUBLICLY_HELD"`                                            |
| founded_year               | The year that this company is founded in                     | `1996`                                                       |
| specialities               | List of specialities                                         | `["Acquisitions", "Asset Management"]`                       |
| locations                  | List of locations                                            | `[{"city":"Singapore","country":"SG","geographic_area":null,"is_hq":true,"line_1":"88a Amoy St","postal_code":"069907"}]` |
| name                       | Name of the company                                          | `"8M"`                                                       |
| tagline                    | Tagline of the company                                       | `"A SPECIALIZED REAL ESTATE INVESTMENT & OPERATING CO"`      |
| universal_name_id          | Month and year of the user's birthday (Dependent on profile's privacy settings) | `"8m"`                                                       |
| profile_pic_url            | Profile picture of the                                       | `"https://media-exp1.licdn.com/dms/image/C510BAQGSRz4mjWcjxg/company-logo_400_400/0?e=1603929600&v=beta&t=yJgQGG-jGRnP1IkFjMF_wJv4fdYlp5o6SaAbtXkFBQo"` |
| background_cover_image_url | Wechat contact information (Dependent on profile's privacy settings) | `"https://media-exp1.licdn.com/dms/image/C510BAQGSRz4mjWcjxg/company-logo_400_400/0?e=1603929600&v=beta&t=yJgQGG-jGRnP1IkFjMF_wJv4fdYlp5o6SaAbtXkFBQo"` |
| funding_data               | Crunchbase data of said company's funding data               |                                                              |
| phone                      | Phone number                                                 | `"+65 1234 1234"`                                            |
| html_src                   | (Optional) HTML source of this Linkedin Profile. To have this value shown, please include `src=include` in the Proxycurl request. | `<html>....</html>`                                          |



### Timeouts and average request duration

The endpoints in our Linkedin crawler takes an average of <u>23 seconds</u> to complete.

The duration is a result of at least 4 hops in real-time; from your client, to the coordinating server, to the crawl worker, to Linkedin website.

Do note that the value of 23 seconds is the average duration, and the variance is large because workers with poor latency might take longer to respond to the crawl request.

We recommend a timeout of at least <u>60 seconds at minimum</u>, with an <u>optimal timeout of 120 seconds</u>.



You should not implement this endpoint to crawl synchronously as it will be slow. An async approach with threads or your favourite asynchronous approach is highly recommended.



## Crawling other pages

To crawl a page that is otherwise blocked from bulk web scraping, you can make a general request with Proxycurl's pool of workers.



### HTTP Request

`GET https://nubela.co/proxycurl/api`



#### JSON body

| Parameter   | Required | Description                                                  | Example                         |
| ----------- | -------- | ------------------------------------------------------------ | ------------------------------- |
| url         | yes      | The URL of the website you want to crawl                     | https://www.amazon.com/         |
| headers     | no       | An array of named objects to override the default request headers. | `{'lang': 'en'}`                |
| method      | no       | The HTTP method for the node to make the request with. Defaults to `GET` | `DELETE`                        |
| contentType | no       | When sending data to the server, use this content type.<br />Defaults to `application/x-www-form-urlencoded; charset=UTF-8` |                                 |
| data        | no       | Content to be placed into the content body of the request.   |                                 |
| dataType    | no       |                                                              | `xml`, `json`, `script`, `html` |



```python
import requests

api_endpoint = 'https://nubela.co/proxycurl/api'
api_key = 'YOUR_API_KEY'
header_dic = {'Authorization': 'Bearer ' + api_key}
payload = {'url': 'https://api.ipify.org?format=json'}


response = requests.get(api_endpoint,
                        json=payload,
                        headers=header_dic)
```





### Response

| Key         |                                         |
| ----------- | --------------------------------------- |
| data        | HTML source of the page that is crawled |
| status_code | Status code of the worker's crawl job   |



```json
{"data":"{\"ip\":\"200.83.234.140\"}","status_code":200}
```



