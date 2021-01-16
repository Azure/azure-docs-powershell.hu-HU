---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
ms.openlocfilehash: 75f6b7cee1517a3f9ae363a7e28df420e18d37ab
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382534"
---
# <span data-ttu-id="b1308-101">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="b1308-101">New-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="b1308-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1308-102">SYNOPSIS</span></span>
<span data-ttu-id="b1308-103">Új identitásszolgáltató-konfigurációt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b1308-103">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="b1308-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b1308-104">SYNTAX</span></span>

```
New-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>] [-SigninPolicyName <String>]
 [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>] [-SigninTenant <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1308-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b1308-105">DESCRIPTION</span></span>
<span data-ttu-id="b1308-106">Új identitásszolgáltató-konfigurációt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b1308-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="b1308-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b1308-107">EXAMPLES</span></span>

### <span data-ttu-id="b1308-108">1. példa: A Facebook konfigurálása identitásszolgáltatóként a fejlesztői portálon való bejelentkezéshez</span><span class="sxs-lookup"><span data-stu-id="b1308-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="b1308-109">Ez a parancs a Facebook-identitást elfogadott identitásszolgáltatóként konfigurálja az ApiManagement szolgáltatás fejlesztői portálján.</span><span class="sxs-lookup"><span data-stu-id="b1308-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="b1308-110">Ez a Facebook app ClientId és ClientSecret adatbeviteleként történik.</span><span class="sxs-lookup"><span data-stu-id="b1308-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

### <span data-ttu-id="b1308-111">2. példa: Konfigurálja az adB2C-t identitásszolgáltatóként a fejlesztői portálon való bejelentkezéshez</span><span class="sxs-lookup"><span data-stu-id="b1308-111">Example 2: Configures adB2C as an identity Provider for Developer Portal Logins</span></span>
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

<span data-ttu-id="b1308-112">Ez a parancs a Facebook-identitást elfogadott identitásszolgáltatóként konfigurálja az ApiManagement szolgáltatás fejlesztői portálján.</span><span class="sxs-lookup"><span data-stu-id="b1308-112">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="b1308-113">Ez a Facebook app ClientId és ClientSecret adatbeviteleként történik.</span><span class="sxs-lookup"><span data-stu-id="b1308-113">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="b1308-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1308-114">PARAMETERS</span></span>

### <span data-ttu-id="b1308-115">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="b1308-115">-AllowedTenants</span></span>
<span data-ttu-id="b1308-116">Engedélyezett Azure Active Directory-bérlők listája</span><span class="sxs-lookup"><span data-stu-id="b1308-116">List of allowed Azure Active Directory Tenants</span></span>

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

### <span data-ttu-id="b1308-117">-Authority</span><span class="sxs-lookup"><span data-stu-id="b1308-117">-Authority</span></span>
<span data-ttu-id="b1308-118">Az OpenID Connect felderítési végpontjának állomásneve az AAD-hez vagy az AAD B2C-hez.</span><span class="sxs-lookup"><span data-stu-id="b1308-118">OpenID Connect discovery endpoint hostname for AAD or AAD B2C.</span></span> <span data-ttu-id="b1308-119">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="b1308-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="b1308-120">-ClientId</span><span class="sxs-lookup"><span data-stu-id="b1308-120">-ClientId</span></span>
<span data-ttu-id="b1308-121">A külső identitásszolgáltatóban az alkalmazás ügyfélazonosítója.</span><span class="sxs-lookup"><span data-stu-id="b1308-121">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="b1308-122">Ez a Facebook-bejelentkezés appazonosítója, a Google-bejelentkezés ügyfélazonosítója, a Microsoft appazonosítója.</span><span class="sxs-lookup"><span data-stu-id="b1308-122">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="b1308-123">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="b1308-123">-ClientSecret</span></span>
<span data-ttu-id="b1308-124">A bejelentkezési kérelem hitelesítéséhez használt, külső identitásszolgáltatóban használt alkalmazás ügyféltitkja.</span><span class="sxs-lookup"><span data-stu-id="b1308-124">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="b1308-125">Ez például a Facebook-bejelentkezés appkulcsa, a Google-bejelentkezés API-kulcsa, a Microsoft nyilvános kulcsa.</span><span class="sxs-lookup"><span data-stu-id="b1308-125">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="b1308-126">-Környezet</span><span class="sxs-lookup"><span data-stu-id="b1308-126">-Context</span></span>
<span data-ttu-id="b1308-127">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="b1308-127">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b1308-128">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="b1308-128">This parameter is required.</span></span>

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

### <span data-ttu-id="b1308-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1308-129">-DefaultProfile</span></span>
<span data-ttu-id="b1308-130">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b1308-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1308-131">-PasswordResetPolicyName</span><span class="sxs-lookup"><span data-stu-id="b1308-131">-PasswordResetPolicyName</span></span>
<span data-ttu-id="b1308-132">Jelszó-visszaállítási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="b1308-132">Password Reset Policy Name.</span></span> <span data-ttu-id="b1308-133">Csak az AAD B2C identitásszolgáltatóra vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="b1308-133">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="b1308-134">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="b1308-134">This parameter is optional.</span></span>

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

### <span data-ttu-id="b1308-135">-ProfileEditingPolicyName</span><span class="sxs-lookup"><span data-stu-id="b1308-135">-ProfileEditingPolicyName</span></span>
<span data-ttu-id="b1308-136">Profilszerkesztési házirend neve.</span><span class="sxs-lookup"><span data-stu-id="b1308-136">Profile Editing Policy Name.</span></span> <span data-ttu-id="b1308-137">Csak az AAD B2C identitásszolgáltatóra vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="b1308-137">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="b1308-138">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="b1308-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="b1308-139">-SigninPolicyName</span><span class="sxs-lookup"><span data-stu-id="b1308-139">-SigninPolicyName</span></span>
<span data-ttu-id="b1308-140">Bejelentkezési házirend neve.</span><span class="sxs-lookup"><span data-stu-id="b1308-140">Signin Policy Name.</span></span> <span data-ttu-id="b1308-141">Csak az AAD B2C identitásszolgáltatóra vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="b1308-141">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="b1308-142">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="b1308-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="b1308-143">-SigninTenant</span><span class="sxs-lookup"><span data-stu-id="b1308-143">-SigninTenant</span></span>
<span data-ttu-id="b1308-144">Signin Tenant to override in AAD B2C instead of the `common` Tenant</span><span class="sxs-lookup"><span data-stu-id="b1308-144">Signin Tenant to override in AAD B2C instead of the `common` Tenant</span></span>

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

### <span data-ttu-id="b1308-145">-SignupPolicyName</span><span class="sxs-lookup"><span data-stu-id="b1308-145">-SignupPolicyName</span></span>
<span data-ttu-id="b1308-146">A bejelentkezési házirend neve.</span><span class="sxs-lookup"><span data-stu-id="b1308-146">Signup Policy Name.</span></span> <span data-ttu-id="b1308-147">Csak az AAD B2C identitásszolgáltatóra vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="b1308-147">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="b1308-148">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="b1308-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="b1308-149">-Type</span><span class="sxs-lookup"><span data-stu-id="b1308-149">-Type</span></span>
<span data-ttu-id="b1308-150">Identitásszolgáltató azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b1308-150">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="b1308-151">Ha meg van adva, a rendszer megpróbálja megtalálni az identitásszolgáltató konfigurációját az azonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="b1308-151">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="b1308-152">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="b1308-152">This parameter is optional.</span></span>

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

### <span data-ttu-id="b1308-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1308-153">-Confirm</span></span>
<span data-ttu-id="b1308-154">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b1308-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1308-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1308-155">-WhatIf</span></span>
<span data-ttu-id="b1308-156">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b1308-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b1308-157">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b1308-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1308-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1308-158">CommonParameters</span></span>
<span data-ttu-id="b1308-159">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1308-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1308-160">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b1308-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1308-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b1308-161">INPUTS</span></span>

### <span data-ttu-id="b1308-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b1308-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b1308-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="b1308-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="b1308-164">System.String</span><span class="sxs-lookup"><span data-stu-id="b1308-164">System.String</span></span>

### <span data-ttu-id="b1308-165">System.String[]</span><span class="sxs-lookup"><span data-stu-id="b1308-165">System.String[]</span></span>

## <span data-ttu-id="b1308-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1308-166">OUTPUTS</span></span>

### <span data-ttu-id="b1308-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="b1308-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="b1308-168">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b1308-168">NOTES</span></span>

## <span data-ttu-id="b1308-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b1308-169">RELATED LINKS</span></span>

[<span data-ttu-id="b1308-170">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="b1308-170">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="b1308-171">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="b1308-171">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="b1308-172">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="b1308-172">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)
