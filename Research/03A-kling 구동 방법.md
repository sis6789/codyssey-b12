## Kling으로 이 광고 제작하기 — 단계별 가이드

**핵심 전제**: Kling은 5~15초 단위 영상 클립 생성, 이미지 기반 캐릭터/장소 일관성(Elements 기능), O3 모델의 경우 오디오 동시 생성을 지원합니다. 다만 **정밀한 자막 타이포그래피, 한국어 나레이션 싱크, 프레임 단위 컷 편집**은 Kling 단독으로는 한계가 있어 별도 편집 툴과 병행해야 합니다.

### 1단계 — 레퍼런스 이미지 준비

컷1의 "차가운 방+인물 실루엣"과 컷3의 "대전충만교회 전경" 이미지를 미리 확보하거나 생성해두세요. Kling의 **Elements 기능**에 업로드하면 인물 외형·조명 톤·공간감을 일관되게 유지한 채 영상화할 수 있습니다. 교회 전경은 실제 사진을 이미지-투-비디오 소스로 쓰는 것이 가장 정확합니다.

### 2단계 — 컷별로 나눠서 생성 (Text/Image-to-Video)

10초를 한 번에 만들지 말고 3개 클립으로 분리 생성하세요. 표의 4초/3초/3초는 Kling 표준 길이(5초 단위)와 안 맞으므로, **각 컷을 5초로 생성한 뒤 편집 단계에서 정확히 트리밍**하는 게 현실적입니다.

- **컷1 프롬프트 예시**: `A lonely woman in her 50s sitting on a bed in a cold blue-grey dark room, head down, wide silhouette shot, scattered smartphone and worldly objects nearby, somber cinematic lighting, slow subtle breathing motion, 16:9`
- **컷2 프롬프트 예시**: `Same woman suddenly lifts her head, warm golden-orange lens flare bursts from upper right, dramatic lighting shift from cold to warm, hopeful expression, cinematic`
- **컷3 프롬프트 예시**: `Drone shot slowly rising over a warm sunlit church exterior, cross against clear sky, peaceful and welcoming atmosphere, cinematic aerial`

모션 강도는 낮게(0.3~0.5) 설정해 인물 왜곡을 방지하고, 동일 Seed 값을 컷1·컷2에 재사용하면 인물 일관성이 올라갑니다.

### 3단계 — 전환 효과(화이트아웃 플래시)

Kling이 생성한 컷 자체에 정확한 4초 타이밍의 화이트 플래시를 넣기는 어렵습니다. 컷1 마지막 프레임과 컷2 시작 프레임 사이에 **편집 툴에서 수동으로 화이트 플래시 1~2프레임 삽입**하는 게 훨씬 정확합니다.

### 4단계 — 오디오 생성

- **BGM**: O3 모델의 네이티브 오디오 생성으로 C마이너 패드음(0~4초)과 어쿠스틱 선율(4~10초) 시도 가능하나, 정확한 코드 지정은 어려우므로 무드 프롬프트(`heavy minor key ambient pad`, `warm bright acoustic melody`)로 생성 후 다듬으세요.
- **한국어 나레이션**: O3가 다국어 립싱크를 지원한다고는 하나 한국어 품질이 아직 검증되지 않았습니다. 결과가 부자연스러우면 **Typecast, Clova Dubbing, ElevenLabs 등 한국어 특화 TTS**로 별도 녹음 후 영상에 싱크하는 방식을 권장합니다.
- **윈드차임/종소리 SFX**: 4초 지점 효과음은 프리사운드 라이브러리 사용이 더 정확합니다.

### 5단계 — 자막(VFX Text) 삽입

Kling은 지정한 폰트·색상·위치의 자막을 그대로 렌더링하지 못합니다. 브리프에 명시된 "얇은 명조체 하단 배치", "두꺼운 고딕체 골드 옐로우" 등은 **Kling 영상 완성 후 Premiere/Capcut/After Effects에서 오버레이**로 작업하세요. 하단 고정 박스(교회 주소·전화번호)도 이 단계에서 삽입합니다.

### 6단계 — 최종 합성 및 편집

1. Kling 컷1(0~4초), 컷2(4~7초), 컷3(7~10초) 트리밍해 순서대로 배치
2. 화이트 플래시 전환, BGM, 나레이션, SFX, 자막을 타임라인에 정렬
3. 정확히 4초·7초 지점에 오디오/비주얼 큐가 맞는지 프레임 단위로 확인

### 7단계 — 인코딩 스펙 맞춰 내보내기

1080p, 24~30fps, H.264(비디오)/AAC(오디오)로 export. Kling 자체 다운로드본이 이 스펙과 다르면 편집 툴에서 최종 export 설정으로 통일하세요.

### 8단계 — 검수

완성본을 처음부터 재생하며 타이밍(4초 전환, 7초 교회 컷 진입), 자막 오탈자, 나레이션-자막 싱크, 인코딩 재생 여부를 확인합니다.

---

**요약**: Kling은 "영상 소스 생성" 담당, 자막·정밀 전환·한국어 나레이션 품질은 별도 편집 툴이 담당하는 하이브리드 워크플로우가 가장 현실적입니다.

Sources:

- [Kling AI 사용법 완벽 가이드: V3·O3 최신 기능부터 요금제까지 총정리](https://carat.im/blog/kling-ai-guide)
- [AI 비디오 캐릭터 일관성: 최종 가이드 (2026)](https://www.kling2-6.com/ko/blog/how-to-maintain-ai-character-consistency)
- [Kling AI의 신기능 Elements: 4개의 이미지로 일관된 비디오 생성하기](https://maily.so/trendium.ai/posts/3jrkpmk8o51)
- [클링AI(KlingAI) 사용법, 모션 컨트롤 제대로 쓰는 법과 실패하지 않는 팁](https://www.elancer.co.kr/blog/detail/1050)
- [Kling O3 AI 비디오 생성기 | 차세대 멀티모달 모델](https://klingo1.co/ko/kling-o3)
- [Kling O3 AI 비디오 생성기 | 세계 최초 통합 멀티모달 비디오 모델](https://kling26.net/ko/kling-o3)