# [AI 도구 학습] 멀티모달 콘텐츠 제작 최종 과제 보고서

## 1. 브랜드 아이덴티티 및 캠페인 정의

- **브랜드명**: 리턴 (Re:Turn) — _내 삶의 방향을 예수님께로 돌리다_
    
- **타겟**: 인본주의 사조 속에서 극심한 경쟁 위주 사회에 신음하는 10~20대 현대 청년들
    
- **톤앤매너**: 시네마틱, 다크 디지털 아트에서 신성하고 따뜻한 금빛(Divine Grace)으로의 반전, 희망찬 웰컴 톤
    
- **차별점 (USP)**: 청년들의 현실적 고통(경쟁)을 위로하고, 오직 ‘영접’이라는 단순하고 명확한 구원의 메시지를 제시한 뒤, 교회를 통한 공동체적 ‘성장’으로 연결
    
- **핵심 메시지 (한 문장)**: **"예수님은 단지 당신이 그 손을 잡고 영접하기만을 기다리십니다."**
    
- **광고 목적**: 인지 및 전환 (고통받는 청년들을 위로하고 대전충만교회 출석 권유)
    

## 2. 사용 도구 목록 및 파이프라인 설계

멀티모달 제작의 효율성과 맥락 제어의 용이성을 고려하여 **[세트 B]** 조합을 최종 선택하여 파이프라인을 구축했습니다.

- **이미지 생성**: **DALL-E 3** (선택 이유: 한국인 청년의 정서와 종교적 맥락, 교회 이름 등의 텍스트 삽입을 가장 직관적이고 정확하게 반영함)
    
- **비디오 생성**: **Runway Gen-3 Alpha** (선택 이유: 텍스트 프롬프트 제어력이 높아 원본 이미지의 화풍을 깨지 않고 정밀한 모션을 연출함)
    
- **오디오 생성**: **ElevenLabs** (선택 이유: 자연스럽고 감정선이 살아있는 AI 보이스 내레이션 및 고품질 효과음 동시 생성 가능)
    
- **최종영상 제작(통합 편집)**: **Vrew** (선택 이유: 음성 인식을 통한 자동 자막 매칭과 컷 편집이 직관적이며 10초 타임라인 제어에 용이함)
    
- **도구 접근성 제한 대비 대체 도구**: Midjourney(이미지 대안) / Kling, Luma(비디오 대안) / Suno, Udio(오디오 대안)
    

## 3. 씬(Scene)별 스토리보드 상세

### 🎬 씬 1 (Intro: 0~3초)

- **씬 길이**: 3초
    
- **목적**: 무한 경쟁 사회 속에서 출구를 찾지 못해 고립된 청년의 고통 시각화
    
- **화면 구성**: 차가운 블루·그레이 톤의 삭막한 미래 도시 빌딩 숲 밤거리, 홀로 주저앉아 고개를 숙이고 무력감을 느끼는 20대 한국인 청년의 뒷모습.
    
- **내레이션 (카피)**: "끝없는 경쟁, 탈출구는 없을까?"
    
- **사용 도구 및 목적**:
    
    - 이미지: DALL-E 3 (고립된 청년의 다크 시네마틱 키 비주얼 확보)
        
    - 비디오: Runway Gen-3 Alpha (배경 네온사인만 타임랩스로 빠르게 흐르게 하여 청년의 멈춰진 절망감 극대화)
        
    - 오디오: ElevenLabs (낮고 차분한 청년 남성 AI 보이스 생성)
        
- **입력 프롬프트 (원문)**:
    
    - _DALL-E 3_: `A cinematic 3d digital art style illustration of a lonely 20-year-old South Korean male youth, sitting on the cold dark street corner of a futuristic neon-lit city at night. He is holding his head in his hands, looking completely exhausted and full of despair from fierce competition. Cold blue and grey color palette, dark moody atmosphere, soft dramatic lighting, ultra-detailed.`
        
    - _Runway_: `Slow subtle breathing motion of the young man sitting on the street. In the background, the neon signs of the high-rise buildings flicker rapidly and traffic lights blur past in a time-lapse effect. Dramatic low angle, camera stays still, high contrast, continuous cinematic movement.`
        
- **출력 결과 요약**: 차가운 도시 질감과 청년의 고립감이 대비되는 3초 오프닝 영상 소스 완성
    
- **생성 파일명**: `scene01_image.jpg` / `scene01_video.mp4` / `scene01_narration.mp3`
    

### 🎬 씬 2 (Body: 3~7초)

- **씬 길이**: 4초
    
- **목적**: 예수님이 기다리고 계시며, 오직 그를 영접하기만 하면 된다는 구원의 핵심 메시지 전달
    
- **화면 구성**: 어둠을 깨고 쏟아지는 따뜻한 금빛 줄기. 인자한 실루엣의 예수님 손이 다가와 청년의 차가운 손을 위로하듯 포개어 맞잡음.
    
- **내레이션 (카피)**: "예수님이 널 기다리셔. 오직 영접함으로."
    
- **사용 도구 및 목적**:
    
    - 이미지: DALL-E 3 (구원과 따뜻한 온기가 느껴지는 두 손의 클로즈업 이미지 생성)
        
    - 비디오: Runway Gen-3 Alpha (두 손이 맞잡히는 순간 황금빛 광원이 폭발하듯 퍼져나가는 극적 연출)
        
    - 오디오: ElevenLabs (따뜻하고 울림이 있는 위로 톤의 보이스 및 빛 확산 효과음 생성)
        
