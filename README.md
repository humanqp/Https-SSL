# Https-SSL
> ###  암호화 / 인증
  - 비대층키 암호화 : Public Key를 암호화하고 Public Key와 쌍을 이루는 Private Key로 복호화
  - 비대층키로 인증 : Private Key로 암호화하고 Public Key로 복호화 성공 시 Private Key의 사용자를 인증 하는 방식(PKI)
  
> ###  SSL 인증서 내용
  - 서비스 정보 : CA, 서비스 도메인 등등
  - 공개키의 내용, 공개키의 암호화 방법

> ### SSL 통신 방식
  - Sever -> Client로 Pulbic key가 포함되어 있는 SSL인증서를 Client에 전달 함
  - Client는 SSL인증서를 Public key를 확인하고 SSL인증서의 유효함(인증)을 확인 함.
  - Client는 다시 대층키를 생성하여 Server에서 제공한 Public key로 대층키를 암호화하고 해당 대층키를 가지고 전송한 데이터를 암호화 함
  - Server는 Client에서 생성한 대층키를 자신이 가지고 있는 Private Key를 가지고 대층키를 얻고 해당 키를 가지고 Client에서 전송한 데이터를 복호화 함
  - Client와 Server 간 대층키가 공유되었고, 서로간 데이터 전송에 해당 대층키를 사용함.


