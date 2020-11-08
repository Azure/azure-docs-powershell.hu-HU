---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
ms.openlocfilehash: 75f6b7cee1517a3f9ae363a7e28df420e18d37ab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186939"
---
# <span data-ttu-id="fbcc2-101">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="fbcc2-101">New-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="fbcc2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fbcc2-102">SYNOPSIS</span></span>
<span data-ttu-id="fbcc2-103">Új személyazonosság-szolgáltatói konfiguráció létrehozása.</span><span class="sxs-lookup"><span data-stu-id="fbcc2-103">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="fbcc2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fbcc2-104">SYNTAX</span></span>

```
New-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>] [-SigninPolicyName <String>]
 [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>] [-SigninTenant <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbcc2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fbcc2-105">DESCRIPTION</span></span>
<span data-ttu-id="fbcc2-106">Új személyazonosság-szolgáltatói konfiguráció létrehozása.</span><span class="sxs-lookup"><span data-stu-id="fbcc2-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="fbcc2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fbcc2-107">EXAMPLES</span></span>

### <span data-ttu-id="fbcc2-108">1. példa: a Facebook identitás-szolgáltatóként való beállítása a fejlesztői portál bejelentkezéséhez</span><span class="sxs-lookup"><span data-stu-id="fbcc2-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="fbcc2-109">Ez a parancs a Facebook-identitást a ApiManagement szolgáltatás fejlesztői portálján, elfogadott identitás-szolgáltatóként állítja be.</span><span class="sxs-lookup"><span data-stu-id="fbcc2-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="fbcc2-110">Ez a funkció a Facebook App ClientId és ClientSecret adja meg.</span><span class="sxs-lookup"><span data-stu-id="fbcc2-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

### <span data-ttu-id="fbcc2-111">2. példa: a adB2C identitás-szolgáltatóként való beállítása a fejlesztői portál bejelentkezéséhez</span><span class="sxs-lookup"><span data-stu-id="fbcc2-111">Example 2: Configures adB2C as an identity Provider for Developer Portal Logins</span></span>
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

<span data-ttu-id="fbcc2-112">Ez a parancs a Facebook-identitást a ApiManagement szolgáltatás fejlesztői portálján, elfogadott identitás-szolgáltatóként állítja be.</span><span class="sxs-lookup"><span data-stu-id="fbcc2-112">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="fbcc2-113">Ez a funkció a Facebook App ClientId és ClientSecret adja meg.</span><span class="sxs-lookup"><span data-stu-id="fbcc2-113">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="fbcc2-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fbcc2-114">PARAMETERS</span></span>

### <span data-ttu-id="fbcc2-115">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="fbcc2-115">-AllowedTenants</span></span>
<span data-ttu-id="fbcc2-116">Az engedélyezett Azure Active Directory-bérlők listája</span><span class="sxs-lookup"><span data-stu-id="fbcc2-116">List of allowed Azure Active Directory Tenants</span></span>

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

### <span data-ttu-id="fbcc2-117">-Authority (jogosultság)</span><span class="sxs-lookup"><span data-stu-id="fbcc2-117">-Authority</span></span>
<span data-ttu-id="fbcc2-118">OpenID Connect Discovery Endpoint hostname for AAD vagy AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="fbcc2-118">OpenID Connect discovery endpoint hostname for AAD or AAD B2C.</span></span> <span data-ttu-id="fbcc2-119">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="fbcc2-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="fbcc2-120">-ClientId</span><span class="sxs-lookup"><span data-stu-id="fbcc2-120">-ClientId</span></span>
<span data-ttu-id="fbcc2-121">Az alkalmazás ügyfél-azonosítója a külső identitás-szolgáltatónál.</span><span class="sxs-lookup"><span data-stu-id="fbcc2-121">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="fbcc2-122">A Facebook-bejelentkezéshez használt app-azonosító, a Google login ügyfél azonosítója, a Microsofthoz tartozó app-azonosító.</span><span class="sxs-lookup"><span data-stu-id="fbcc2-122">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="fbcc2-123">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="fbcc2-123">-ClientSecret</span></span>
<span data-ttu-id="fbcc2-124">Ügyfél titka az alkalmazás külső identitás-szolgáltatónál, amely a bejelentkezési kérelem hitelesítésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="fbcc2-124">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="fbcc2-125">A Facebook-bejelentkezéshez például az App titka, a Google bejelentkezési API kulcsa, a Microsoft nyilvános kulcsa.</span><span class="sxs-lookup"><span data-stu-id="fbcc2-125">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="fbcc2-126">-Környezet</span><span class="sxs-lookup"><span data-stu-id="fbcc2-126">-Context</span></span>
<span data-ttu-id="fbcc2-127">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="fbcc2-127">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="fbcc2-128">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="fbcc2-128">This parameter is required.</span></span>

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

### <span data-ttu-id="fbcc2-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbcc2-129">-DefaultProfile</span></span>
<span data-ttu-id="fbcc2-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fbcc2-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbcc2-131">-PasswordResetPolicyName</span><span class="sxs-lookup"><span data-stu-id="fbcc2-131">-PasswordResetPolicyName</span></span>
<span data-ttu-id="fbcc2-132">A jelszó-visszaállítási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="fbcc2-132">Password Reset Policy Name.</span></span> <span data-ttu-id="fbcc2-133">Csak a AAD B2C identitás-szolgáltatóra érvényes.</span><span class="sxs-lookup"><span data-stu-id="fbcc2-133">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="fbcc2-134">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="fbcc2-134">This parameter is optional.</span></span>

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

### <span data-ttu-id="fbcc2-135">-ProfileEditingPolicyName</span><span class="sxs-lookup"><span data-stu-id="fbcc2-135">-ProfileEditingPolicyName</span></span>
<span data-ttu-id="fbcc2-136">Profil szerkesztési házirend neve.</span><span class="sxs-lookup"><span data-stu-id="fbcc2-136">Profile Editing Policy Name.</span></span> <span data-ttu-id="fbcc2-137">Csak a AAD B2C identitás-szolgáltatóra érvényes.</span><span class="sxs-lookup"><span data-stu-id="fbcc2-137">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="fbcc2-138">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="fbcc2-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="fbcc2-139">-SigninPolicyName</span><span class="sxs-lookup"><span data-stu-id="fbcc2-139">-SigninPolicyName</span></span>
<span data-ttu-id="fbcc2-140">A jel házirend neve.</span><span class="sxs-lookup"><span data-stu-id="fbcc2-140">Signin Policy Name.</span></span> <span data-ttu-id="fbcc2-141">Csak a AAD B2C identitás-szolgáltatóra érvényes.</span><span class="sxs-lookup"><span data-stu-id="fbcc2-141">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="fbcc2-142">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="fbcc2-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="fbcc2-143">-SigninTenant</span><span class="sxs-lookup"><span data-stu-id="fbcc2-143">-SigninTenant</span></span>
<span data-ttu-id="fbcc2-144">A bérlői fiók helyett a AAD B2C jel `common`</span><span class="sxs-lookup"><span data-stu-id="fbcc2-144">Signin Tenant to override in AAD B2C instead of the `common` Tenant</span></span>

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

### <span data-ttu-id="fbcc2-145">-SignupPolicyName</span><span class="sxs-lookup"><span data-stu-id="fbcc2-145">-SignupPolicyName</span></span>
<span data-ttu-id="fbcc2-146">Feliratkozási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="fbcc2-146">Signup Policy Name.</span></span> <span data-ttu-id="fbcc2-147">Csak a AAD B2C identitás-szolgáltatóra érvényes.</span><span class="sxs-lookup"><span data-stu-id="fbcc2-147">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="fbcc2-148">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="fbcc2-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="fbcc2-149">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="fbcc2-149">-Type</span></span>
<span data-ttu-id="fbcc2-150">Egy identitás-szolgáltató azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fbcc2-150">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="fbcc2-151">Ha meg van adva, az azonosító segítségével megpróbálja megtalálni az identitás-szolgáltató konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="fbcc2-151">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="fbcc2-152">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="fbcc2-152">This parameter is optional.</span></span>

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

### <span data-ttu-id="fbcc2-153">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fbcc2-153">-Confirm</span></span>
<span data-ttu-id="fbcc2-154">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fbcc2-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbcc2-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbcc2-155">-WhatIf</span></span>
<span data-ttu-id="fbcc2-156">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fbcc2-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fbcc2-157">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fbcc2-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbcc2-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbcc2-158">CommonParameters</span></span>
<span data-ttu-id="fbcc2-159">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fbcc2-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbcc2-160">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fbcc2-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbcc2-161">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fbcc2-161">INPUTS</span></span>

### <span data-ttu-id="fbcc2-162">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="fbcc2-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fbcc2-163">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="fbcc2-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="fbcc2-164">System. String</span><span class="sxs-lookup"><span data-stu-id="fbcc2-164">System.String</span></span>

### <span data-ttu-id="fbcc2-165">System. string []</span><span class="sxs-lookup"><span data-stu-id="fbcc2-165">System.String[]</span></span>

## <span data-ttu-id="fbcc2-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fbcc2-166">OUTPUTS</span></span>

### <span data-ttu-id="fbcc2-167">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="fbcc2-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="fbcc2-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fbcc2-168">NOTES</span></span>

## <span data-ttu-id="fbcc2-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fbcc2-169">RELATED LINKS</span></span>

[<span data-ttu-id="fbcc2-170">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="fbcc2-170">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="fbcc2-171">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="fbcc2-171">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="fbcc2-172">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="fbcc2-172">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)