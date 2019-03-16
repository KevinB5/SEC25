# GROUP 25

- Kevin Corrales 94131
- Mário Silva 93799
- Cintia Almeida 85139

#Dúvidas:
- Interface Gráfica
- Um user pode comprar e vender ao mesmo tempo?
- 2 users podem combinar para fazer uma sobrecarga no sistema?
- 

#To Do List:
- An initial set of users, the set of goods they own (represented via a set of tuples
<goodID, userID>) and the notary identity are assumed to exist when the
application first starts.
- The initial set of users and goods is immutable and known by
every user. 
- notary initially has access to the set of users (and their public keys) and the
corresponding set of goods they own.
- notary has to certify that:
  1) the good to be transferred is currently owned by the seller;
  2) both the seller and the buyer have expressed their interest in executing the
transaction.
- users can perform:
  1) obtain the status of any good, i.e. its owner and whether it is on sale;
  2) express their intention to sell any of their goods or buy any good currently
available on sale;
  3) submit their transaction requests to the notary.
- Notary equipped with Citizen Card (cryptography)
- User are identified through a Public-Key Infrastructure (PKI), static and public.
 
#Verify workflow
#Implementation Steps

Sites onde podemos buscar info:
- http://cs.lmu.edu/~ray/notes/javanetexamples/

#ameaças

-Forjar identidade de um cliente(autenticidade)
-Alterar o conteúdo de uma mensagem durante a transmissão(integridade)
-Negar o envio de umaa certa mensagem(repúdio)
-Retransmissão de mensagens já enviadas(replay attack)

#mecanismos de proteção

-assinatura digital do resumo das mensagens (3 primeiras ameaças)
-um sequenciador , exclusivo de cada cliente, em cada mensagem deste(ultima ameaça)


