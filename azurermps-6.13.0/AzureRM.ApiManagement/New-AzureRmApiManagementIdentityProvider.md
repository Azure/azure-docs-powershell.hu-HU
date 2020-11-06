---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: d0883edb698000ae0aaff957899a03e9936e4d93
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498536"
---
# <span data-ttu-id="f057c-101">New-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="f057c-101">New-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="f057c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f057c-102">SYNOPSIS</span></span>
<span data-ttu-id="f057c-103">Új személyazonosság-szolgáltatói konfiguráció létrehozása.</span><span class="sxs-lookup"><span data-stu-id="f057c-103">Creates a new Identity Provider configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f057c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f057c-104">SYNTAX</span></span>

```
New-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f057c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f057c-105">DESCRIPTION</span></span>
<span data-ttu-id="f057c-106">Új személyazonosság-szolgáltatói konfiguráció létrehozása.</span><span class="sxs-lookup"><span data-stu-id="f057c-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="f057c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f057c-107">EXAMPLES</span></span>

### <span data-ttu-id="f057c-108">1. példa: a Facebook identitás-szolgáltatóként való beállítása a fejlesztői portál bejelentkezéséhez</span><span class="sxs-lookup"><span data-stu-id="f057c-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="f057c-109">Ez a parancs a Facebook-identitást a ApiManagement szolgáltatás fejlesztői portálján, elfogadott identitás-szolgáltatóként állítja be.</span><span class="sxs-lookup"><span data-stu-id="f057c-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="f057c-110">Ez a funkció a Facebook App ClientId és ClientSecret adja meg.</span><span class="sxs-lookup"><span data-stu-id="f057c-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="f057c-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f057c-111">PARAMETERS</span></span>

### <span data-ttu-id="f057c-112">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="f057c-112">-AllowedTenants</span></span>
<span data-ttu-id="f057c-113">Az engedélyezett Azure Active Directory-bérlők listája</span><span class="sxs-lookup"><span data-stu-id="f057c-113">List of allowed Azure Active Directory Tenants</span></span>

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

### <span data-ttu-id="f057c-114">-ClientId</span><span class="sxs-lookup"><span data-stu-id="f057c-114">-ClientId</span></span>
<span data-ttu-id="f057c-115">Az alkalmazás ügyfél-azonosítója a külső identitás-szolgáltatónál.</span><span class="sxs-lookup"><span data-stu-id="f057c-115">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="f057c-116">A Facebook-bejelentkezéshez használt app-azonosító, a Google login ügyfél azonosítója, a Microsofthoz tartozó app-azonosító.</span><span class="sxs-lookup"><span data-stu-id="f057c-116">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="f057c-117">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="f057c-117">-ClientSecret</span></span>
<span data-ttu-id="f057c-118">Ügyfél titka az alkalmazás külső identitás-szolgáltatónál, amely a bejelentkezési kérelem hitelesítésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="f057c-118">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="f057c-119">A Facebook-bejelentkezéshez például az App titka, a Google bejelentkezési API kulcsa, a Microsoft nyilvános kulcsa.</span><span class="sxs-lookup"><span data-stu-id="f057c-119">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="f057c-120">-Környezet</span><span class="sxs-lookup"><span data-stu-id="f057c-120">-Context</span></span>
<span data-ttu-id="f057c-121">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="f057c-121">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="f057c-122">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="f057c-122">This parameter is required.</span></span>

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

### <span data-ttu-id="f057c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f057c-123">-DefaultProfile</span></span>
<span data-ttu-id="f057c-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f057c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f057c-125">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="f057c-125">-Type</span></span>
<span data-ttu-id="f057c-126">Egy identitás-szolgáltató azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f057c-126">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="f057c-127">Ha meg van adva, az azonosító segítségével megpróbálja megtalálni az identitás-szolgáltató konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="f057c-127">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="f057c-128">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="f057c-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="f057c-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f057c-129">-Confirm</span></span>
<span data-ttu-id="f057c-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f057c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f057c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f057c-131">-WhatIf</span></span>
<span data-ttu-id="f057c-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f057c-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f057c-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f057c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f057c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f057c-134">CommonParameters</span></span>
<span data-ttu-id="f057c-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f057c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f057c-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f057c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f057c-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f057c-137">INPUTS</span></span>

### <span data-ttu-id="f057c-138">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f057c-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f057c-139">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="f057c-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="f057c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f057c-140">System.String</span></span>

### <span data-ttu-id="f057c-141">System. string []</span><span class="sxs-lookup"><span data-stu-id="f057c-141">System.String[]</span></span>

## <span data-ttu-id="f057c-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f057c-142">OUTPUTS</span></span>

### <span data-ttu-id="f057c-143">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="f057c-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="f057c-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f057c-144">NOTES</span></span>

## <span data-ttu-id="f057c-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f057c-145">RELATED LINKS</span></span>

[<span data-ttu-id="f057c-146">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="f057c-146">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="f057c-147">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="f057c-147">Remove-AzureRmApiManagementIdentityProvider</span></span>](./Remove-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="f057c-148">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="f057c-148">Set-AzureRmApiManagementIdentityProvider</span></span>](./Set-AzureRmApiManagementIdentityProvider.md)
