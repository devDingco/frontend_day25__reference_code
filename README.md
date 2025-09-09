## 과제 요구 사항

### 공통

- [ ]  완성된 `day25` 폴더를 활용하여 `day26` 을 완성해 주세요.
    - 폴더를 다시 생성할 필요는 없습니다 !
    - 해당 폴더에서 계속 작업해서 과제 제출해 주시면 됩니다.

### 게시글 등록/수정

- [ ]  게시글 등록/수정 페이지에서 렌더링 되는 게시글작성 컴포넌트를 리팩토링해요.
    - 주어진 폴더 경로에 파일을 만들고 코드를 적절히 이동합니다.
    - 폴더 경로: `src/components/boards-write`
    - 파일 목록:
        - hook.ts
        - index.tsx
        - queries.ts
        - styles.module.css
        - types.ts

### 게시글 상세

- [ ]  게시글 상세 페이지에서 게시글 상세 컴포넌트를 불러오도록 리팩토링해요.
    - 주어진 폴더 경로에 파일을 만들고 코드를 적절히 이동합니다.
    - 폴더 경로: `src/component/boards-detail`
    - 파일 목록:
        - hook.ts
        - index.tsx
        - queries.ts
        - styles.module.css
        - types.ts
- [ ]  게시글 상세 페이지는 새롭게 만든 컴포넌트가 렌더링 될 수 있도록 변경합니다.
    - 게시글 상세 페이지 경로: `app/boards/[boardId]/page.tsx`

### 게시글 목록

- [ ]  게시글 목록 페이지에서 게시글 목록 컴포넌트를 불러오도록 리팩토링해요.
    - 주어진 폴더 경로에 파일을 만들고 코드를 적절히 이동합니다.
    - 폴더 경로: `src/component/boards-list`
    - 파일 목록:
        - hook.ts
        - index.tsx
        - queries.ts
        - styles.module.css
        - types.ts

### 타입 스크립트

- [ ]  GraphQL API와 관련된 데이터의 타입을 모두 보완해요.
- [ ]  graphql-codegen 을 설치해요.
    - 명령어: `pnpm add --dev @graphql-codegen/cli`
- [ ]  `codegen.ts` 파일을 복사 후 아래 내용을 변경하세요.
    - schema: `"http://main-practice.codebootcamp.co.kr/graphql"`
- [ ]  `package.json` 의 script에 실행 명령을 추가해 주세요.
    - `"codegen"`: `"graphql-codegen --config codegen.ts"`
- [ ]  codegen 을 통해 생성한 타입이 적용된 Document 를 통해 모든 `useQuery`, `useMutation` 을 변경해요.
    - `any` 타입으로 정의된 API 관련 데이터 타입은 없어야 합니다.
    - 예시:
        - 게시글등록 => useMutation(CreateBoardDocument)
