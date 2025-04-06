<h1>dangerouslySetInnerHTML 속성</h1>
<p>HTML 문자열을 React 컴포넌트에 직접 삽입(render) 하고 싶을 때 사용하는 속성이다.
dangerously 가 붙은 이유는 XSS 공격(스크립트 삽입) 위험이 있기 때문이다.

```
function MyComponent() {
  const htmlString = "<p style='color: red;'>안녕하세요! <strong>굵게</strong> 표시됩니다.</p>";

  return (
    <div dangerouslySetInnerHTML={{ __html: htmlString }} />
  );
}
```

만약 외부 입력(사용자 작성 HTML) 을 그대로 넣으면 XSS 공격이 가능하다.
