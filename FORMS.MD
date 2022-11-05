Watchlist

```
import React from 'react';
import { useForm } from 'react-hook-form';

export default function App() {
  const { register, handleSubmit, formState: { errors } } = useForm();
  const onSubmit = data => console.log(data);
  console.log(errors);
  
  return (
    <form onSubmit={handleSubmit(onSubmit)}>
      <input type="text" placeholder="Title" {...register("Title", {required: true, max: 100, min: 3})} />
      <textarea {...register("Description", {})} />
      <input type="undefined" placeholder="Is Public" {...register} />

      <input type="submit" />
    </form>
  );
}
```
