<template>
  <div id="pricing">
      <div class="container">
          <div class="container-head">
              <h2>Styles And Pricing</h2>
          </div>
	<table  data-aos="fade-up" data-aos-duration="1000">
		<thead>
			<tr>
				<th>Style</th>
				<th>From</th>
				<th>Style</th>
				<th>From</th>
			</tr>
		</thead>
		<tbody>
			<tr>
				<td>Agbada</td>
				<td>N18,000</td>
				<td>Pencil Skirt</td>
				<td>N4,000</td>
			</tr>
			<tr>
				<td>Senator</td>
				<td>N12,000</td>
				<td>Pants</td>
				<td>N4,000</td>
			</tr>
			<tr>
				<td>Native Top/Office Shirst</td>
				<td>N5,000</td>
				<td>Jumpsuit</td>
				<td>N8,000</td>
			</tr>
			<tr>
				<td>Up and down</td>
				<td>N12,000</td>
				<td>Skirt and blouse, Ankara</td>
				<td>N12,000</td>
			</tr>
            <tr>
				<td>Skirt and blouse, Lase</td>
				<td>N12,000</td>
				<td>Maxi dress/for Lace</td>
				<td>N12,000</td>
			</tr>
            <tr>
				<td>Mini dress/for Lace</td>
				<td>N8,000</td>
				<td>-</td>
				<td>-</td>
			</tr>
		</tbody>
	</table>
</div>
  </div>

</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.container {
	margin: 30px 30px 30px 120px;
	@media(max-width: 600px) {
		// overflow: auto;
		margin: 0px;
		 width: 100%;
		 padding: 10px;
	}
	

    &-head {
        text-align: center;
        font-size: 1.5em;
        color: #4C4556;
        margin: 40px 0px;

    }
}

table {
	width: 1300px;
	border-collapse: collapse;
	overflow: hidden;
	box-shadow: 0 0 20px rgba(0,0,0,0.1);
	@media(max-width: 600px) {
		width: 100%;
		// margin-left: 0px;
	}
}

th,
td {
	padding: 15px;
	background-color: rgba(255,255,255,0.2);
	color: #4C4556;
	@media(max-width: 600px) {
		padding: 10px;
	}
}

th {
	text-align: left;
}

thead {
	th {
		background-color: #4C4556;
        color: #ffff;
	}
}

tbody {
	tr {
		&:hover {
			background-color: rgba(255,255,255,0.3);
		}
	}
	td {
		position: relative;
		&:hover {
			&:before {
				content: "";
				position: absolute;
				left: 0;
				right: 0;
				top: -9999px;
				bottom: -9999px;
				background-color: rgba(255,255,255,0.2);
				z-index: -1;
			}
		}
	}
}
</style>