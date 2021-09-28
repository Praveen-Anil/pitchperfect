# pitchperfect
PITCH PERFECT: A platform, For ideas to reach its true potential
List of Personas:
o	Students / Developers (Founders)
o	Login / Sign In
o	Domain
o	Idea submission (Create / Save / Delete)
o	Validate idea
o	List ideas with matching
o	Accept / Reject invitation from investor
o	Investors
o	Login / Sign In
o	Filter / Search ideas
o	Rate / Comment on Ideas
o	Interest (Partial interest for collaboration)
o	Setup meeting
o	Invest
Database Schema:
 
API’s needed:
o	Login API (v1/pitchperfect/login)
o	API for submit(v1/pitchperfect/idea)
o	API to retrieve project names and abstracts
o	API to retrieve projects based on filters / Search API
o	API to save project details
o	API to delete project details
o	API for investors to show interest in a project
o	API for investors to invest on projects
o	
API	Methods	Response code	Input	Response Json/String
v1/pitchperfect/login	POST	200 
	User,password	Json with access token
		401		Unauthorized
		403		Forbidden
v1/pitchperfect/idea	POST	201	{"title":"","abstract":"","scope":"","implementationDetails":""}	Id, timestamp
v1/pitchperfect/idea/{id}	PUT	200	{"title":"","abstract":"","scope":"","implementationDetails":""}	
	DELETE	204		
	GET	200		Title,abstract,scope,implementationdetail,timestamp(created),timestamp(updated)
v1/pitchperfect/idea/{id}/rate	POST	200		
	GET	200		Rating value
v1/pitchperfect/idea/{id}/comment	POST,GET,DELETE	200,200,200		Post-
Get-all the comments
o	
Database:
Data is stored in MongoDB
Flow diagram:
 

