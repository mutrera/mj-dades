<template>
    <!-- <div>
        Heroo
    </div> -->
    <v-img v-if="heroInfo" 
    height="100vk" 
    :src="heroInfo.imatge"
    gradient="to top right, rgba(0,0,0,.33), rgba(0,0,0,0.7)"
 >
        <v-container fill-height style="height:100%">
            <v-row style="height:100%" align="center">
                <v-col cols="12" md="4" offset-md="3" align="center">
                    <h3>{{heroInfo.subtitol}}</h3>
                    <h1>{{heroInfo.titol}}</h1>
                    <p>{{heroInfo.text}}</p>

                    <v-btn target="_blank"
                    :href="heroInfo.botoUrl">
                    {{heroInfo.botoText}}
                    </v-btn>
            
                </v-col>
            </v-row>
        </v-container>




    </v-img>
</template>
<script>
    export default{
        //manera de pasar bola d'informació a una pàgina -> props
        props:["heroInfo"]

    }
</script>