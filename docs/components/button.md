<script setup>
import ExampleSection from "../components/demo/ExampleSection.vue";
</script>

# 버튼

버튼 컴포넌트는 사용자와의 상호작용을 위한 컴포넌트입니다. 주로 사용자의 액션을 나타낼 때 사용됩니다.

## 모아보기

### 타입

`filled`, `outline-box`, `void` 타입이 제공됩니다. 자세한 내용을 보려면 [여기](#type)를 클릭하세요.

<div class="n-item d:flex jc:center gap:2 mt:4">
  <button class="n-btn">Button</button>
  <button class="n-btn n-btn:outline-box">Button</button>
  <button class="n-btn n-btn:void">Button</button>
</div>

### 사이즈

`small`, `medium`, `large` 사이즈가 제공됩니다. 자세한 내용을 보려면 [여기](#size)를 클릭하세요.

<div class="n-item d:flex jc:center gap:2 ai:end mt:4">
  <button type="button" class="n-btn n-btn-size:1">Button</button>
  <button type="button" class="n-btn n-btn-size:2">Button</button>
  <button type="button" class="n-btn n-btn-size:3">Button</button>
</div>

### 색상

`main`, `sub`, `accent`, `base` 색상이 제공됩니다. 자세한 내용을 보려면 [여기](#color)를 클릭하세요.

<div class="n-item d:flex jc:center gap:2 mt:4">
  <button type="button" class="n-btn n-btn-color:main">Button</button>
  <button type="button" class="n-btn n-btn-color:sub">Button</button>
  <button type="button" class="n-btn n-btn-color:accent">Button</button>
  <button type="button" class="n-btn n-btn-color:base">Button</button>
</div>

### 상태

`disabled` 상태가 제공됩니다. 자세한 내용을 보려면 [여기](#disabled)를 클릭하세요.

<div class="n-item d:flex jc:center gap:2 mt:4">
  <button type="button" class="n-btn" disabled>Button</button>
</div>

## 사용법

버튼 컴포넌트는 요소에 `n-btn` 클래스를 적용하여 사용할 수 있습니다.

<ExampleSection>
  <button type="button" class="n-btn">Button</button>
</ExampleSection>

```html
<button type="button" class="n-btn">Button</button>
```

::: details CSS details

```css
.n-btn {
  /* ... */
  color: var(--color-base-1);
  border: 1px solid transparent;
  background-color: var(--color-main-2);

  height: 36px;
  padding-top: 4px;
  padding-left: 16px;
  padding-right: 16px;
  padding-bottom: 4px;
  /* ... */
}
```

:::

## 타입 {#type}

`n-btn-type:타입` 또는 `n-btn:타입` 약어 클래스를 통해 다양한 버튼 타입을 적용할 수 있습니다.

<ExampleSection>
  <template #h>버튼 타입</template>
  <div class="d:flex gap:2 jc:center">
    <button class="n-btn">filled</button>
    <button class="n-btn n-btn:outline-box">outline</button>
    <button class="n-btn n-btn:void">void</button>
  </div>
</ExampleSection>

```html
<button type="button" class="n-btn n-btn-type:filled">filled</button>
<button type="button" class="n-btn n-btn-type:outline">outline</button>
<button type="button" class="n-btn n-btn-type:void">void</button>
```

<table>
  <thead>
    <tr>
      <th scope="col">타입</th>
      <th scope="col">클래스</th>
      <th scope="col">약어 클래스</th>
      <th scope="col">변수</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>filled</td>
      <td>
        <code>n-btn-type:filled</code>
      </td>
      <td>
        <code>n-btn:filled</code>
      </td>
      <td>
        <span class="code">
          .n-btn { <br/> 
            --btn-filled-background-color: var(--color-main-2); <br/>
            --btn-filled-color: var(--color-base-1); <br/>
          }
        </span>
      </td>
    </tr>
    <tr>
      <td>outline-box</td>
      <td>
        <code>n-btn-type:outline-box</code> <br/>
        <code>n-btn-type:outline</code>
      </td>
      <td>
        <code>n-btn:outline-box</code> <br/>
        <code>n-btn:outline</code> <br/>
      </td>
      <td>
        <span class="code">
          .n-btn { <br/> 
            --btn-outline-border-color: var(--color-base-3); <br/>
            --btn-outline-color: inherit; <br/>
          }
        </span>
      </td>
    </tr>
    <tr>
      <td>void</td>
      <td>
        <code>n-btn-type:void</code>
      </td>
      <td>
        <code>n-btn:void</code>
      </td>
      <td>
      </td>
    </tr>
  </tbody>
</table>

## 사이즈 {#size}

`n-btn-size:사이즈` 클래스를 통해 버튼 사이즈를 변경할 수 있습니다.

<ExampleSection>
  <template #h>버튼 사이즈</template>
  <div class="d:flex gap:2 jc:center ai:end">
    <button class="n-btn n-btn-size:1">Button</button>
    <button class="n-btn n-btn-size:2">Button</button>
    <button class="n-btn n-btn-size:3">Button</button>
  </div>
</ExampleSection>

```html
<button type="button" class="n-btn n-btn-size:1">Button</button>
<button type="button" class="n-btn n-btn-size:2">Button</button>
<button type="button" class="n-btn n-btn-size:3">Button</button>
```

<table>
  <thead>
    <tr>
      <th scope="col">사이즈</th>
      <th scope="col">클래스</th>
      <th scope="col">변수</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td><code>n-btn-size:1</code></td>
      <td>
        <span class="code">
          .n-btn { <br/> 
            --btn-height-1: 28px; <br/>
            --btn-padding-1: 4px 12px; <br/>
            --btn-font-size-1: 14px; <br/>
          }
        </span>
      </td>
    </tr>
    <tr>
      <td>2</td>
      <td><code>n-btn-size:2</code></td>
      <td>
        <span class="code">
          .n-btn { <br/> 
            --btn-height-2: 36px; <br/>
            --btn-padding-2: 4px 16px; <br/>
            --btn-font-size-2: 14px; <br/>
          }
        </span>
      </td>
    </tr>
    <tr>
      <td>3</td>
      <td><code>n-btn-size:3</code></td>
      <td>
        <span class="code">
          .n-btn { <br/> 
            --btn-height-3: 44px; <br/>
            --btn-padding-3: 4px 20px; <br/>
            --btn-font-size-3: 16px; <br/>
          }
        </span>
      </td>
    </tr>
  </tbody>
</table>

## 색상 {#color}

`n-btn-color:색상` 클래스를 통해 버튼의 색을 변경할 수 있습니다.

:::raw
<ExampleSection>

  <ul class="d:flex gap:4">
    <li>
      <button type="button" class="n-btn n-btn-color:main" style="width: 70px;">
        main
      </button>
    </li>
    <li>
      <button type="button" class="n-btn n-btn-color:sub" style="width: 70px;">
        sub
      </button>
    </li>
    <li>
      <button type="button" class="n-btn n-btn-color:accent" style="width: 70px;">
        accent
      </button>
    </li>
    <li>
      <button type="button" class="n-btn n-btn-color:base" style="width: 70px;">
        base
      </button>
    </li>
  </ul>
</ExampleSection>
:::

```html
<button type="button" class="n-btn n-btn-color:main">main</button>
<button type="button" class="n-btn n-btn-color:sub">sub</button>
<button type="button" class="n-btn n-btn-color:accent">accent</button>
<button type="button" class="n-btn n-btn-color:base">base</button>
```

| 색상   | 클래스               |
| ------ | -------------------- |
| main   | `n-btn-color:main`   |
| sub    | `n-btn-color:sub`    |
| accent | `n-btn-color:accent` |
| base   | `n-btn-color:base`   |

## 비활성화 {#disabled}

`disabled` 속성을 추가하거나 클래스에 `disabled`를 추가하여 버튼 컴포넌트에 비활성화 스타일을 적용할 수 있습니다.

:::raw
<ExampleSection>

  <ul class="d:flex gap:4">
    <li>
      <button type="button" class="n-btn" disabled>filled</button>
    </li>
    <li>
      <button type="button" class="n-btn n-btn:outline disabled">outline</button>
    </li>
    <li>
      <button type="button" class="n-btn n-btn:void" disabled>void</button>
    </li>
  </ul>
</ExampleSection>
:::

```html
<button type="button" class="n-btn" disabled>filled</button>
<button type="button" class="n-btn n-btn:outline disabled">outline</button>
<button type="button" class="n-btn n-btn:void" disabled>void</button>
```

## 스타일 재정의 {#overriding}

버튼 컴포넌트는 버튼의 크기 및 모서리의 둥글기 정도를 조절할 수 있는 변수를 제공합니다. 해당 변수를 오버라이딩하여 버튼의 크기와 모서리 둥글기를 자유롭게 재정의 할 수 있습니다.
또한, 버튼 스타일 중 `filled`, `outline` 타입의 변수를 오버라이딩하여 스타일을 재정의 할 수 있습니다.

```css
.n-btn {
  /* btn-size:1 */
  --btn-height-1: 28px;
  --btn-padding-1: 4px 12px;
  --btn-font-size-1: 14px;

  /* btn-size:2 */
  --btn-height-2: 36px;
  --btn-padding-2: 4px 16px;
  --btn-font-size-2: 14px;

  /* btn-size:3 */
  --btn-height-3: 44px;
  --btn-padding-3: 4px 20px;
  --btn-font-size-3: 16px;

  /* btn-type:filled */
  --btn-filled-background-color: var(--color-main-2);
  --btn-filled-color: var(--color-base-1);

  /* btn-type:outline */
  --btn-outline-border-color: var(--color-base-3);
  --btn-outline-color: inherit;
}
```

### 스타일 재정의 예시

<ExampleSection class="my:4">
  <div class="d:flex ai:center gap:2">
    <button type="button" class="n-btn n-btn:void" style="height:24px; padding: 0 8px; font-size:12px; border-radius:6px;">Button</button>
    <button type="button" class="n-btn" style="height:32px; padding: 0 12px; font-size:14px; border-radius:6px; background-color:#3182ce; color:#1E293B;">Button</button>
    <button type="button" class="n-btn n-btn:outline" style="height:40px; padding: 0 16px; font-size:16px; border-radius:6px; border-color:#3182ce; color:#3182ce;">Button</button>
  </div>
</ExampleSection>

```html
<button type="button" class="n-btn n-btn:void n-btn-size:1">Button</button>
<button type="button" class="n-btn n-btn:filled n-btn-size:2">Button</button>
<button type="button" class="n-btn n-btn:outline n-btn-size:3">Button</button>
```

```css
.n-btn {
  /* btn-size:1 */
  --btn-height-1: 24px;
  --btn-padding-1: 0px 8px;
  --btn-font-size-1: 12px;

  /* btn-size:2 */
  --btn-height-2: 32px;
  --btn-padding-2: 0px 12px;
  --btn-font-size-2: 14px;

  /* btn-size:2 */
  --btn-height-3: 40px;
  --btn-padding-3: 0px 16px;
  --btn-font-size-3: 16px;

  /* btn-border-radius */
  --btn-border-radius: 6px;

  /* btn-type:filled */
  --btn-filled-background-color: #3182ce;
  --btn-filled-color: #1e293b;

  /* btn-type:outline */
  --btn-outline-border-color: #3182ce;
  --btn-outline-color: #3182ce;
}
```

:::tip
컴포넌트 스타일 재정의에 대한 자세한 내용은 [스타일 재정의하기](/guide/customizing)에서 확인하실 수 있습니다.
:::

## 활용 예시 {#examples}

<ExampleSection class="mb:4">
  <div class="d:flex gap:2">
    <button type="button" class="n-btn n-btn:void">취소</button>
    <button type="button" class="n-btn">확인</button>
  </div>
</ExampleSection>

::: details codes

```html
<div class="d:flex gap:2">
  <button type="button" class="n-btn n-btn:void">취소</button>
  <button type="button" class="n-btn">확인</button>
</div>
```

:::

<ExampleSection class="mb:4">
  <div class="d:flex gap:2">
    <button type="button" class="n-btn n-btn:outline">닫기</button>
    <button type="button" class="n-btn n-btn-color:accent">삭제</button>
  </div>
</ExampleSection class="mb:4">

::: details codes

```html
<div class="d:flex gap:2">
  <button type="button" class="n-btn n-btn:outline">닫기</button>
  <button type="button" class="n-btn n-btn-color:accent">삭제</button>
</div>
```

:::

<ExampleSection class="mb:4">
  <button type="button" class="n-btn n-btn:outline px:2">
    <span class="icon icon:share_fat_fill icon-color:base-7 icon-size:3">공유</span>
  </button>
</ExampleSection>

::: details codes

```html
<button type="button" class="n-btn n-btn:outline px:2">
  <span class="icon icon:share_fat_fill icon-color:base-7 icon-size:3"
    >공유</span
  >
</button>
```

:::

<ExampleSection>
  <button type="button" class="n-btn n-btn:outline ">
    <span class="deco deco-position:right deco-size:3 icon:trash icon-color:base-7">삭제</span>
  </button>
</ExampleSection>

::: details codes

```html
<button type="button" class="n-btn n-btn:outline ">
  <span
    class="deco deco-position:right deco-size:3 icon:trash icon-color:base-7"
    >삭제</span
  >
</button>
```

:::