import { useState } from "react";

function App() {
  const [formValue, setFormValue] = useState({
    name: "",
    email: "",
  });

  const [allData, setAllData] = useState([]);
  const handleEvent = (e) => {
    setFormValue({ ...formValue, [e.target.name]: e.target.value });
  };
  const submitHandler = (e) => {
    e.preventDefault();
    setAllData([...allData, formValue]);
    resetForm();
  };

  const table = allData?.map((item) => item);

  const resetForm = () => {
    setFormValue({
      name: "",
      email: "",
    });
  };

  return (
    <>
      <form>
        <input
          type="text"
          placeholder="Name"
          name="name"
          value={formValue.name}
          onChange={handleEvent}
        />
        <input
          type="text"
          placeholder="Email"
          name="email"
          value={formValue.email}
          onChange={handleEvent}
        />
        <button type="button" onClick={submitHandler}>
          submit
        </button>
      </form>

      <br />

      <table style={{ border: "1px solid grey" }}>
        <tbody>
          <tr>
            <th style={{ border: "1px solid grey" }}>S.no</th>
            <th style={{ border: "1px solid grey" }}>Name</th>
            <th style={{ border: "1px solid grey" }}>Email</th>
          </tr>
          {allData?.map((item, index) => (
            <tr key={index}>
              <td style={{ border: "1px solid grey" }}>{index + 1}</td>
              <td style={{ border: "1px solid grey" }}>{item.name}</td>
              <td style={{ border: "1px solid grey" }}>{item.email}</td>
            </tr>
          ))}
        </tbody>
      </table>
    </>
  );
}

export default App;
