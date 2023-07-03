## useCustomHttpHook
## useCustomHttpHook - це кастомний хук React для роботи з HTTP запитами.

## Встановлення
Відкрийте термінал та виконайте наступну команду:

### 'bash'

 Copy code

### 'npm install use-custom-http-hook' 

## Використання
Імпортуйте useCustomHttpHook в компонент React та використовуйте його для відправки HTTP запитів.

 javascript
# Copy code

### import React from 'react';
### import useCustomHttpHook from 'use-custom-http-hook';

### function App() {
 ### const { data, isLoading, error } = useCustomHttpHook('https://api.example.com', {});

 ### if (isLoading) {
 ###   return <div>Завантаження...</div>; }

 ### if (error) {
  ###  return <div>Помилка: {error.message}</div>;}

 ### return <div>{JSON.stringify(data)}</div>;}

### export default App;
## API
### useCustomHttpHook приймає наступні параметри:

#### url (string): URL, куди відправляється запит.
#### options (object): параметри для fetch запиту.
#### useCustomHttpHook повертає об'єкт з наступними полями:

#### data (object | null): дані, отримані з запиту, або null, якщо дані ще не отримано.
#### isLoading (boolean): вказує, чи триває завантаження даних.
#### error (object | null): об'єкт помилки, якщо виникла помилка під час виконання запиту.