---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementIdentityProvider.md
ms.openlocfilehash: d2d689c9df73f7cd9bb6df6a5153e9afa71cb39d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667937"
---
# <span data-ttu-id="cdb17-101">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="cdb17-101">Set-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="cdb17-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cdb17-102">SYNOPSIS</span></span>
<span data-ttu-id="cdb17-103">Frissíti egy meglévő személyazonosság-szolgáltató konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="cdb17-103">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="cdb17-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cdb17-104">SYNTAX</span></span>

### <span data-ttu-id="cdb17-105">ExpandedParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cdb17-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-ClientId <String>] [-ClientSecret <String>]
 [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>] [-SigninPolicyName <String>]
 [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdb17-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="cdb17-106">ByInputObject</span></span>
```
Set-AzApiManagementIdentityProvider -InputObject <PsApiManagementIdentityProvider> [-ClientId <String>]
 [-ClientSecret <String>] [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>]
 [-SigninPolicyName <String>] [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdb17-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cdb17-107">DESCRIPTION</span></span>
<span data-ttu-id="cdb17-108">Frissíti egy meglévő személyazonosság-szolgáltató konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="cdb17-108">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="cdb17-109">Példák</span><span class="sxs-lookup"><span data-stu-id="cdb17-109">EXAMPLES</span></span>

### <span data-ttu-id="cdb17-110">Példa 1: a Facebook-identitás szolgáltatójának frissítése</span><span class="sxs-lookup"><span data-stu-id="cdb17-110">Example 1 : Update the facebook Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Set-AzApiManagementIdentityProvider -Context $apimContext -Type Facebook -ClientSecret "updatedSecret" -PassThru
```

<span data-ttu-id="cdb17-111">A parancsmag frissíti a Facebook-identitás szolgáltatójának az ügyfél titkát;</span><span class="sxs-lookup"><span data-stu-id="cdb17-111">The cmdlet updates the Client Secret of the Facebook Identity Provider;</span></span>

## <span data-ttu-id="cdb17-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cdb17-112">PARAMETERS</span></span>

### <span data-ttu-id="cdb17-113">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="cdb17-113">-AllowedTenants</span></span>
<span data-ttu-id="cdb17-114">Az engedélyezett Azure Active Directory-bérlők listája.</span><span class="sxs-lookup"><span data-stu-id="cdb17-114">List of allowed Azure Active Directory Tenants.</span></span>

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

### <span data-ttu-id="cdb17-115">-Authority (jogosultság)</span><span class="sxs-lookup"><span data-stu-id="cdb17-115">-Authority</span></span>
<span data-ttu-id="cdb17-116">OpenID Connect Discovery Endpoint hostname for AAD vagy AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="cdb17-116">OpenID Connect discovery endpoint hostname for AAD or AAD B2C.</span></span> <span data-ttu-id="cdb17-117">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="cdb17-117">This parameter is optional.</span></span>

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

### <span data-ttu-id="cdb17-118">-ClientId</span><span class="sxs-lookup"><span data-stu-id="cdb17-118">-ClientId</span></span>
<span data-ttu-id="cdb17-119">Az alkalmazás ügyfél-azonosítója a külső identitás-szolgáltatónál.</span><span class="sxs-lookup"><span data-stu-id="cdb17-119">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="cdb17-120">A Facebook-bejelentkezéshez használt app-azonosító, a Google login ügyfél azonosítója, a Microsofthoz tartozó app-azonosító.</span><span class="sxs-lookup"><span data-stu-id="cdb17-120">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="cdb17-121">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="cdb17-121">-ClientSecret</span></span>
<span data-ttu-id="cdb17-122">Ügyfél titka az alkalmazás külső identitás-szolgáltatónál, amely a bejelentkezési kérelem hitelesítésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="cdb17-122">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="cdb17-123">A Facebook-bejelentkezéshez például az App titka, a Google bejelentkezési API kulcsa, a Microsoft nyilvános kulcsa.</span><span class="sxs-lookup"><span data-stu-id="cdb17-123">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="cdb17-124">-Környezet</span><span class="sxs-lookup"><span data-stu-id="cdb17-124">-Context</span></span>
<span data-ttu-id="cdb17-125">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="cdb17-125">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="cdb17-126">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="cdb17-126">This parameter is required.</span></span>

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

### <span data-ttu-id="cdb17-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdb17-127">-DefaultProfile</span></span>
<span data-ttu-id="cdb17-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cdb17-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cdb17-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cdb17-129">-InputObject</span></span>
<span data-ttu-id="cdb17-130">A PsApiManagementIdentityProvider példánya.</span><span class="sxs-lookup"><span data-stu-id="cdb17-130">Instance of PsApiManagementIdentityProvider.</span></span> <span data-ttu-id="cdb17-131">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="cdb17-131">This parameter is required.</span></span>

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

### <span data-ttu-id="cdb17-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cdb17-132">-PassThru</span></span>
<span data-ttu-id="cdb17-133">Jelzi, hogy ez a parancsmag a parancsmag által módosított  **PsApiManagementIdentityProvider** adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="cdb17-133">Indicates that this cmdlet returns the  **PsApiManagementIdentityProvider** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="cdb17-134">-PasswordResetPolicyName</span><span class="sxs-lookup"><span data-stu-id="cdb17-134">-PasswordResetPolicyName</span></span>
<span data-ttu-id="cdb17-135">A jelszó-visszaállítási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="cdb17-135">Password Reset Policy Name.</span></span> <span data-ttu-id="cdb17-136">Csak a AAD B2C identitás-szolgáltatóra érvényes.</span><span class="sxs-lookup"><span data-stu-id="cdb17-136">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="cdb17-137">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="cdb17-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="cdb17-138">-ProfileEditingPolicyName</span><span class="sxs-lookup"><span data-stu-id="cdb17-138">-ProfileEditingPolicyName</span></span>
<span data-ttu-id="cdb17-139">Profil szerkesztési házirend neve.</span><span class="sxs-lookup"><span data-stu-id="cdb17-139">Profile Editing Policy Name.</span></span> <span data-ttu-id="cdb17-140">Csak a AAD B2C identitás-szolgáltatóra érvényes.</span><span class="sxs-lookup"><span data-stu-id="cdb17-140">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="cdb17-141">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="cdb17-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="cdb17-142">-SigninPolicyName</span><span class="sxs-lookup"><span data-stu-id="cdb17-142">-SigninPolicyName</span></span>
<span data-ttu-id="cdb17-143">A jel házirend neve.</span><span class="sxs-lookup"><span data-stu-id="cdb17-143">Signin Policy Name.</span></span> <span data-ttu-id="cdb17-144">Csak a AAD B2C identitás-szolgáltatóra érvényes.</span><span class="sxs-lookup"><span data-stu-id="cdb17-144">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="cdb17-145">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="cdb17-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="cdb17-146">-SignupPolicyName</span><span class="sxs-lookup"><span data-stu-id="cdb17-146">-SignupPolicyName</span></span>
<span data-ttu-id="cdb17-147">Feliratkozási házirend neve.</span><span class="sxs-lookup"><span data-stu-id="cdb17-147">Signup Policy Name.</span></span> <span data-ttu-id="cdb17-148">Csak a AAD B2C identitás-szolgáltatóra érvényes.</span><span class="sxs-lookup"><span data-stu-id="cdb17-148">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="cdb17-149">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="cdb17-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="cdb17-150">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="cdb17-150">-Type</span></span>
<span data-ttu-id="cdb17-151">A meglévő személyazonosság-szolgáltató azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cdb17-151">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="cdb17-152">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="cdb17-152">This parameter is required.</span></span>

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

### <span data-ttu-id="cdb17-153">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cdb17-153">-Confirm</span></span>
<span data-ttu-id="cdb17-154">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cdb17-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdb17-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdb17-155">-WhatIf</span></span>
<span data-ttu-id="cdb17-156">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cdb17-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cdb17-157">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cdb17-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdb17-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdb17-158">CommonParameters</span></span>
<span data-ttu-id="cdb17-159">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cdb17-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdb17-160">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cdb17-160">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdb17-161">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cdb17-161">INPUTS</span></span>

### <span data-ttu-id="cdb17-162">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="cdb17-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="cdb17-163">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="cdb17-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="cdb17-164">System. String</span><span class="sxs-lookup"><span data-stu-id="cdb17-164">System.String</span></span>

### <span data-ttu-id="cdb17-165">System. string []</span><span class="sxs-lookup"><span data-stu-id="cdb17-165">System.String[]</span></span>

### <span data-ttu-id="cdb17-166">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="cdb17-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cdb17-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cdb17-167">OUTPUTS</span></span>

### <span data-ttu-id="cdb17-168">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="cdb17-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="cdb17-169">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cdb17-169">NOTES</span></span>

## <span data-ttu-id="cdb17-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cdb17-170">RELATED LINKS</span></span>

[<span data-ttu-id="cdb17-171">Új – AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="cdb17-171">New-AzApiManagementIdentityProvider</span></span>](./New-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="cdb17-172">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="cdb17-172">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="cdb17-173">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="cdb17-173">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)
