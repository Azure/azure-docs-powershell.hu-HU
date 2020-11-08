---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementIdentityProvider.md
ms.openlocfilehash: a110e950bff46bba7d3c7b5033c01b95ac2397f1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013855"
---
# <span data-ttu-id="2a86b-101">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="2a86b-101">Set-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="2a86b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2a86b-102">SYNOPSIS</span></span>
<span data-ttu-id="2a86b-103">Frissíti egy meglévő személyazonosság-szolgáltató konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="2a86b-103">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="2a86b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2a86b-104">SYNTAX</span></span>

### <span data-ttu-id="2a86b-105">ExpandedParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2a86b-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-ClientId <String>] [-ClientSecret <String>]
 [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>] [-SigninPolicyName <String>]
 [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>] [-SignInTenant <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a86b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2a86b-106">ByInputObject</span></span>
```
Set-AzApiManagementIdentityProvider -InputObject <PsApiManagementIdentityProvider> [-ClientId <String>]
 [-ClientSecret <String>] [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>]
 [-SigninPolicyName <String>] [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>]
 [-SignInTenant <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a86b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2a86b-107">DESCRIPTION</span></span>
<span data-ttu-id="2a86b-108">Frissíti egy meglévő személyazonosság-szolgáltató konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="2a86b-108">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="2a86b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2a86b-109">EXAMPLES</span></span>

### <span data-ttu-id="2a86b-110">Példa 1: a Facebook-identitás szolgáltatójának frissítése</span><span class="sxs-lookup"><span data-stu-id="2a86b-110">Example 1 : Update the facebook Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Set-AzApiManagementIdentityProvider -Context $apimContext -Type Facebook -ClientSecret "updatedSecret" -PassThru
```

<span data-ttu-id="2a86b-111">A parancsmag frissíti a Facebook-identitás szolgáltatójának az ügyfél titkát;</span><span class="sxs-lookup"><span data-stu-id="2a86b-111">The cmdlet updates the Client Secret of the Facebook Identity Provider;</span></span>

## <span data-ttu-id="2a86b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2a86b-112">PARAMETERS</span></span>

### <span data-ttu-id="2a86b-113">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="2a86b-113">-AllowedTenants</span></span>
<span data-ttu-id="2a86b-114">Az engedélyezett Azure Active Directory-bérlők listája.</span><span class="sxs-lookup"><span data-stu-id="2a86b-114">List of allowed Azure Active Directory Tenants.</span></span>

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

### <span data-ttu-id="2a86b-115">-Authority (jogosultság)</span><span class="sxs-lookup"><span data-stu-id="2a86b-115">-Authority</span></span>
<span data-ttu-id="2a86b-116">OpenID Connect Discovery Endpoint hostname for AAD vagy AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="2a86b-116">OpenID Connect discovery endpoint hostname for AAD or AAD B2C.</span></span> <span data-ttu-id="2a86b-117">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="2a86b-117">This parameter is optional.</span></span>

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

### <span data-ttu-id="2a86b-118">-ClientId</span><span class="sxs-lookup"><span data-stu-id="2a86b-118">-ClientId</span></span>
<span data-ttu-id="2a86b-119">Az alkalmazás ügyfél-azonosítója a külső identitás-szolgáltatónál.</span><span class="sxs-lookup"><span data-stu-id="2a86b-119">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="2a86b-120">A Facebook-bejelentkezéshez használt app-azonosító, a Google login ügyfél azonosítója, a Microsofthoz tartozó app-azonosító.</span><span class="sxs-lookup"><span data-stu-id="2a86b-120">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="2a86b-121">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="2a86b-121">-ClientSecret</span></span>
<span data-ttu-id="2a86b-122">Ügyfél titka az alkalmazás külső identitás-szolgáltatónál, amely a bejelentkezési kérelem hitelesítésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="2a86b-122">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="2a86b-123">A Facebook-bejelentkezéshez például az App titka, a Google bejelentkezési API kulcsa, a Microsoft nyilvános kulcsa.</span><span class="sxs-lookup"><span data-stu-id="2a86b-123">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="2a86b-124">-Környezet</span><span class="sxs-lookup"><span data-stu-id="2a86b-124">-Context</span></span>
<span data-ttu-id="2a86b-125">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="2a86b-125">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2a86b-126">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="2a86b-126">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a86b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a86b-127">-DefaultProfile</span></span>
<span data-ttu-id="2a86b-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2a86b-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a86b-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a86b-129">-InputObject</span></span>
<span data-ttu-id="2a86b-130">A PsApiManagementIdentityProvider példánya.</span><span class="sxs-lookup"><span data-stu-id="2a86b-130">Instance of PsApiManagementIdentityProvider.</span></span> <span data-ttu-id="2a86b-131">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="2a86b-131">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a86b-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a86b-132">-PassThru</span></span>
<span data-ttu-id="2a86b-133">Jelzi, hogy ez a parancsmag a parancsmag által módosított  **PsApiManagementIdentityProvider** adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="2a86b-133">Indicates that this cmdlet returns the  **PsApiManagementIdentityProvider** that this cmdlet modifies.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a86b-134">-PasswordResetPolicyName</span><span class="sxs-lookup"><span data-stu-id="2a86b-134">-PasswordResetPolicyName</span></span>
<span data-ttu-id="2a86b-135">A jelszó-visszaállítási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="2a86b-135">Password Reset Policy Name.</span></span> <span data-ttu-id="2a86b-136">Csak a AAD B2C identitás-szolgáltatóra érvényes.</span><span class="sxs-lookup"><span data-stu-id="2a86b-136">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="2a86b-137">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="2a86b-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="2a86b-138">-ProfileEditingPolicyName</span><span class="sxs-lookup"><span data-stu-id="2a86b-138">-ProfileEditingPolicyName</span></span>
<span data-ttu-id="2a86b-139">Profil szerkesztési házirend neve.</span><span class="sxs-lookup"><span data-stu-id="2a86b-139">Profile Editing Policy Name.</span></span> <span data-ttu-id="2a86b-140">Csak a AAD B2C identitás-szolgáltatóra érvényes.</span><span class="sxs-lookup"><span data-stu-id="2a86b-140">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="2a86b-141">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="2a86b-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="2a86b-142">-SigninPolicyName</span><span class="sxs-lookup"><span data-stu-id="2a86b-142">-SigninPolicyName</span></span>
<span data-ttu-id="2a86b-143">A jel házirend neve.</span><span class="sxs-lookup"><span data-stu-id="2a86b-143">Signin Policy Name.</span></span> <span data-ttu-id="2a86b-144">Csak a AAD B2C identitás-szolgáltatóra érvényes.</span><span class="sxs-lookup"><span data-stu-id="2a86b-144">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="2a86b-145">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="2a86b-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="2a86b-146">-SignupPolicyName</span><span class="sxs-lookup"><span data-stu-id="2a86b-146">-SignupPolicyName</span></span>
<span data-ttu-id="2a86b-147">Feliratkozási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="2a86b-147">Signup Policy Name.</span></span> <span data-ttu-id="2a86b-148">Csak a AAD B2C identitás-szolgáltatóra érvényes.</span><span class="sxs-lookup"><span data-stu-id="2a86b-148">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="2a86b-149">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="2a86b-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="2a86b-150">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="2a86b-150">-Type</span></span>
<span data-ttu-id="2a86b-151">A meglévő személyazonosság-szolgáltató azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2a86b-151">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="2a86b-152">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="2a86b-152">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: ExpandedParameter
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a86b-153">-SigninTenant</span><span class="sxs-lookup"><span data-stu-id="2a86b-153">-SigninTenant</span></span>
<span data-ttu-id="2a86b-154">A bérlői fiók helyett a AAD B2C jel `common`</span><span class="sxs-lookup"><span data-stu-id="2a86b-154">Signin Tenant to override in AAD B2C instead of the `common` Tenant</span></span>

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

### <span data-ttu-id="2a86b-155">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2a86b-155">-Confirm</span></span>
<span data-ttu-id="2a86b-156">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2a86b-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a86b-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a86b-157">-WhatIf</span></span>
<span data-ttu-id="2a86b-158">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2a86b-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2a86b-159">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2a86b-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a86b-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a86b-160">CommonParameters</span></span>
<span data-ttu-id="2a86b-161">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2a86b-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a86b-162">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2a86b-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a86b-163">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a86b-163">INPUTS</span></span>

### <span data-ttu-id="2a86b-164">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2a86b-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2a86b-165">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="2a86b-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="2a86b-166">System. String</span><span class="sxs-lookup"><span data-stu-id="2a86b-166">System.String</span></span>

### <span data-ttu-id="2a86b-167">System. string []</span><span class="sxs-lookup"><span data-stu-id="2a86b-167">System.String[]</span></span>

### <span data-ttu-id="2a86b-168">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2a86b-168">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2a86b-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a86b-169">OUTPUTS</span></span>

### <span data-ttu-id="2a86b-170">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="2a86b-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="2a86b-171">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2a86b-171">NOTES</span></span>

## <span data-ttu-id="2a86b-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2a86b-172">RELATED LINKS</span></span>

[<span data-ttu-id="2a86b-173">Új – AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="2a86b-173">New-AzApiManagementIdentityProvider</span></span>](./New-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="2a86b-174">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="2a86b-174">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="2a86b-175">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="2a86b-175">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)
