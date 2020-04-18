# myblockchain  
Grace Cheung  
gvc8  

1)  

node 8000 waiting for genesis block  
node 8003 waiting for genesis block  
node 8002 waiting for genesis block  
node 8004 waiting for genesis block  
node 8005 waiting for genesis block  
node 8001 broadcasting  
node 8005 broadcasting  
node 8001 broadcasting  
node 8003 broadcasting  
node 8004 broadcasting  
node 8003 broadcasting  
node 8000 broadcasting  
node 8005 broadcasting  
node 8005 - length 8 - head 000032454c7a6ee942e7730ad38f33a311b4264e76f7f683bb8819bbe870919f  
node 8001 - length 8 - head 000032454c7a6ee942e7730ad38f33a311b4264e76f7f683bb8819bbe870919f  
node 8002 - length 8 - head 000032454c7a6ee942e7730ad38f33a311b4264e76f7f683bb8819bbe870919f  
node 8004 - length 8 - head 000032454c7a6ee942e7730ad38f33a311b4264e76f7f683bb8819bbe870919f  
node 8003 - length 8 - head 000032454c7a6ee942e7730ad38f33a311b4264e76f7f683bb8819bbe870919f  
node 8000 - length 8 - head 000032454c7a6ee942e7730ad38f33a311b4264e76f7f683bb8819bbe870919f  
{'00001be563c5af60778148a111d303ee8cf9b03821313141f4295913e99aa0e0': {'header': {'index': 4,  
                                                                                 'nonce': '625156d9bf6f9e7c451e0b286b708a693a96f73d1a3ca1e1d8ec5d304ec62896',  
                                                                                 'parent': '000063449df568570c1bce4a4d68093908db8d51de92d9be618d58de870d6329',  
                                                                                 'timestamp': 1587172017.846845},  
                                                                      'transactions': None},  
 '000027489cd5c2a08536c4ec6c9f79a6ede5d3436c8fdbead8c308a6b795e390': {'header': {'index': 6,  
                                                                                 'nonce': '2cb38e757a0451c398e8acc093f00cce50ba3c5a39f944815596edcf7d91a688',  
                                                                                 'parent': '00005db430ce79efcf4010323cfe062148aa942f670aacb811e99e37e41af194',  
                                                                                 'timestamp': 1587172024.113337},  
                                                                      'transactions': None},  
 '000032454c7a6ee942e7730ad38f33a311b4264e76f7f683bb8819bbe870919f': {'header': {'index': 7,  
                                                                                 'nonce': 'bde335801f6f56eda80e694c8118946df951d6ec7444c815426f4c4c84d903cf',  
                                                                                 'parent': '000027489cd5c2a08536c4ec6c9f79a6ede5d3436c8fdbead8c308a6b795e390',  
                                                                                 'timestamp': 1587172039.775552},  
                                                                      'transactions': None},  
 '0000359dab4328c008050d59807bc632ae00e0a5f3641cf55562f11e8650bd0c': {'header': {'index': 2,  
                                                                                 'nonce': '2c85326b1a6ceb493f4fcf15be56762ed8a6e5e60b5bcd33a6740a7e0f62697e',  
                                                                                 'parent': '000069e8aa67b5989bc36e41d4faa415328d9874ee5cb52f0da10dea33d13c96',  
                                                                                 'timestamp': 1587172006.317229},  
                                                                      'transactions': None},  
 '0000482a52f379e6b48cd7a3073dd71c34ed2127542e44abe9e9922111ba5495': {'header': {'index': 0,  
                                                                                 'nonce': 'f4a3a6cf39e91569462c40573906aaaa8a443d9a93a7c0cb7bac2b9c48fa0213',  
                                                                                 'parent': 0,  
                                                                                 'timestamp': 1587171972.350563},  
                                                                      'transactions': []},  
 '00005db430ce79efcf4010323cfe062148aa942f670aacb811e99e37e41af194': {'header': {'index': 5,  
                                                                                 'nonce': '561aee47c952cb69d1b07d894a66dd7c06649353840b8dc1163e9b364c0017da',  
                                                                                 'parent': '00001be563c5af60778148a111d303ee8cf9b03821313141f4295913e99aa0e0',  
                                                                                 'timestamp': 1587172022.0193899},  
                                                                      'transactions': None},  
 '000063449df568570c1bce4a4d68093908db8d51de92d9be618d58de870d6329': {'header': {'index': 3,  
                                                                                 'nonce': 'e66ae6186468d5a193184742df435b409d75d020bcd725b473f86d1232b5f0cd',  
                                                                                 'parent': '0000359dab4328c008050d59807bc632ae00e0a5f3641cf55562f11e8650bd0c',  
                                                                                 'timestamp': 1587172012.3535519},  
                                                                      'transactions': None},  
 '000069e8aa67b5989bc36e41d4faa415328d9874ee5cb52f0da10dea33d13c96': {'header': {'index': 1,  
                                                                                 'nonce': '747ce9d2964af19cf893341c050b17971ced38d6b3fa7db66077b6b30086604e',  
                                                                                 'parent': '0000482a52f379e6b48cd7a3073dd71c34ed2127542e44abe9e9922111ba5495',  
                                                                                 'timestamp': 1587171988.029807},  
                                                                      'transactions': None}}  
  
2)  
  
a) Why do so many more blocks appear in the list of all those known in the system? Why are there so many with the same index?  

The variable DIFFICULTY is used to set the mining difficulty. In this case, this is implemented by checking for a block whose hash beats the difficulty parameter by having at least that many leading zeros. If a block that fulfills the difficulty parameter is not found within a certain limit of tries, then find_block returns (None, None). So, when the difficulty is lowered, 

b) Do most or all of the nodes all exit with the same head of the chain? If so, how? If not, why can’t they agree?  

