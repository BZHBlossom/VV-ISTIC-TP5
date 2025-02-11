# Random Wikipedia walker

Using Selenium, create a small program that, starting from the main page https://www.wikipedia.org/, walks trough a sequence of random links and takes a snapshot of the last page.
The process is as follows:

 1. Navigate to the main page https://www.wikipedia.org/
 2. Select a random link in the page
 3. Navigate to the link
 4. Repeat steps 2 to 3 until you have visited 10 different pages
 5. Take a snapshot of the current page and save it

Include the code of the walker and the snapshot in this document.

## Answer
```JSON
{
"id": "46c92b79-7451-4950-a79d-dbcb113de89b",
"version": "2.0",
"name": "tp5",
"url": "https://www.wikipedia.org/",
"tests": [{
"id": "7a1cca0b-98cc-4227-a2e2-542538ece130",
"name": "Untitled",
"commands": [{
"id": "ee12be77-b9cb-4b1f-8266-c85f48bc2a73",
"comment": "",
"command": "open",
"target": "https://www.wikipedia.org/",
"targets": [],
"value": ""
}, {
"id": "60c5f132-153a-44a5-9b76-aec4f14f859c",
"comment": "",
"command": "times",
"target": "10",
"targets": [],
"value": ""
}, {
"id": "55d6fb7a-4898-4aeb-ac0d-7de0b9e840a2",
"comment": "",
"command": "executeScript",
"target": "var links = document.getElementsByTagName(\"a\"); var randNum = Math.round( Math.random() * (links.length-1)); links[randNum].click()",
"targets": [],
"value": ""
}, {
"id": "68e99eba-5c98-4df5-b1be-3ac4b4370109",
"comment": "",
"command": "end",
"target": "",
"targets": [],
"value": ""
}, {
"id": "aa2a8739-cbbe-42ca-a9d1-83ce36032121",
"comment": "",
"command": "",
"target": "",
"targets": [],
"value": ""
}]
}],
"suites": [{
"id": "ecbdfd53-03c6-4442-9850-9a0f13283593",
"name": "Default Suite",
"persistSession": false,
"parallel": false,
"timeout": 300,
"tests": ["7a1cca0b-98cc-4227-a2e2-542538ece130"]
}],
"urls": ["https://www.wikipedia.org/"],
"plugins": []
}
```
Ce qui donne ceci dans l'éditeur web :
![img_1.png](img_1.png)


Avec la capture d'écran de la dernière page :
![img.png](img.png)