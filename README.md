# syoes03.github.io
<head>
	<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
	<script>
		$(function () {
			var people = [];

			$.getJSON("stored/personal.json", function (data) {
				$.each(data.content, function (i, f) {
					var tblRow =
						"<tr>" +
						"<td>" +
						f.name +
						"</td>" +
						"<td>" +
						f.args +
						"</td>" +
						"<td>" +
						f.description +
						"</td>" +
						"<td>" +
						f.aliases +
						"</td>" +
						"</tr>";
					$(tblRow).appendTo("#userdata tbody");
				});
			});
		});
	</script>
</head>

</head>

<body>

	<div class="wrapper">
		<div class="profile">
			<table id="userdata" border="2">
				<thead>
					<th>Command Name</th>
					<th>Args</th>
					<th>Description</th>
					<th>Aliases</th>
				</thead>
				<tbody>

				</tbody>
			</table>

		</div>
	</div>

</body>
