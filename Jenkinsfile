 pipeline {
    agent { label 'NODE1' }
     
    parameters {  
                 choice(name: 'maven_goal', choices: ['install','package','clean install'], description: 'build the code')
                 choice(name: 'branch_to_build', choices: ['main', 'dev', 'ppm'], description: 'choose build')
                }
    stages {
        stage ('vcs') {
            steps {
             sh'ls && pwd'
             sh" cd src && dotnet restore NopCommerce.sln"
             sh"cd ${WORKSPACE}/src/Presentation/Nop.Web && dotnet build Nop.Web.csproj -c Release"
             sh"cd ${WORKSPACE}/src/Plugins/Nop.Plugin.DiscountRules.CustomerRoles && dotnet build Nop.Plugin.DiscountRules.CustomerRoles.csproj -c Release"
             sh"cd ${WORKSPACE}/src/Plugins/Nop.Plugin.ExchangeRate.EcbExchange && dotnet build Nop.Plugin.ExchangeRate.EcbExchange.csproj -c Release"
             sh'cd ${WORKSPACE}/src/Plugins/Nop.Plugin.ExternalAuth.Facebook && dotnet build Nop.Plugin.ExternalAuth.Facebook.csproj -c Release'
             sh'cd ${WORKSPACE}/src/Plugins/Nop.Plugin.Misc.Sendinblue && dotnet build Nop.Plugin.Misc.Sendinblue.csproj -c Release'
             sh'cd ${WORKSPACE}/src/Plugins/Nop.Plugin.Misc.WebApi.Frontend && dotnet build Nop.Plugin.Misc.WebApi.Frontend.csproj -c Release'
             sh'cd ${WORKSPACE}/src/Plugins/Nop.Plugin.Misc.Zettle && dotnet build Nop.Plugin.Misc.Zettle.csproj -c Release'
             sh'cd ${WORKSPACE}/src/Plugins/Nop.Plugin.MultiFactorAuth.GoogleAuthenticator && dotnet build Nop.Plugin.MultiFactorAuth.GoogleAuthenticator.csproj -c Release'
             sh'cd ${WORKSPACE}/src/Plugins/Nop.Plugin.Payments.CheckMoneyOrder && dotnet build Nop.Plugin.Payments.CheckMoneyOrder.csproj -c Release'
             sh'cd ${WORKSPACE}/src/Plugins/Nop.Plugin.Payments.CyberSource && dotnet build Nop.Plugin.Payments.CyberSource.csproj -c Release'
             sh'cd ${WORKSPACE}/src/Plugins/Nop.Plugin.Payments.Manual && dotnet build Nop.Plugin.Payments.Manual.csproj -c Release'
             sh'cd ${WORKSPACE}/src/Plugins/Nop.Plugin.Payments.PayPalCommerce && dotnet build Nop.Plugin.Payments.PayPalCommerce.csproj -c Release'
             sh'cd ${WORKSPACE}/src/Plugins/Nop.Plugin.Pickup.PickupInStore && dotnet build Nop.Plugin.Pickup.PickupInStore.csproj -c Release'
             sh'cd ${WORKSPACE}/src/Plugins/Nop.Plugin.Shipping.FixedByWeightByTotal && dotnet build Nop.Plugin.Shipping.FixedByWeightByTotal.csproj -c Release'
             sh'cd ${WORKSPACE}/src/Plugins/Nop.Plugin.Shipping.UPS && dotnet build Nop.Plugin.Shipping.UPS.csproj -c Release'
             sh'cd ${WORKSPACE}/src/Plugins/Nop.Plugin.Tax.Avalara && dotnet build Nop.Plugin.Tax.Avalara.csproj -c Release'
             sh'cd ${WORKSPACE}/src/Plugins/Nop.Plugin.Tax.FixedOrByCountryStateZip && dotnet build Nop.Plugin.Tax.FixedOrByCountryStateZip.csproj -c Release '
             sh'cd ${WORKSPACE}/src/Plugins/Nop.Plugin.Widgets.AccessiBe && dotnet build Nop.Plugin.Widgets.AccessiBe.csproj -c Release'
             sh'cd ${WORKSPACE}/src/Plugins/Nop.Plugin.Widgets.FacebookPixel && dotnet build Nop.Plugin.Widgets.FacebookPixel.csproj -c Release'
             sh'cd ${WORKSPACE}/src/Plugins/Nop.Plugin.Widgets.GoogleAnalytics && dotnet build Nop.Plugin.Widgets.GoogleAnalytics.csproj -c Release'
             sh'cd ${WORKSPACE}/src/Plugins/Nop.Plugin.Widgets.NivoSlider && dotnet build Nop.Plugin.Widgets.NivoSlider.csproj -c Release'
             sh'cd ${WORKSPACE}/src/Plugins/Nop.Plugin.Widgets.What3words && dotnet build Nop.Plugin.Widgets.What3words.csproj -c Release'
             // publishing project
             sh'cd ${WORKSPACE}/src/Presentation/Nop.Web && dotnet publish Nop.Web.csproj -c Release -o /app/published'
             sh'''
             cd ${WORKSPACE}/app/published && mkdir logs && mkdir bin 

             '''
             //66 lines completed

            }
        }
    

    }
 }
