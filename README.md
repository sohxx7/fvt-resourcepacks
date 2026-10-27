# FvT Minecraft 26.3 Resource Packs

현재 배포: [색상 합성 보정 10](https://github.com/sohxx7/fvt-resourcepacks/releases/tag/v2026.10.27-mc26.3.10-colors)

원본 1.21.7 서버의 연출을 26.3에서 복구한 리소스팩입니다. 51개 화면 효과를 유지하며 접속자용 보조 모드는 필요하지 않습니다. 서버는 함께 제공된 Gamerule 1.0-fvt263.5를 사용해야 합니다.

## 수정 내용

- 임시 이펙트 엔티티의 청크 준비를 보완해 대형 불꽃·종·성·달 등의 표시 누락을 수정했습니다.
- 원본 캐릭터 스킨 90개를 서버 실행본에 복원했습니다.
- 효과 번호·진행값을 지속 표시 신호로 전달해 흡광·반사·왜곡·블룸을 복구했습니다.
- 배드애플의 BetterModel 호환 오류와 이동 고정 효과가 관전 카메라를 끊던 문제를 수정했습니다.

원본 Paper/client 1.21.7과 26.3에서 언급한 연출 19종을 실제 재생했습니다. 배드애플은 양쪽에서 전체 재생했으며, POTG의 일반 강조·멀티 킬·렌즈도 녹화한 QA 프레임과 제어한 사망 이벤트로 기존 Replay 렌더러를 검사했습니다. 기존 Fabulously Optimized 모드 54개를 복사한 격리 클라이언트에서 추가 재생과 실제 리소스 재로딩 2회도 마쳤습니다.

셰이더 변형 84개, Shaderc 조합 672개, 외부 API 참조 1,530개를 검사했습니다. 공개 다운로드의 크기·CRC·SHA1·SHA256도 인증 없이 검증했습니다. 원본의 모든 독립 색상 버퍼를 재생성한 것은 아니므로 모든 조명·투명도 겹침의 픽셀 단위 동일성을 보장하지는 않습니다.

## 다운로드

다음 순서로 적용합니다. GitHub 로그인이나 리소스팩 전용 포트 개방이 필요하지 않습니다.

1. [base.zip](https://github.com/sohxx7/fvt-resourcepacks/releases/download/v2026.10.27-mc26.3.10-colors/base.zip)
2. [Touhou_Holy_Grail_War_sub_1.zip](https://github.com/sohxx7/fvt-resourcepacks/releases/download/v2026.10.27-mc26.3.10-colors/Touhou_Holy_Grail_War_sub_1.zip)
3. [Touhou_Holy_Grail_War_sub_2.zip](https://github.com/sohxx7/fvt-resourcepacks/releases/download/v2026.10.27-mc26.3.10-colors/Touhou_Holy_Grail_War_sub_2.zip)

[SHA1/SHA256 목록](https://github.com/sohxx7/fvt-resourcepacks/releases/download/v2026.10.27-mc26.3.10-colors/manifest.json)

서버 실행본의 port263.yml과 Gamerule resourcepacks.yml은 위 공개 주소를 사용합니다. 이 저장소의 릴리스 파일은 리소스팩입니다.

원본 프로젝트 및 리소스 제작: [heIp12/fate-vs-touhou-Server v1.0.0](https://github.com/heIp12/fate-vs-touhou-Server/releases/tag/v1.0.0)

## 전체 점검 추가 수정

실제 경기의 전투 진입을 막던 26.3 월드 경계 크기 오류를 현재 API 한도로 보정했습니다. 26.3에서 모델 전체를 거부하게 하던 빈 면 요소 2개도 제거하고 보이는 6개 요소는 유지했습니다.

캐릭터 50종·스킬 332개 설정·로드아웃이 원본과 일치했습니다. 공통 피해·방어·보호막·회복 19개 표본, 범위 질의 5개, 메뉴 6종의 문구를 비교했습니다. 실제 메뉴 구매 결과도 골드 500 차감·민첩 1 증가로 일치했습니다.

양쪽의 일반 2인 경기에서 선택·전투 진입·접속복구·종료를 실행했습니다. 재접속 중 라운드가 끝난 경우가 있어 전투가 계속되는 상황의 상태 보존까지 동일하다고 판정하지는 않았습니다. 기본 대화상자 여백·배치 차이는 남습니다. 모든 실전 조합·외부 랭크 API 쓰기·실제 스피커 청취의 전수 검증을 뜻하지 않습니다.

## 26.3 color composition update

The 26.3.10 pack preserves partial alpha in OIT and restores the original FFFFFE self-lit effect tint in the item renderer. All 51 screen effects, images, and sounds remain enabled. The six independent legacy color targets are not fully restored. Gamerule 1.0-fvt263.5 is unchanged.
