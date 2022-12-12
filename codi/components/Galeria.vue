<template>
    <div>
        {{color}}
        <v-carousel>
        <v-carousel-item v-for="(imatge, pos) in imatgesFiltradesPerColor"  :key="imatge.imatge" >
            <v-img
            :title="imatge.text"
            :alt="imatge.text"
            :src="imatge.imatge"
            >
            </v-img>

        </v-carousel-item>

        </v-carousel>
        <!-- <pre>
            {{imatges}}
        </pre> -->
    </div>
</template>
<script>
export default{
    props:['imatges','color'],
    computed:{
        imatgesFiltradesPerColor(){
            var self = this
            if(this.imatges){
            //    filter->  es con el foreach pero no torna un object sino true/false, et dona cada un dels elements si torna true el ho incorpora als elements filtrats sino el descarta
                    return this.imatges.filter((imatge)=>{
                    console.log("this",this)
                    console.log("self",self)
                    if(imatge.color == self.color){
                        return true
                    }
                })
            }else{
                return {}
            }
            
        }
    }

}

</script>