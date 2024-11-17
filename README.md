# konglog
세상에서 제일 예쁜 내 고양이 콩이 자랑 겸 개발 블로그

# 기능
- 게시글 목록(전체, 카테고리 별, 페이지네이션)
- 게시글 상세 페이지
- 댓글(대댓글)
- 다크/라이트 모드
- 조회수 표시
- 태그 표시
- 최상단, 최하단으로 이동
- 게시글 주소 복사
- scroll progress status bar
- 검색 엔진 최적화 (SEO)
- 글 읽는 소요시간

# 기술스택
- NextJS 14 이상
- tailwind
- vercel
- Supabase

# DB
- 게시글(post) 
  - post_id, 생성일(create_date), 수정일(update_date), 제목(title), 본문(content, nullable), 썸네일(thumbnail, nullable), 부제목(sub_title, 목록에서 보이는 요약, nullable)
- 조회수(view_count)
  - post_id(fk), 조회수(count), 조회일시(view_date)
- 태그(tag)
  - tag_id, 이름(name), 생성일(create_date)
- 게시글_태그(post_tag) - n:n 매핑이기 때문에 매핑테이블 생성
