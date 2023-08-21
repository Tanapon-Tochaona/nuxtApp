<template>
    <div >
        <div id="app">
<img :src="picture" :width="sizewid" :height="sizehei">

</div>
<p>ชื่อ : {{ firstname }}</p>
<p>นามสกุล : {{ lastname }}</p>
<p>ชื่อเล่น : {{ nickname }}</p>
<p>อายุ : {{ age }}</p>
<p>ที่อยู่ : <span v-html="address"></span></p>
<p v-if="hobby.length ===0">ไม่มีงานอดิเรก</p>
<div v-else>
<p>งานอดิเรก : </p>
<ul>
   <li v-for="item in hobby">{{ item }}</li>
</ul>
</div>

<p>ข้อมูลพื้นฐาน : </p>
<ul>
    <li v-for="(value,key) in general" :key="key">{{ key }} : {{ value }}</li>
</ul>
<button @click="showData">คลิกเพื่อดูข้อมูล</button>
 </div>
</template>
<script>
export default{
    data(){
        return{
            firstname:"Tanapon",
            lastname:"Tochaona",
            age:18,
            address: "<i>Chonburi</i>",
            picture:"https://rms.tatc.ac.th/files/importpicstd/01/66309010012.jpg",
            sizewid: 177,
            sizehei: 236,
            hobby:["นอน","เล่นตะกร้อ",'เล่นเกม'],
            general:{gender:"ชาย",weight:65,hight:169,status:false},
            nickname:''
        }
    },
    methods: {
    getFullname(){
        return `$(this.firstname) $(this.lastname)`
    },
    showData(){
        alert (this.firstname)
    },
    increment(value){
        this.age += value
    },
    decrement(value){
        this.age -= value
    },
    setNickName(event){
        this.nickname = event.target.value
    },
    submitForm(e){
        e.preventDefault();
        alert('บันทึกข้อมูลเรียบร้อย')
    }

}
}

</script>
