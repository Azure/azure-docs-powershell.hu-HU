---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementIdentityProvider.md
ms.openlocfilehash: f8bc49e4a5b4e8e7fb6285327cf4432cd0561506
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836911"
---
# <span data-ttu-id="302b3-101">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="302b3-101">Set-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="302b3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="302b3-102">SYNOPSIS</span></span>
<span data-ttu-id="302b3-103">Frissíti egy meglévő személyazonosság-szolgáltató konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="302b3-103">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="302b3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="302b3-104">SYNTAX</span></span>

```
Set-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-ClientId <String>] [-ClientSecret <String>]
 [-AllowedTenants <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="302b3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="302b3-105">DESCRIPTION</span></span>
<span data-ttu-id="302b3-106">Frissíti egy meglévő személyazonosság-szolgáltató konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="302b3-106">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="302b3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="302b3-107">EXAMPLES</span></span>

### <span data-ttu-id="302b3-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="302b3-108">Example 1</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Set-AzApiManagementIdentityProvider -Context $apimContext -Type Facebook -ClientSecret "updatedSecret" -PassThru
```

<span data-ttu-id="302b3-109">A parancsmag frissíti a Facebook-identitás szolgáltatójának az ügyfél titkát;</span><span class="sxs-lookup"><span data-stu-id="302b3-109">The cmdlet updates the Client Secret of the Facebook Identity Provider;</span></span>

## <span data-ttu-id="302b3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="302b3-110">PARAMETERS</span></span>

### <span data-ttu-id="302b3-111">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="302b3-111">-AllowedTenants</span></span>
<span data-ttu-id="302b3-112">Az engedélyezett Azure Active Directory-bérlők listája.</span><span class="sxs-lookup"><span data-stu-id="302b3-112">List of allowed Azure Active Directory Tenants.</span></span>

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

### <span data-ttu-id="302b3-113">-ClientId</span><span class="sxs-lookup"><span data-stu-id="302b3-113">-ClientId</span></span>
<span data-ttu-id="302b3-114">Az alkalmazás ügyfél-azonosítója a külső identitás-szolgáltatónál.</span><span class="sxs-lookup"><span data-stu-id="302b3-114">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="302b3-115">A Facebook-bejelentkezéshez használt app-azonosító, a Google login ügyfél azonosítója, a Microsofthoz tartozó app-azonosító.</span><span class="sxs-lookup"><span data-stu-id="302b3-115">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="302b3-116">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="302b3-116">-ClientSecret</span></span>
<span data-ttu-id="302b3-117">Ügyfél titka az alkalmazás külső identitás-szolgáltatónál, amely a bejelentkezési kérelem hitelesítésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="302b3-117">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="302b3-118">A Facebook-bejelentkezéshez például az App titka, a Google bejelentkezési API kulcsa, a Microsoft nyilvános kulcsa.</span><span class="sxs-lookup"><span data-stu-id="302b3-118">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="302b3-119">-Környezet</span><span class="sxs-lookup"><span data-stu-id="302b3-119">-Context</span></span>
<span data-ttu-id="302b3-120">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="302b3-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="302b3-121">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="302b3-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="302b3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="302b3-122">-DefaultProfile</span></span>
<span data-ttu-id="302b3-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="302b3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="302b3-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="302b3-124">-PassThru</span></span>
<span data-ttu-id="302b3-125">Jelzi, hogy ez a parancsmag a parancsmag által módosított  **PsApiManagementIdentityProvider** adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="302b3-125">Indicates that this cmdlet returns the  **PsApiManagementIdentityProvider** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="302b3-126">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="302b3-126">-Type</span></span>
<span data-ttu-id="302b3-127">A meglévő személyazonosság-szolgáltató azonosítója.</span><span class="sxs-lookup"><span data-stu-id="302b3-127">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="302b3-128">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="302b3-128">This parameter is required.</span></span>

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

### <span data-ttu-id="302b3-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="302b3-129">-Confirm</span></span>
<span data-ttu-id="302b3-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="302b3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="302b3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="302b3-131">-WhatIf</span></span>
<span data-ttu-id="302b3-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="302b3-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="302b3-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="302b3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="302b3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="302b3-134">CommonParameters</span></span>
<span data-ttu-id="302b3-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="302b3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="302b3-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="302b3-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="302b3-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="302b3-137">INPUTS</span></span>

### <span data-ttu-id="302b3-138">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="302b3-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="302b3-139">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="302b3-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="302b3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="302b3-140">System.String</span></span>

### <span data-ttu-id="302b3-141">System. string []</span><span class="sxs-lookup"><span data-stu-id="302b3-141">System.String[]</span></span>

### <span data-ttu-id="302b3-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="302b3-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="302b3-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="302b3-143">OUTPUTS</span></span>

### <span data-ttu-id="302b3-144">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="302b3-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="302b3-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="302b3-145">NOTES</span></span>

## <span data-ttu-id="302b3-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="302b3-146">RELATED LINKS</span></span>

[<span data-ttu-id="302b3-147">Új – AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="302b3-147">New-AzApiManagementIdentityProvider</span></span>](./New-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="302b3-148">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="302b3-148">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="302b3-149">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="302b3-149">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)
