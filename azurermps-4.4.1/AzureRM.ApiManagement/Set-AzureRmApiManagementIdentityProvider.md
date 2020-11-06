---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: 76ee402fee2e18d426875340d4eaadda2cc63042
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499284"
---
# <span data-ttu-id="ad642-101">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="ad642-101">Set-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="ad642-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ad642-102">SYNOPSIS</span></span>
<span data-ttu-id="ad642-103">Frissíti egy meglévő személyazonosság-szolgáltató konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="ad642-103">Updates the Configuration of an existing Identity Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad642-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ad642-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-ClientId <String>] [-ClientSecret <String>]
 [-AllowedTenants <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ad642-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ad642-105">DESCRIPTION</span></span>
<span data-ttu-id="ad642-106">Frissíti egy meglévő személyazonosság-szolgáltató konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="ad642-106">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="ad642-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ad642-107">EXAMPLES</span></span>

### <span data-ttu-id="ad642-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ad642-108">Example 1</span></span>
```
PS C:\> Set-AzureRmApiManagementIdentityProvider -Context $apimcontext -Type Facebook -ClientSecret "updatedSecret" -PassThru
```

<span data-ttu-id="ad642-109">A parancsmag frissíti a Facebook-identitás szolgáltatójának az ügyfél titkát;</span><span class="sxs-lookup"><span data-stu-id="ad642-109">The cmdlet updates the Client Secret of the Facebook Identity Provider;</span></span>

## <span data-ttu-id="ad642-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ad642-110">PARAMETERS</span></span>

### <span data-ttu-id="ad642-111">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="ad642-111">-AllowedTenants</span></span>
<span data-ttu-id="ad642-112">Az engedélyezett Azure Active Directory-bérlők listája.</span><span class="sxs-lookup"><span data-stu-id="ad642-112">List of allowed Azure Active Directory Tenants.</span></span>

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

### <span data-ttu-id="ad642-113">-ClientId</span><span class="sxs-lookup"><span data-stu-id="ad642-113">-ClientId</span></span>
<span data-ttu-id="ad642-114">Az alkalmazás ügyfél-azonosítója a külső identitás-szolgáltatónál.</span><span class="sxs-lookup"><span data-stu-id="ad642-114">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="ad642-115">A Facebook-bejelentkezéshez használt app-azonosító, a Google login ügyfél azonosítója, a Microsofthoz tartozó app-azonosító.</span><span class="sxs-lookup"><span data-stu-id="ad642-115">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="ad642-116">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="ad642-116">-ClientSecret</span></span>
<span data-ttu-id="ad642-117">Ügyfél titka az alkalmazás külső identitás-szolgáltatónál, amely a bejelentkezési kérelem hitelesítésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="ad642-117">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="ad642-118">A Facebook-bejelentkezéshez például az App titka, a Google bejelentkezési API kulcsa, a Microsoft nyilvános kulcsa.</span><span class="sxs-lookup"><span data-stu-id="ad642-118">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="ad642-119">-Környezet</span><span class="sxs-lookup"><span data-stu-id="ad642-119">-Context</span></span>
<span data-ttu-id="ad642-120">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="ad642-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ad642-121">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="ad642-121">This parameter is required.</span></span>

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

### <span data-ttu-id="ad642-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad642-122">-PassThru</span></span>
<span data-ttu-id="ad642-123">Jelzi, hogy ez a parancsmag a parancsmag által módosított  **PsApiManagementIdentityProvider** adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="ad642-123">Indicates that this cmdlet returns the  **PsApiManagementIdentityProvider** that this cmdlet modifies.</span></span>


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

### <span data-ttu-id="ad642-124">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="ad642-124">-Type</span></span>
<span data-ttu-id="ad642-125">A meglévő személyazonosság-szolgáltató azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ad642-125">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="ad642-126">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="ad642-126">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad642-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ad642-127">-Confirm</span></span>
<span data-ttu-id="ad642-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ad642-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad642-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad642-129">-WhatIf</span></span>
<span data-ttu-id="ad642-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ad642-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ad642-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ad642-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad642-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad642-132">-DefaultProfile</span></span>
<span data-ttu-id="ad642-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ad642-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad642-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad642-134">CommonParameters</span></span>
<span data-ttu-id="ad642-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ad642-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad642-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad642-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad642-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad642-137">INPUTS</span></span>

## <span data-ttu-id="ad642-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad642-138">OUTPUTS</span></span>

### <span data-ttu-id="ad642-139">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="ad642-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="ad642-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ad642-140">NOTES</span></span>

## <span data-ttu-id="ad642-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ad642-141">RELATED LINKS</span></span>

[<span data-ttu-id="ad642-142">Új – AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="ad642-142">New-AzureRmApiManagementIdentityProvider</span></span>](./New-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="ad642-143">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="ad642-143">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="ad642-144">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="ad642-144">Remove-AzureRmApiManagementIdentityProvider</span></span>](./Remove-AzureRmApiManagementIdentityProvider.md)