- **입력 프롬프트 (원문)**:
    
    - _DALL-E 3_: `A cinematic 3d digital art style illustration, close-up shot of two hands connecting. A warm, glowing golden hand of Jesus Christ is gently holding and lifting up the cold, trembling hand of the exhausted South Korean young man. Divine bright golden light emitting from the center of the touch, breaking the darkness. Emotional, hopeful, divine grace, soft dramatic lighting.`
        
    - _Runway_: `The two hands firmly and gently clasp together. At the exact moment of the touch, a massive burst of warm golden light emanates from the palms, rapidly spreading across the screen and washing away the dark blue shadows. Smooth continuous motion, cinematic lighting shift.`
        
- **출력 결과 요약**: 어둠에서 빛으로 전환되며 감정을 극대화하는 4초 클라이맥스 소스 완성
    
- **생성 파일명**: `scene02_image.jpg` / `scene02_video.mp4` / `scene02_narration.mp3` / `scene02_sfx.mp3`
    

### 🎬 씬 3 (Outro / CTA: 7~10초)

- **씬 길이**: 3초
    
- **목적**: 교회 출석을 통한 영적 성장 도모 및 최종 목적인 대전충만교회 출석 권유 (CTA)
    
- **화면 구성**: 푸르고 희망찬 하늘 아래 모던하고 아름다운 교회 건물 외관. 상단에 **'대전충만교회'** 문구가 깔끔하게 인그레이빙되어 있음. 평안한 표정의 청년이 활짝 열린 교회 문 안쪽의 밝은 빛을 향해 걸어 들어감.
    
- **내레이션 (카피)**: (자막 동시 출력) "함께 성장하는 곳, 대전충만교회"
    
- **사용 도구 및 목적**:
    
    - 이미지: DALL-E 3 (정확한 한글 타이포그래피가 적용된 대전충만교회 전경 이미지 생성)
        
    - 비디오: Runway Gen-3 Alpha (교회와 십자가를 향해 부드럽게 무빙하는 슬로우 카메라 트래킹 카메라 워크 연출)
        
    - 오디오: ElevenLabs (신뢰감 있고 또렷하게 마무리지어 주는 내레이션 보이스 생성)
        
- **입력 프롬프트 (원문)**:
    
    - _DALL-E 3_: `A cinematic 3d digital art style illustration of a modern, beautiful church building exterior with a clear glowing cross. Above the entrance door, the Korean text '대전충만교회' is clearly and elegantly engraved in a clean font. The South Korean young man, now looking peaceful, is walking towards the wide-open, bright doors of the church. Sunny day, hopeful atmosphere, volumetric lighting.`
        
    - _Runway_: `Smooth slow cinematic camera tracking shot behind the young man as he walks towards the bright open entrance of the church. The camera gently pans up towards the glowing cross and the text '대전충만교회'. Warm sun flares, inspirational and welcoming atmosphere, seamless movement.`
        
- **출력 결과 요약**: 브랜드(교회명) 인지와 초청의 메시지가 명확히 전달되는 3초 엔딩 컷 완성
    
- **생성 파일명**: `scene03_image.jpg` / `scene03_video.mp4` / `scene03_narration.mp3`
    

## 4. 프롬프트 엔지니어링 개선 로그 (요약)

- **개선 대상**: 씬 2 (구원과 영접) 이미지 생성 단계
    
- **수정 전 프롬프트**: `A man meeting Jesus and holding hands in dark city, holy light.`
    
    - _문제점_: 인물의 생김새가 서양인 가이드라인으로 무작위 생성되었고, 손을 잡는 구도가 부자연스러우며, 배경인 도시와 신성한 광원이 뭉개져 브랜드가 추구하는 세련된 3D 디지털 아트 느낌이 살지 않음.
        
- **수정 후 프롬프트**: `A cinematic 3d digital art style illustration, close-up shot of two hands connecting. A warm, glowing golden hand of Jesus Christ is gently holding and lifting up the cold, trembling hand of the exhausted South Korean young man... (이하 씬2 원문과 동일)`
    
- **개선 결과**: 화풍의 스타일(`3d digital art style`)을 명확히 지정하고 인물의 국적(`South Korean`) 및 감정 상태(`exhausted`, `trembling`), 광원의 세부 묘사(`glowing golden hand`)를 명시하여 타겟층(청년)이 몰입할 수 있는 완벽한 톤앤매너 일관성을 확보함.
    

## 5. 최종 통합 편집 전략 및 영상 스펙

- **편집 도구**: **Vrew**
    
- **통합 방식**:
    
    1. ElevenLabs에서 생성한 오디오 소스 3개를 순서대로 임포트하여 AI 가독성 자막 라인을 자동 매칭함.
        
    2. 각 내레이션 음성 길이에 맞춰 Runway에서 제작한 3개의 영상 클립(mp4)을 배치 및 미세 컷 편집함.
        
    3. 씬 2가 시작되는 3초 타임라인 지점에 `scene02_sfx.mp3` 효과음을 레이어링하여 시청각적 반전 효과를 극대화함.
        
    4. 7~10초 엔딩 구간(씬 3)에는 화면 하단에 대전충만교회의 실제 로고 이미지와 약도 자막을 오버레이 고정하여 최종 브랜딩 장치(CTA)를 완성함.
        

### 🎬 최종 출력 영상 파일 스펙

- **파일명**: `Return_Branding_DaejeonChungman.mp4`
    
- **길이**: 10초
    
- **해상도**: 1920x1080 (16:9 가로형 표준 광고 스펙)
    
- **프레임레이트**: 30fps
    
- **비디오 코덱**: H.264
    
- **오디오 코덱**: AAC