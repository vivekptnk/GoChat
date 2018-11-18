<template>
    <div class="container chat">
        <h2 class="text-primary text-center"></h2>
        <h5 class="text-secondary text-center">Powered by Vue.js & Firebase</h5>
    </div>
    <div class="card">
        <div class="card-body">
            <p class="text secondary nomessages" v-if="messages.length == 0">
                [No messages yet!]
            </p>
            <div class="messages">
                <div v-for="message in messages" :key="message.id">
                    <span class=text-info>[{{message.name}}]: </span>
                    <span>{{message.message}}</span>
                    <span class="text-secondary time">{{message.timestamo}}</span>
                </div>
            </div>
            <div class="card-action">
                <CreateMessage :name="name"/>
            </div>
        </div>
    </div>
    
</template>
