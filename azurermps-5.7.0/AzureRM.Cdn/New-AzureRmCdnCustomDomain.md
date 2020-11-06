---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 7060D3D7-B397-447E-88E3-B6F0D094770D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/new-azurermcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnCustomDomain.md
ms.openlocfilehash: 2788c135f7c93d0ca2f3a8dbb17228e4118625c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493225"
---
# <span data-ttu-id="220b9-101">New-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="220b9-101">New-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="220b9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="220b9-102">SYNOPSIS</span></span>
<span data-ttu-id="220b9-103">Egyéni tartományt hoz létre a CDN-végponthoz.</span><span class="sxs-lookup"><span data-stu-id="220b9-103">Creates a custom domain for a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="220b9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="220b9-104">SYNTAX</span></span>

### <span data-ttu-id="220b9-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="220b9-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzureRmCdnCustomDomain -HostName <String> -CustomDomainName <String> -EndpointName <String>
 -ProfileName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="220b9-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="220b9-106">ByObjectParameterSet</span></span>
```
New-AzureRmCdnCustomDomain -HostName <String> -CustomDomainName <String> -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="220b9-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="220b9-107">DESCRIPTION</span></span>
<span data-ttu-id="220b9-108">A **New-AzureRmCdnCustomDomain** parancsmag létrehoz egy egyéni tartományt az Azure Content Delivery Network (CDN) végponthoz.</span><span class="sxs-lookup"><span data-stu-id="220b9-108">The **New-AzureRmCdnCustomDomain** cmdlet creates a custom domain for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="220b9-109">Példák</span><span class="sxs-lookup"><span data-stu-id="220b9-109">EXAMPLES</span></span>

## <span data-ttu-id="220b9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="220b9-110">PARAMETERS</span></span>

### <span data-ttu-id="220b9-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="220b9-111">-CdnEndpoint</span></span>
<span data-ttu-id="220b9-112">Annak a CDN-végpont-objektumnak a megadása, amelyhez az egyéni tartomány hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="220b9-112">Specifies the CDN endpoint object to which the custom domain is added.</span></span>

```yaml
Type: PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="220b9-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="220b9-113">-CustomDomainName</span></span>
<span data-ttu-id="220b9-114">Az egyéni tartomány erőforrásának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="220b9-114">Specifies the resource name of the custom domain.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="220b9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="220b9-115">-DefaultProfile</span></span>
<span data-ttu-id="220b9-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="220b9-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="220b9-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="220b9-117">-EndpointName</span></span>
<span data-ttu-id="220b9-118">A végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="220b9-118">Specifies the name of the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="220b9-119">-HostName (állomásnév)</span><span class="sxs-lookup"><span data-stu-id="220b9-119">-HostName</span></span>
<span data-ttu-id="220b9-120">Az egyéni tartomány állomásnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="220b9-120">Specifies the host name of the custom domain.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="220b9-121">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="220b9-121">-ProfileName</span></span>
<span data-ttu-id="220b9-122">A profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="220b9-122">Specifies the name of the profile.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="220b9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="220b9-123">-ResourceGroupName</span></span>
<span data-ttu-id="220b9-124">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez az egyéni tartomány tartozik.</span><span class="sxs-lookup"><span data-stu-id="220b9-124">Specifies the name of the resource group to which the custom domain belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="220b9-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="220b9-125">-Confirm</span></span>
<span data-ttu-id="220b9-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="220b9-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="220b9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="220b9-127">-WhatIf</span></span>
<span data-ttu-id="220b9-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="220b9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="220b9-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="220b9-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="220b9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="220b9-130">CommonParameters</span></span>
<span data-ttu-id="220b9-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="220b9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="220b9-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="220b9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="220b9-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="220b9-133">INPUTS</span></span>

### <span data-ttu-id="220b9-134">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="220b9-134">PSEndpoint</span></span>
<span data-ttu-id="220b9-135">A ' CdnEndpoint ' paraméter az "PSEndpoint" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="220b9-135">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="220b9-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="220b9-136">OUTPUTS</span></span>

### <span data-ttu-id="220b9-137">Microsoft. Azure. Command. CDN. models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="220b9-137">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="220b9-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="220b9-138">NOTES</span></span>

## <span data-ttu-id="220b9-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="220b9-139">RELATED LINKS</span></span>

[<span data-ttu-id="220b9-140">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="220b9-140">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="220b9-141">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="220b9-141">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="220b9-142">Teszt-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="220b9-142">Test-AzureRmCdnCustomDomain</span></span>](./Test-AzureRmCdnCustomDomain.md)


