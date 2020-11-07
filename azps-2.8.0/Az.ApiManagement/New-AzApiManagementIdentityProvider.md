---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
ms.openlocfilehash: fc033eb1989838d8ed8e20d568f92ef20f8275e8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668041"
---
# <span data-ttu-id="7511c-101">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="7511c-101">New-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="7511c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7511c-102">SYNOPSIS</span></span>
<span data-ttu-id="7511c-103">Új személyazonosság-szolgáltatói konfiguráció létrehozása.</span><span class="sxs-lookup"><span data-stu-id="7511c-103">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="7511c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7511c-104">SYNTAX</span></span>

```
New-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>] [-SigninPolicyName <String>]
 [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7511c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7511c-105">DESCRIPTION</span></span>
<span data-ttu-id="7511c-106">Új személyazonosság-szolgáltatói konfiguráció létrehozása.</span><span class="sxs-lookup"><span data-stu-id="7511c-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="7511c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7511c-107">EXAMPLES</span></span>

### <span data-ttu-id="7511c-108">1. példa: a Facebook identitás-szolgáltatóként való beállítása a fejlesztői portál bejelentkezéséhez</span><span class="sxs-lookup"><span data-stu-id="7511c-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="7511c-109">Ez a parancs a Facebook-identitást a ApiManagement szolgáltatás fejlesztői portálján, elfogadott identitás-szolgáltatóként állítja be.</span><span class="sxs-lookup"><span data-stu-id="7511c-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="7511c-110">Ez a funkció a Facebook App ClientId és ClientSecret adja meg.</span><span class="sxs-lookup"><span data-stu-id="7511c-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

### <span data-ttu-id="7511c-111">2. példa: a adB2C identitás-szolgáltatóként való beállítása a fejlesztői portál bejelentkezéséhez</span><span class="sxs-lookup"><span data-stu-id="7511c-111">Example 2: Configures adB2C as an identity Provider for Developer Portal Logins</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementIdentityProvider -Context $context -Type AadB2C -ClientId 6b1fc750-9e68-450c-97d2-ba6acd0fbc20 -ClientSecret "foobar" -AllowedTenants 'samirtestbc.onmicrosoft.com' -SignupPolicyName B2C_1_signup-policy

Type                     : AadB2C
ClientId                 : 6b1fc750-9e68-450c-97d2-ba6acd0fbc20
ClientSecret             : foobar
AllowedTenants           : {samirtestbc.onmicrosoft.com}
Authority                : login.microsoftonline.com
SignupPolicyName         : B2C_1_signup-policy
SigninPolicyName         :
ProfileEditingPolicyName :
PasswordResetPolicyName  :
Id                       : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/identityProviders/AadB2C
ResourceGroupName        : Api-Default-WestUS
ServiceName              : contoso
```

<span data-ttu-id="7511c-112">Ez a parancs a Facebook-identitást a ApiManagement szolgáltatás fejlesztői portálján, elfogadott identitás-szolgáltatóként állítja be.</span><span class="sxs-lookup"><span data-stu-id="7511c-112">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="7511c-113">Ez a funkció a Facebook App ClientId és ClientSecret adja meg.</span><span class="sxs-lookup"><span data-stu-id="7511c-113">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="7511c-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7511c-114">PARAMETERS</span></span>

