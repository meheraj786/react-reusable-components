# ⚛️ React + Tailwind Reusable UI Components

A collection of simple and reusable **React components** styled with **Tailwind CSS** to speed up your front-end development.

---

## 📦 Components Included

- 🔘 [Button](#-button)
- 📦 [Container](#-container)
- 🧱 [Flex](#-flex)
- 📝 [Input](#-input)

---

## 🔘 Button

A reusable button component with default Tailwind styling. Easily customizable using `className`.


```jsx

import React from 'react'

const Button = ({ children, onClick, className = "", type = "button" }) => {
  return (
    <button
      type={type}
      onClick={onClick}
      className={`px-4 py-2 bg-blue-500 text-white rounded hover:bg-blue-600 ${className}`}
    >
      {children}
    </button>
  );
};

export default Button;

import React from 'react'

const Container = ({ children, className = "" }) => {
  return (
    <div className={`max-w-6xl mx-auto ${className}`}>
      {children}
    </div>
  );
};

export default Container;

import React from 'react'

const Flex = ({
  children,
  className = "",
}) => {
  return (
    <div
      className={`flex ${className}`}
    >
      {children}
    </div>
  );
};

export default Flex;

import React from 'react'

const Input = ({ value, onChange, placeholder = "", className = "", type = "text" }) => {
  return (
    <input
      type={type}
      value={value}
      onChange={onChange}
      placeholder={placeholder}
      className={`border px-3 py-2 rounded w-full ${className}`}
    />
  );
};

export default Input;

