<script>
        $.getJSON("stored/personal.json", function (data) {
            data.content.forEach(f => {
                let tblRow = `
                <tr>
                    <td>${f.name}</td>
                    ${f.args ? `<td>[${f.args}]</td>` : `<td></td>` }
                    <td>${f.description}</td>
                   
                </tr>`;
                $(tblRow).appendTo("#personal");
            });
        });
    </script>

<table>
    <thead>
     <th>Command Name</th>
       <th>Args</th>
       <th>Description</th>
      </thead>
    <tbody id="personal">
 </tbody>
 </table>