### <span data-ttu-id="7511c-115">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="7511c-115">-AllowedTenants</span></span>
<span data-ttu-id="7511c-116">Az engedélyezett Azure Active Directory-bérlők listája</span><span class="sxs-lookup"><span data-stu-id="7511c-116">List of allowed Azure Active Directory Tenants</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7511c-117">-Authority (jogosultság)</span><span class="sxs-lookup"><span data-stu-id="7511c-117">-Authority</span></span>
<span data-ttu-id="7511c-118">OpenID Connect Discovery Endpoint hostname for AAD vagy AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="7511c-118">OpenID Connect discovery endpoint hostname for AAD or AAD B2C.</span></span> <span data-ttu-id="7511c-119">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="7511c-119">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7511c-120">-ClientId</span><span class="sxs-lookup"><span data-stu-id="7511c-120">-ClientId</span></span>
<span data-ttu-id="7511c-121">Az alkalmazás ügyfél-azonosítója a külső identitás-szolgáltatónál.</span><span class="sxs-lookup"><span data-stu-id="7511c-121">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="7511c-122">A Facebook-bejelentkezéshez használt app-azonosító, a Google login ügyfél azonosítója, a Microsofthoz tartozó app-azonosító.</span><span class="sxs-lookup"><span data-stu-id="7511c-122">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7511c-123">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="7511c-123">-ClientSecret</span></span>
<span data-ttu-id="7511c-124">Ügyfél titka az alkalmazás külső identitás-szolgáltatónál, amely a bejelentkezési kérelem hitelesítésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="7511c-124">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="7511c-125">A Facebook-bejelentkezéshez például az App titka, a Google bejelentkezési API kulcsa, a Microsoft nyilvános kulcsa.</span><span class="sxs-lookup"><span data-stu-id="7511c-125">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7511c-126">-Környezet</span><span class="sxs-lookup"><span data-stu-id="7511c-126">-Context</span></span>
<span data-ttu-id="7511c-127">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="7511c-127">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="7511c-128">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="7511c-128">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7511c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7511c-129">-DefaultProfile</span></span>
<span data-ttu-id="7511c-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7511c-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7511c-131">-PasswordResetPolicyName</span><span class="sxs-lookup"><span data-stu-id="7511c-131">-PasswordResetPolicyName</span></span>
<span data-ttu-id="7511c-132">A jelszó-visszaállítási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="7511c-132">Password Reset Policy Name.</span></span> <span data-ttu-id="7511c-133">Csak a AAD B2C identitás-szolgáltatóra érvényes.</span><span class="sxs-lookup"><span data-stu-id="7511c-133">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="7511c-134">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="7511c-134">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7511c-135">-ProfileEditingPolicyName</span><span class="sxs-lookup"><span data-stu-id="7511c-135">-ProfileEditingPolicyName</span></span>
<span data-ttu-id="7511c-136">Profil szerkesztési házirend neve.</span><span class="sxs-lookup"><span data-stu-id="7511c-136">Profile Editing Policy Name.</span></span> <span data-ttu-id="7511c-137">Csak a AAD B2C identitás-szolgáltatóra érvényes.</span><span class="sxs-lookup"><span data-stu-id="7511c-137">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="7511c-138">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="7511c-138">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7511c-139">-SigninPolicyName</span><span class="sxs-lookup"><span data-stu-id="7511c-139">-SigninPolicyName</span></span>
<span data-ttu-id="7511c-140">A jel házirend neve.</span><span class="sxs-lookup"><span data-stu-id="7511c-140">Signin Policy Name.</span></span> <span data-ttu-id="7511c-141">Csak a AAD B2C identitás-szolgáltatóra érvényes.</span><span class="sxs-lookup"><span data-stu-id="7511c-141">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="7511c-142">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="7511c-142">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7511c-143">-SignupPolicyName</span><span class="sxs-lookup"><span data-stu-id="7511c-143">-SignupPolicyName</span></span>
<span data-ttu-id="7511c-144">Feliratkozási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="7511c-144">Signup Policy Name.</span></span> <span data-ttu-id="7511c-145">Csak a AAD B2C identitás-szolgáltatóra érvényes.</span><span class="sxs-lookup"><span data-stu-id="7511c-145">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="7511c-146">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="7511c-146">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7511c-147">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="7511c-147">-Type</span></span>
<span data-ttu-id="7511c-148">Egy identitás-szolgáltató azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7511c-148">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="7511c-149">Ha meg van adva, az azonosító segítségével megpróbálja megtalálni az identitás-szolgáltató konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="7511c-149">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="7511c-150">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="7511c-150">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7511c-151">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7511c-151">-Confirm</span></span>
<span data-ttu-id="7511c-152">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7511c-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7511c-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7511c-153">-WhatIf</span></span>
<span data-ttu-id="7511c-154">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7511c-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7511c-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7511c-155">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7511c-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7511c-156">CommonParameters</span></span>
<span data-ttu-id="7511c-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7511c-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7511c-158">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7511c-158">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7511c-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7511c-159">INPUTS</span></span>

### <span data-ttu-id="7511c-160">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7511c-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7511c-161">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="7511c-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="7511c-162">System. String</span><span class="sxs-lookup"><span data-stu-id="7511c-162">System.String</span></span>

### <span data-ttu-id="7511c-163">System. string []</span><span class="sxs-lookup"><span data-stu-id="7511c-163">System.String[]</span></span>

## <span data-ttu-id="7511c-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7511c-164">OUTPUTS</span></span>

### <span data-ttu-id="7511c-165">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="7511c-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="7511c-166">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7511c-166">NOTES</span></span>

## <span data-ttu-id="7511c-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7511c-167">RELATED LINKS</span></span>

[<span data-ttu-id="7511c-168">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="7511c-168">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="7511c-169">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="7511c-169">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="7511c-170">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="7511c-170">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)
