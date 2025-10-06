#semester project 
Abstract:
The Tender Management System is a web-based application developed to simplify and digitize the tendering process in colleges and organizations. Traditionally, tender creation, approvals, bidding, and contract awarding are handled manually, leading to delays, inefficiency, and lack of transparency.

This system is built using the MERN stack (MongoDB, Express.js, React.js, Node.js) and provides a fully automated workflow. It supports different user roles such as Departmental Coordinator, Director, Dean Procurement, Registrar, and Contractors, each with role-based access.

The process begins when a coordinator creates a tender request. This request must be approved by the Director, Dean Procurement, and Registrar before it is published. To ensure authenticity and security, all approvals and awarded contracts are validated using digital signatures from the respective authorities. Once approved, the tender is opened for bidding. Contractors can submit their quotations, which remain hidden until the bidding period ends to maintain fairness. After closing, the system automatically evaluates all bids and selects the lowest quotation for awarding the contract.

An important feature of the system is the segregation of tenders by department. Each coordinator manages tenders specific to their department, ensuring requirements, documents, and approvals are streamlined within the appropriate domain. This departmental categorization improves clarity, accountability, and ease of tracking tenders across the institution.

The awarded contract is digitally signed by the approving authorities, monitored until completion, and finally linked with a digital work completion certificate. All data—tenders, approvals, bids, contracts, and certificates—are managed through structured models to maintain accuracy, accountability, and legal compliance.

By digitizing workflows, integrating departmental segregation, and implementing digital signatures, this system improves efficiency, transparency, security, and fairness while reducing paperwork and administrative overhead. It makes tender management more effective and reliable for academic institutions and organizations.

Conditions
Tender requests must be approved by three authorities: Director, Dean Procurement, Registrar.

Approval must include a digital signature for authenticity.

Contractors cannot see others’ bids until the tender closes.

Contracts are awarded only to the lowest bidder after closing.

Each coordinator handles only tenders belonging to their department.

Completion certificates must be digitally signed before archiving.

Tasks
Tender Creation

Coordinator enters tender details and uploads requirements.

Tender status = PendingApproval.

Approval Workflow

System routes tender sequentially to Director, Dean Procurement, and Registrar.

Each authority digitally signs the approval.

Once all approve → Tender status = Approved.

Tender Publication

Approved tender becomes visible to contractors.

Status = OpenForBids.

Bidding Phase

Contractors submit bids before the deadline.

Quotations remain hidden until the tender closes.

Bid Evaluation

After closing, bids are compared automatically.

Winning bid = minimum quotation amount.

Contract Award

System generates a contract.

Authorities digitally sign it.

Status = InProgress.

Completion & Certificate

Coordinator updates contract on completion.

Work completion certificate is issued and digitally signed.

Status = Completed.

Actions
Coordinator: Create tenders, upload documents, monitor contracts, issue certificates.

Director/Dean/Registrar: Approve tenders & contracts with digital signatures.

Contractors: Submit bids, view awarded results, complete projects.

System: Manage role-based access, store approvals, auto-select lowest bid, maintain records.

Tech Stack
Frontend: React.js, Tailwind CSS/Bootstrap

Backend: Node.js, Express.js

Database: MongoDB (Mongoose for schema modeling)

Authentication: JWT, Role-based Access Control

File Handling: Multer (tender docs, contracts)

Digital Signatures: Node.js crypto / PKI-based hashing