<!-- v-model 디렉티브르ㅡㄹ 사요애 상태와 폼 입력 칸에 양방향 바인딩 가능 -->
<template>
	<div>
		<h2>텍스트 입력</h2>
		<input v-model="text" /> {{ text }}

		<h2>checked</h2>
		<input type="checkbox" id="checkbox" v-model="checked" />
		<label type="checkbox">체크됨: {{ checked }} </label>

		<h2>멀티 체크</h2>
		<input
			type="checkbox"
			id="chulsoo"
			value="chulsoo"
			v-model="checkedNames"
		/>
		<label for="chulsoo">chulsoo</label>
		<input type="checkbox" id="yuri" value="yuri" v-model="checkedNames" />
		<label for="yuri">yuri</label>
		<input
			type="checkbox"
			id="maenggu"
			value="maenggu"
			v-model="checkedNames"
		/>
		<label for="maenggu">maenggu</label>
		<p>체크된이름:</p>
		<pre>{{ checkedNames }}</pre>

		<h2>라디오</h2>
		<input type="radio" id="seoul" value="seoul" v-model="picked" />
		<label for="seoul">seoul</label>
		<input type="radio" id="busan" value="busan" v-model="picked" />
		<label for="busan">busan</label>
		<input type="radio" id="inchun" value="inchun" v-model="picked" />
		<label for="inchun">inchun</label>
		<span>고른것: {{ picked }}</span>

		<h2>선택</h2>
		<select v-model="selected">
			<option disabled value="">하나를 선택하세요</option>
			<option>가</option>
			<option>나</option>
			<option>다</option>
		</select>
		<span>선택함: {{ selected }}</span>

		<h2>복수 선택</h2>
		<select v-model="multiSelected" multiple style="width: 100px">
			<option>무궁화</option>
			<option>진달래</option>
			<option>개나리</option>
		</select>
		<span>선택함: {{ multiSelected }}</span>
	</div>
</template>
<script>
export default {
	components: {},
	data() {
		return {
			text: '수정',
			checked: true,
			checkedNames: ['chulsoo'],
			picked: 'seoul',
			selected: '하나를 선택하세요',
			multiSelected: ['무궁화'],
		};
	},
	setup() {},
	created() {},
	mounted() {},
	unmounted() {},
	methods: {},
};
</script>
