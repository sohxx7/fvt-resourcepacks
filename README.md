# FvT Minecraft 26.3 Resource Packs

현재 배포: [연출 복구 8](https://github.com/sohxx7/fvt-resourcepacks/releases/tag/v2026.10.27-mc26.3.8-cinematics)

원본 1.21.7 서버의 연출을 26.3에서 복구한 리소스팩입니다. 51개 화면 효과를 유지하며 접속자용 보조 모드는 필요하지 않습니다. 서버는 함께 제공된 Gamerule 1.0-fvt263.4를 사용해야 합니다.

## 수정 내용

- 임시 이펙트 엔티티의 청크 준비를 보완해 대형 불꽃·종·성·달 등의 표시 누락을 수정했습니다.
- 원본 캐릭터 스킨 90개를 서버 실행본에 복원했습니다.
- 효과 번호·진행값을 지속 표시 신호로 전달해 흡광·반사·왜곡·블룸을 복구했습니다.
- 배드애플의 BetterModel 호환 오류와 이동 고정 효과가 관전 카메라를 끊던 문제를 수정했습니다.

원본 Paper/client 1.21.7과 26.3에서 언급한 연출 19종을 실제 재생했습니다. 배드애플은 양쪽에서 전체 재생했으며, POTG의 일반 강조·멀티 킬·렌즈도 녹화한 QA 프레임과 제어한 사망 이벤트로 기존 Replay 렌더러를 검사했습니다. 기존 Fabulously Optimized 모드 54개를 복사한 격리 클라이언트에서 추가 재생과 실제 리소스 재로딩 2회도 마쳤습니다.

셰이더 변형 46개, Shaderc 조합 368개, 외부 API 참조 1,517개를 검사했습니다. 공개 다운로드의 크기·CRC·SHA1·SHA256도 인증 없이 검증했습니다. 원본의 모든 독립 색상 버퍼를 재생성한 것은 아니므로 모든 조명·투명도 겹침의 픽셀 단위 동일성을 보장하지는 않습니다.

## 다운로드

다음 순서로 적용합니다. GitHub 로그인이나 리소스팩 전용 포트 개방이 필요하지 않습니다.

1. [base.zip](https://github.com/sohxx7/fvt-resourcepacks/releases/download/v2026.10.27-mc26.3.8-cinematics/base.zip)
2. [Touhou_Holy_Grail_War_sub_1.zip](https://github.com/sohxx7/fvt-resourcepacks/releases/download/v2026.10.27-mc26.3.8-cinematics/Touhou_Holy_Grail_War_sub_1.zip)
3. [Touhou_Holy_Grail_War_sub_2.zip](https://github.com/sohxx7/fvt-resourcepacks/releases/download/v2026.10.27-mc26.3.8-cinematics/Touhou_Holy_Grail_War_sub_2.zip)

[SHA1/SHA256 목록](https://github.com/sohxx7/fvt-resourcepacks/releases/download/v2026.10.27-mc26.3.8-cinematics/manifest.json)

서버 실행본의 port263.yml과 Gamerule resourcepacks.yml은 위 공개 주소를 사용합니다. 이 저장소의 릴리스 파일은 리소스팩입니다.

원본 프로젝트 및 리소스 제작: [heIp12/fate-vs-touhou-Server v1.0.0](https://github.com/heIp12/fate-vs-touhou-Server/releases/tag/v1.0.0)
