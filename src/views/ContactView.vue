<template>
    <Content>
        <Card style="top: 17%; width: 70%; min-height: 60%">
            <Header>
                Contact Me
            </Header>
            <Description>
                <p>
                    I don't have many (public) ways of being contacted, but I do have an email at <a href="mailto:tim@takitatd.dev" target="blank" :class="$style.MailLink">tim@takitatd.dev</a>
                </p>
            </Description>
        </Card>
    </Content>    
</template>

<script>
import ContentComponent from "@/components/ContentComponent.vue";
import CardComponent from "@/components/CardComponent.vue";
import HeaderComponent from "@/components/HeaderComponent.vue";
import DescriptionComponent from '@/components/DescriptionComponent.vue'

export default {
    components: {
    Content: ContentComponent,
    Card: CardComponent,
    Header: HeaderComponent,
    Description: DescriptionComponent
}
}

</script>

<style scoped module lang="scss">
.MailLink {
    display: inline-flex;
    justify-content: center;
    align-items: center;
    margin: 0;
    padding: 0;
    text-decoration: none;
    color: #fff;
    background-image: linear-gradient(to bottom right, #bf616a, #ebcb8b);
    background-size: 0 3px;
    background-repeat: no-repeat;
    background-position-x: left;
    background-position-y: bottom;
    transition: all .4s;
}
.MailLink:hover {
    color: #c1c7d1;
    background-size: 100% 3px;
}
</style>