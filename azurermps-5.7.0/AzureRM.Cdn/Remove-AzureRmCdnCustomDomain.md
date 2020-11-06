---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 5727E2CA-0A0B-4050-9F4A-7E06758D9B53
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/remove-azurermcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnCustomDomain.md
ms.openlocfilehash: 8c6e3629d4ac6e8592370393b94727234a6eb12a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493222"
---
# <span data-ttu-id="86ccb-101">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="86ccb-101">Remove-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="86ccb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="86ccb-102">SYNOPSIS</span></span>
<span data-ttu-id="86ccb-103">Eltávolít egy egyéni tartományt.</span><span class="sxs-lookup"><span data-stu-id="86ccb-103">Removes a custom domain.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86ccb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="86ccb-104">SYNTAX</span></span>

### <span data-ttu-id="86ccb-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="86ccb-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzureRmCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="86ccb-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="86ccb-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmCdnCustomDomain -CdnCustomDomain <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86ccb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="86ccb-107">DESCRIPTION</span></span>
<span data-ttu-id="86ccb-108">A **Remove-AzureRmCdnCustomDomain** parancsmag az egyéni tartományt egy Azure Content Delivery Network (CDN) végpontból távolítja el.</span><span class="sxs-lookup"><span data-stu-id="86ccb-108">The **Remove-AzureRmCdnCustomDomain** cmdlet removes the custom domain from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="86ccb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="86ccb-109">EXAMPLES</span></span>

## <span data-ttu-id="86ccb-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="86ccb-110">PARAMETERS</span></span>

### <span data-ttu-id="86ccb-111">-CdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="86ccb-111">-CdnCustomDomain</span></span>
<span data-ttu-id="86ccb-112">A parancsmag által eltávolított egyéni tartomány meghatározása.</span><span class="sxs-lookup"><span data-stu-id="86ccb-112">Specifies the custom domain that this cmdlet removes.</span></span>

```yaml
Type: PSCustomDomain
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86ccb-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="86ccb-113">-CustomDomainName</span></span>
<span data-ttu-id="86ccb-114">Annak az egyéni tartománynak az erőforrás nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="86ccb-114">Specifies the resource name of the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="86ccb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86ccb-115">-DefaultProfile</span></span>
<span data-ttu-id="86ccb-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="86ccb-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86ccb-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="86ccb-117">-EndpointName</span></span>
<span data-ttu-id="86ccb-118">Annak a végpontnak a neve, amelyből a parancsmag eltávolítja az egyéni tartományt.</span><span class="sxs-lookup"><span data-stu-id="86ccb-118">Specifies the name of the endpoint from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="86ccb-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86ccb-119">-PassThru</span></span>
<span data-ttu-id="86ccb-120">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="86ccb-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="86ccb-121">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="86ccb-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86ccb-122">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="86ccb-122">-ProfileName</span></span>
<span data-ttu-id="86ccb-123">Annak a profilnak a neve, amelyből a parancsmag eltávolítja az egyéni tartományt.</span><span class="sxs-lookup"><span data-stu-id="86ccb-123">Specifies the name of the profile from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="86ccb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86ccb-124">-ResourceGroupName</span></span>
<span data-ttu-id="86ccb-125">Annak az erőforrás-csoportnak a neve, amelyből a parancsmag eltávolítja az egyéni tartományt.</span><span class="sxs-lookup"><span data-stu-id="86ccb-125">Specifies the name of the resource group from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="86ccb-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="86ccb-126">-Confirm</span></span>
<span data-ttu-id="86ccb-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="86ccb-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86ccb-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86ccb-128">-WhatIf</span></span>
<span data-ttu-id="86ccb-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="86ccb-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86ccb-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="86ccb-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86ccb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86ccb-131">CommonParameters</span></span>
<span data-ttu-id="86ccb-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="86ccb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86ccb-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86ccb-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86ccb-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="86ccb-134">INPUTS</span></span>

### <span data-ttu-id="86ccb-135">PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="86ccb-135">PSCustomDomain</span></span>
<span data-ttu-id="86ccb-136">A ' CdnCustomDomain ' paraméter az "PSCustomDomain" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="86ccb-136">Parameter 'CdnCustomDomain' accepts value of type 'PSCustomDomain' from the pipeline</span></span>

## <span data-ttu-id="86ccb-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86ccb-137">OUTPUTS</span></span>

### <span data-ttu-id="86ccb-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="86ccb-138">System.Boolean</span></span>

## <span data-ttu-id="86ccb-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="86ccb-139">NOTES</span></span>

## <span data-ttu-id="86ccb-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86ccb-140">RELATED LINKS</span></span>

[<span data-ttu-id="86ccb-141">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="86ccb-141">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="86ccb-142">Új – AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="86ccb-142">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="86ccb-143">Teszt-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="86ccb-143">Test-AzureRmCdnCustomDomain</span></span>](./Test-AzureRmCdnCustomDomain.md)


