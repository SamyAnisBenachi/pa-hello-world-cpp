properties([
    pipelineTriggers([pollSCM('H/3 * * * *')])
    ])

node(){
    cleanWs()
    checkoutscm
    sh"make"
    sh"./main"
}