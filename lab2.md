![image](https://github.com/SumayKalra/cse15L-labreports-winter2024/assets/67125138/d7d449b9-c759-4098-b018-4cd5b7b0d80c)

![image](https://github.com/SumayKalra/cse15L-labreports-winter2024/assets/67125138/93543ecf-dbb8-4453-8177-3d2e374f35b5)
Which methods in your code are called?
- The method called here is handleRequest(URL) in the chat Handler class
  
What are the relevant arguments to those methods, and the values of any relevant fields of the class?
- The url argument is relevant to the handler method, the path is the /add-message with the query being/add-message?s=Hello&user=jpolitz
- chat log is relevant as it starts as an empty string and this new query is basically added to it and then its displayed

How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why.
- How it works to me is the handler request checks the path, and its add message, so it goes on to the code to add a message, in which the chat log value is updated from an empty string to what we see on the query

![image](https://github.com/SumayKalra/cse15L-labreports-winter2024/assets/67125138/6f525b07-10ee-409b-a563-dbbc2bcb7962)
Which methods in your code are called?
- The method called here is handleRequest(URL) in the chat Handler class

What are the relevant arguments to those methods, and the values of any relevant fields of the class?
- The url argument is relevant to the handler method, the path is the /add-message with the query being/add-message?s=Hi&user=Yash
- chat log is relevant as it starts as an the new string from the last command and this new query is basically added to it and then its displayed
How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why.
- How it works to me is the handler request checks the path, and its add message, so it goes on to the code to add a message, in which the chat log value is updated fromthe first string to both so it looks like a chat

