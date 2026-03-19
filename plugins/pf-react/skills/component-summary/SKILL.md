Read a React component file and output a quick-reference summary for someone who hasn't seen the component before.

## Input

The user will provide a component file path. Read the file before generating the summary.

## Output

### 1. What it does

1-2 sentences explaining the component's purpose and behavior in plain English. Focus on what a consumer needs to know, not implementation details.

### 2. Props

A table of all props:

| Prop | Type | Default | Description |
|------|------|---------|-------------|
| name | `string` | — | What this prop controls |

- Pull types from the Props interface/type, inline destructuring defaults, or `defaultProps`.
- Use `—` for required props with no default.
- Keep descriptions to a few words.
- If the component accepts no props, skip the table and say "This component accepts no props."

### 3. Usage

A minimal JSX code block showing how to use the component with only the required props and one or two common optional ones. Use realistic but concise placeholder values.

```tsx
import { ComponentName } from './ComponentName';

<ComponentName requiredProp="value" />
```

## Rules

- Read the actual file — never guess or hallucinate props.
- If the component uses `forwardRef`, note the ref type in the description.
- Don't add commentary beyond the three sections.
