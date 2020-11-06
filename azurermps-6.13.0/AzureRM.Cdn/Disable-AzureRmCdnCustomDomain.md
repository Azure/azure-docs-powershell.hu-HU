---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/disable-azurermcdncustomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Disable-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Disable-AzureRmCdnCustomDomain.md
ms.openlocfilehash: 1f0694d93f95f9fed6f23d7912003a179598ac91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498388"
---
# <span data-ttu-id="3246b-101">Disable-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="3246b-101">Disable-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="3246b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3246b-102">SYNOPSIS</span></span>
<span data-ttu-id="3246b-103">Letiltja az egyéni HTTPS-t.</span><span class="sxs-lookup"><span data-stu-id="3246b-103">Disables custom HTTPS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3246b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3246b-104">SYNTAX</span></span>

### <span data-ttu-id="3246b-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3246b-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzureRmCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3246b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3246b-106">ByObjectParameterSet</span></span>
```
Disable-AzureRmCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3246b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3246b-107">DESCRIPTION</span></span>
<span data-ttu-id="3246b-108">A **disable-AzureRmCdnCustomDomain** parancsmag letiltja a biztonságos HTTPS-kézbesítést egy CDN-beli egyéni tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="3246b-108">The **Disable-AzureRmCdnCustomDomain** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="3246b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3246b-109">EXAMPLES</span></span>

### <span data-ttu-id="3246b-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3246b-110">Example 1</span></span>
```powershell
Disable-AzureRmCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="3246b-111">Tiltsa le az egyéni tartomány HTTPS-kézbesítését.</span><span class="sxs-lookup"><span data-stu-id="3246b-111">Disable https delivery of the custom domain.</span></span>

## <span data-ttu-id="3246b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3246b-112">PARAMETERS</span></span>

### <span data-ttu-id="3246b-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="3246b-113">-CustomDomainName</span></span>
<span data-ttu-id="3246b-114">Azure CDN egyéni tartomány megjelenítendő neve</span><span class="sxs-lookup"><span data-stu-id="3246b-114">Azure CDN custom domain display name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3246b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3246b-115">-DefaultProfile</span></span>
<span data-ttu-id="3246b-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3246b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3246b-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="3246b-117">-EndpointName</span></span>
<span data-ttu-id="3246b-118">Azure CDN végpont neve.</span><span class="sxs-lookup"><span data-stu-id="3246b-118">Azure CDN endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3246b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3246b-119">-InputObject</span></span>
<span data-ttu-id="3246b-120">Az egyéni tartomány-objektum.</span><span class="sxs-lookup"><span data-stu-id="3246b-120">The custom domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3246b-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3246b-121">-PassThru</span></span>
<span data-ttu-id="3246b-122">Visszatérési objektum (ha meg van adva)</span><span class="sxs-lookup"><span data-stu-id="3246b-122">Return object (if specified).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3246b-123">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="3246b-123">-ProfileName</span></span>
<span data-ttu-id="3246b-124">Azure CDN-profil neve.</span><span class="sxs-lookup"><span data-stu-id="3246b-124">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3246b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3246b-125">-ResourceGroupName</span></span>
<span data-ttu-id="3246b-126">Az Azure CDN-profil erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="3246b-126">The resource group of the Azure CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3246b-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3246b-127">-Confirm</span></span>
<span data-ttu-id="3246b-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3246b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3246b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3246b-129">-WhatIf</span></span>
<span data-ttu-id="3246b-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3246b-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3246b-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3246b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3246b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3246b-132">CommonParameters</span></span>
<span data-ttu-id="3246b-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3246b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3246b-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3246b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3246b-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3246b-135">INPUTS</span></span>

### <span data-ttu-id="3246b-136">Microsoft. Azure. Command. CDN. models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="3246b-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>
<span data-ttu-id="3246b-137">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3246b-137">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="3246b-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3246b-138">OUTPUTS</span></span>

### <span data-ttu-id="3246b-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3246b-139">System.Boolean</span></span>

## <span data-ttu-id="3246b-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3246b-140">NOTES</span></span>

## <span data-ttu-id="3246b-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3246b-141">RELATED LINKS</span></span>
