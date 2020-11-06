---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 5727E2CA-0A0B-4050-9F4A-7E06758D9B53
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnCustomDomain.md
ms.openlocfilehash: 2aa6b3932424f7a8375cca2584a7fc7916124c54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500903"
---
# <span data-ttu-id="5232d-101">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="5232d-101">Remove-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="5232d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5232d-102">SYNOPSIS</span></span>
<span data-ttu-id="5232d-103">Eltávolít egy egyéni tartományt.</span><span class="sxs-lookup"><span data-stu-id="5232d-103">Removes a custom domain.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5232d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5232d-104">SYNTAX</span></span>

### <span data-ttu-id="5232d-105">Paraméterérték a mezők paramétereinek beállításához (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5232d-105">Parameter Set for fields parameters (Default)</span></span>
```
Remove-AzureRmCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5232d-106">Az objektum paramétereinek beállítása paraméter</span><span class="sxs-lookup"><span data-stu-id="5232d-106">Parameter Set for object parameters</span></span>
```
Remove-AzureRmCdnCustomDomain -CdnCustomDomain <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5232d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5232d-107">DESCRIPTION</span></span>
<span data-ttu-id="5232d-108">A **Remove-AzureRmCdnCustomDomain** parancsmag az egyéni tartományt egy Azure Content Delivery Network (CDN) végpontból távolítja el.</span><span class="sxs-lookup"><span data-stu-id="5232d-108">The **Remove-AzureRmCdnCustomDomain** cmdlet removes the custom domain from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="5232d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5232d-109">EXAMPLES</span></span>

## <span data-ttu-id="5232d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5232d-110">PARAMETERS</span></span>

### <span data-ttu-id="5232d-111">-CdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="5232d-111">-CdnCustomDomain</span></span>
<span data-ttu-id="5232d-112">A parancsmag által eltávolított egyéni tartomány meghatározása.</span><span class="sxs-lookup"><span data-stu-id="5232d-112">Specifies the custom domain that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5232d-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="5232d-113">-CustomDomainName</span></span>
<span data-ttu-id="5232d-114">Annak az egyéni tartománynak az erőforrás nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="5232d-114">Specifies the resource name of the custom domain that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5232d-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="5232d-115">-EndpointName</span></span>
<span data-ttu-id="5232d-116">Annak a végpontnak a neve, amelyből a parancsmag eltávolítja az egyéni tartományt.</span><span class="sxs-lookup"><span data-stu-id="5232d-116">Specifies the name of the endpoint from which this cmdlet removes a custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5232d-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5232d-117">-PassThru</span></span>
<span data-ttu-id="5232d-118">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="5232d-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5232d-119">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="5232d-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5232d-120">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="5232d-120">-ProfileName</span></span>
<span data-ttu-id="5232d-121">Annak a profilnak a neve, amelyből a parancsmag eltávolítja az egyéni tartományt.</span><span class="sxs-lookup"><span data-stu-id="5232d-121">Specifies the name of the profile from which this cmdlet removes a custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5232d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5232d-122">-ResourceGroupName</span></span>
<span data-ttu-id="5232d-123">Annak az erőforrás-csoportnak a neve, amelyből a parancsmag eltávolítja az egyéni tartományt.</span><span class="sxs-lookup"><span data-stu-id="5232d-123">Specifies the name of the resource group from which this cmdlet removes a custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5232d-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5232d-124">-Confirm</span></span>
<span data-ttu-id="5232d-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5232d-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5232d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5232d-126">-WhatIf</span></span>
<span data-ttu-id="5232d-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5232d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5232d-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5232d-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5232d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5232d-129">-DefaultProfile</span></span>
<span data-ttu-id="5232d-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5232d-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5232d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5232d-131">CommonParameters</span></span>
<span data-ttu-id="5232d-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5232d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5232d-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5232d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5232d-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5232d-134">INPUTS</span></span>

### <span data-ttu-id="5232d-135">PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="5232d-135">PSCustomDomain</span></span>
<span data-ttu-id="5232d-136">A ' CdnCustomDomain ' paraméter az "PSCustomDomain" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="5232d-136">Parameter 'CdnCustomDomain' accepts value of type 'PSCustomDomain' from the pipeline</span></span>

## <span data-ttu-id="5232d-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5232d-137">OUTPUTS</span></span>

### <span data-ttu-id="5232d-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5232d-138">System.Boolean</span></span>

## <span data-ttu-id="5232d-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5232d-139">NOTES</span></span>

## <span data-ttu-id="5232d-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5232d-140">RELATED LINKS</span></span>

[<span data-ttu-id="5232d-141">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="5232d-141">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="5232d-142">Új – AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="5232d-142">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="5232d-143">Teszt-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="5232d-143">Test-AzureRmCdnCustomDomain</span></span>](./Test-AzureRmCdnCustomDomain.md)


