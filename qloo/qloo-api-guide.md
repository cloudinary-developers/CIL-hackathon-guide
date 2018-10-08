# Qloo Developer Guide

[**Qloo**](https://qloo.com) **is the cultural AI, and we produce deep data science for the largest verticals of culture and entertainment. As experts in people’s taste, we uniquely find connections across over a dozen categories and use that knowledge to generate high quality recommendations at scale. For this hackathon, we’re giving you access to a limited version of our enterprise API.**  


**Challenge: Discover music by its relation to any combination of locations, books, restaurants, fashion, film, music or tV.**  


### **Overview**

**You, hackathoner, can use Qloo’s API to:**

* **Search through ≈ 5.5 million entities spanning books, restaurants, fashion, film, music, travel destinations and TV.**
* **Use any combination of entities to get recommendations in the category of your choice.**

### **Important Information**

* **Each team will be given a token to access the API.**
* **You need to add the following parameters to all API requests:**
  *       **"Content-Type": "application/json"**
  *       **"Authorization": &lt;token&gt;**

### **Quickstart**

**Javascript \(es6\)**  


| **const fetch = require\('node-fetch'\); const token = '...'; const url = 'https://gfqb4seej7.execute-api.us-east-1.amazonaws.com/production';  const qlooApi = async \(path, params\) =&gt; {   const paramString = new URLSearchParams\(params\).toString\(\);   const results = await fetch\(\`${url}/${path}?${paramString}\`, {     method: "GET",     headers: {       "Content-Type": "application/json",       "Authorization": token,     },   }\);   return await results.json\(\); }  \(async \(\) =&gt; {     console.log\(await qlooApi\('/search', { query: 'beyonce' }\)\);     console.log\(await qlooApi\('/recs', { sample: \['id', 'id'\] }\)\); }\)\(\)** |
| :--- |


### **API Endpoints**

**Our documentation for this project lives at:**  


**http://docs-a07d0e4aa.qloo.com/**  


