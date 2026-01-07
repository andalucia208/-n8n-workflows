# -n8n-workflows
Collection of my n8n automation workflows @me
- The GamesTailor workflow: automates email notifications by receiving an email generated from a webform of enquiries for ideas for "80s arcade type of online 20 second games" which its prize for the players is a CTA button for an incentive to use the company's services (i.e: discount coupon etc)
Workflow: Workflow's Emails trigger receives a new email from the website webform. Extracts the email body and ID, takes it to the AI agent for web scrapping and creating a sales pitch for the game idea based on the curtomer's industry and brand, using OpenAI chat model.
Then it sends it to Stripe node for creating a payment link, from there takes it though the "Edit Fields" node to prepare the reply the cutomer name, the payment URL and the game pitch in the email and them reply to the csutomer using the " Outlook- send a message" node.
- The Pseudonymization workflow: receives emails with PII sensitive data from a " Email Trigger (IMAP)" node, take it to an "HTTP Request" node in order to pseudonymize (hide the PII- the Personally Identifiable Information of) the email and then replies it back to the customer.
