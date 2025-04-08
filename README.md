# [ParamEditor](https://github.com/Dmitiy/ParamEditor.git)

- The `ParamEditor` component is a `React class component` designed to edit a `Model` structure by allowing users to set values for parameters (`Param[]`). It provides an interface for rendering all parameters for editing and ensures that the passed values are displayed in the editing form. The component supports only text-based parameters (`type: 'string'`).

- Features:
- - Displays all parameters (`Param[]`) for editing.
- - Allows users to modify parameter values (`ParamValue[]`) in the `Model`.
- - Provides a method `getModel()` to retrieve the complete `Model` structure,
- - including all updated parameter values.
- - Designed to be easily extensible for adding new parameter types (e.g., numeric or dropdown values) in the future.

- Uses TypeScript for type safety and better development experience.

- Interfaces:
- - `Param`: Represents a parameter with an ID, name, and type.
- - `ParamValue`: Represents a value associated with a parameter ID.
- - `Model`: Represents the structure containing parameter values and additional properties like `colors`.
- - `Props`: Defines the props for the `ParamEditor` component, including `params` and `model`.

## Example Usage:

```javascript
const params = [
  { id: 1, name: 'Назначение', type: 'string' },
  { id: 2, name: 'Длина', type: 'string' },
];
const model = {
  paramValues: [
    { paramId: 1, value: 'повседневное' },
    { paramId: 2, value: 'макси' },
  ],
  colors: [],
};
```

```javascript
<ParamEditor params={params} model={model} />
```
