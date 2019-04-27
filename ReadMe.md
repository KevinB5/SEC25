# GROUP 25

- Kevin Corrales 94131
- Mário Silva 93799
- Cintia Almeida 85139

#Dúvidas 2 fase:
- Se cada replica do notario tem um id diferente? Como faz com a chave? Todos utilizam a mesma chave ou criam novas?

_______________________________________________________________________________________________________________________
#Dúvidas:
- O projeto inicia com lista de users e de good predefinidos, como ligam os users? abrem todos automaticamente ou ligam 1 a 1, dizendo o id do user?
- O cliente também tem que ler a lista de goods?
- O que acontece aos PrivateKeys no GenerateKeyPair() ?
- PKI é uma entidade a parte ou apenas uma classe?

#To Do List:
- / An initial set of users, the set of goods they own (represented via a set of tuples
<goodID, userID>) and the notary identity are assumed to exist when the
application first starts.
- X The initial set of users and goods is immutable and known by
every user. 
- / notary initially has access to the set of users (and their public keys) and the
corresponding set of goods they own.
- notary has to certify that:
  1) the good to be transferred is currently owned by the seller;
  2) both the seller and the buyer have expressed their interest in executing the
transaction.
- X users can perform:
  1) obtain the status of any good, i.e. its owner and whether it is on sale;
  2) express their intention to sell any of their goods or buy any good currently
available on sale;
  3) submit their transaction requests to the notary.
- Notary equipped with Citizen Card (cryptography)
- / User are identified through a Public-Key Infrastructure (PKI), static and public.
 
#Verify workflow
#Implementation Steps

#Sites onde podemos buscar info:
- http://cs.lmu.edu/~ray/notes/javanetexamples/ (Server-Client)
- https://gist.github.com/dmydlarz/32c58f537bb7e0ab9ebf (RSA)
- https://crypto.stackexchange.com/questions/14339/securely-send-public-key-from-client-to-server-in-rsa (Lógica do RSA)
- http://www.informit.com/articles/article.aspx?p=170967&seqNum=6 (Implementação do MAC)
- https://www.programcreek.com/java-api-examples/?class=java.security.KeyStore&method=store (Keystore)
- https://docs.oracle.com/javase/7/docs/api/java/security/KeyStore.html (KeyStore javadoc)

#ameaças

-Forjar identidade de um cliente(autenticidade)
-Alterar o conteúdo de uma mensagem durante a transmissão(integridade)
-Negar o envio de umaa certa mensagem(repúdio)
-Retransmissão de mensagens já enviadas(replay attack)

# Info do stor

Meter contador para garantir a frescura
MAC assume que os dois sabem a chave e seria possivel forjar a chave.
Diffie Helman partilhar as chaves de forma segura
numero de sequencia de tcp
a sessão tem um counter e se não bater certo
log
biblioteca neutra para realizar a comunicação

#mecanismos de proteção

-assinatura digital do resumo das mensagens (3 primeiras ameaças)
-um sequenciador , exclusivo de cada cliente, em cada mensagem deste(ultima ameaça)

freshness - enviar sempre o MAC ou uma hash (message digest), e o servidor vai guardando
		se encontrar outro igual descarta
		alternativa: usar nonces


