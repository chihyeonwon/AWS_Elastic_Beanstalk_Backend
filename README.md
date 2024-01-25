# AWS_Elastic_Beanstalk_Backend
[AWS] AWS Elastic Beanstalk을 이용한 백엔드배포

## Elastic Beanstalk 이란?
```
애플리케이션 로드 밸런서, 오토 스케일링 그룹, RDS, EC2 등을 하나하나 따로따로 설정하지 않아도 된다.
Elastic Beanstalk이 이를 구축해 주고 연결해 준다.

백엔드 어플리케이션의 경우 RDS에 MySQL를 데이터베이스로 두며, 서버는 로드 밸런서에 오토 스케일링 그룹을
연결하는 형태이다.

따라서 첫 번째로 데이터베이스 설정을 한 후 오토 스케일링 그룹을 생성하고 오토 스케일링 그룹 내에서
실행되는 ec2 인스턴스들이 어플리케이션을 실행할 수 있도록 스크립트를 짜야 한다.
또 로드 밸런서에 오토 스케일링 그룹을 타깃 그룹으로 지정해줘야 한다.

이 모든 과정을 일래스틱 빈스톡은 한 커맨드 라인으로 가능하게 한다.

$ eb create --database --elb-type application --instance-type t2.micro
```

