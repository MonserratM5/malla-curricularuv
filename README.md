# malla-curricularuv
Malla curricular interactiva de Ingeniería en Negocios Internacionales - Universidad de Valparaíso
<!DOCTYPE html>
<html>
<head>
  <title>Malla Interactiva - Ingeniería en Negocios Internacionales</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #fff0f5;
      padding: 20px;
      color: #5a2a4d;
    }
    h1 {
      text-align: center;
      margin-bottom: 30px;
    }
    table {
      width: 100%;
      border-collapse: collapse;
      background: white;
      box-shadow: 0 0 10px rgba(202, 114, 150, 0.3);
    }
    th, td {
      border: 1px solid #cda1b6;
      padding: 12px;
      text-align: left;
    }
    th {
      background-color: #f9c2d1;
      font-weight: bold;
      text-align: center;
    }
    tr.aprobado td.ramo {
      text-decoration: line-through;
      color: gray;
    }
  </style>
</head>
<body>

  <h1>Malla Curricular Interactiva</h1>
  <p>Marca los ramos que ya aprobaste para que se tachen.</p>

  <table>
    <thead>
      <tr>
        <th>Semestre</th>
        <th>Ramo</th>
        <th>Aprobado</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td style="text-align:center;">1°</td>
        <td class="ramo">Álgebra</td>
        <td style="text-align:center;">
          <input type="checkbox" onchange="toggleAprobado(this)">
        </td>
      </tr>
      <tr>
        <td style="text-align:center;">1°</td>
        <td class="ramo">Gestión de Organizaciones</td>
        <td style="text-align:center;">
          <input type="checkbox" onchange="toggleAprobado(this)">
        </td>
      </tr>
      <tr>
        <td style="text-align:center;">1°</td>
        <td class="ramo">Habilidades Comunicacionales</td>
        <td style="text-align:center;">
          <input type="checkbox" onchange="toggleAprobado(this)">
        </td>
      </tr>
      <!-- Agrega más ramos aquí -->
    </tbody>
  </table>

  <script>
    function toggleAprobado(checkbox) {
      const fila = checkbox.closest('tr');
      if (checkbox.checked) {
        fila.classList.add('aprobado');
      } else {
        fila.classList.remove('aprobado');
      }
    }
  </script>

</body>
</html>
