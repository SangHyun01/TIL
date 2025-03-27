<h1>React.memo와 useCallback() 의 차이</h1>
<p>둘 다 불필요한 렌더링을 방지하는 역할이지만 <strong>memo</strong>는 컴포넌트 자체의 불필요한 렌더링을 방지하고, <strong>useCallback()</strong>은 함수가 계속 생성되는 것을 방지한다. 따라서 함수형 컴포넌트에서 props로 함수를 전달할 때, useCallback과 memo를 함께 사용하면 좋다.
