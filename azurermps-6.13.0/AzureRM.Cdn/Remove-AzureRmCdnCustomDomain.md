---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 5727E2CA-0A0B-4050-9F4A-7E06758D9B53
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/remove-azurermcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnCustomDomain.md
ms.openlocfilehash: fa0e3682d62f01d7d305d190c6765aab709bed15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498375"
---
# <span data-ttu-id="82148-101">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="82148-101">Remove-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="82148-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="82148-102">SYNOPSIS</span></span>
<span data-ttu-id="82148-103">Eltávolít egy egyéni tartományt.</span><span class="sxs-lookup"><span data-stu-id="82148-103">Removes a custom domain.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82148-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="82148-104">SYNTAX</span></span>

### <span data-ttu-id="82148-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="82148-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzureRmCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="82148-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="82148-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmCdnCustomDomain -CdnCustomDomain <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82148-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="82148-107">DESCRIPTION</span></span>
<span data-ttu-id="82148-108">A **Remove-AzureRmCdnCustomDomain** parancsmag az egyéni tartományt egy Azure Content Delivery Network (CDN) végpontból távolítja el.</span><span class="sxs-lookup"><span data-stu-id="82148-108">The **Remove-AzureRmCdnCustomDomain** cmdlet removes the custom domain from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="82148-109">Példák</span><span class="sxs-lookup"><span data-stu-id="82148-109">EXAMPLES</span></span>

## <span data-ttu-id="82148-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="82148-110">PARAMETERS</span></span>

### <span data-ttu-id="82148-111">-CdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="82148-111">-CdnCustomDomain</span></span>
<span data-ttu-id="82148-112">A parancsmag által eltávolított egyéni tartomány meghatározása.</span><span class="sxs-lookup"><span data-stu-id="82148-112">Specifies the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="82148-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="82148-113">-CustomDomainName</span></span>
<span data-ttu-id="82148-114">Annak az egyéni tartománynak az erőforrás nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="82148-114">Specifies the resource name of the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="82148-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82148-115">-DefaultProfile</span></span>
<span data-ttu-id="82148-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="82148-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82148-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="82148-117">-EndpointName</span></span>
<span data-ttu-id="82148-118">Annak a végpontnak a neve, amelyből a parancsmag eltávolítja az egyéni tartományt.</span><span class="sxs-lookup"><span data-stu-id="82148-118">Specifies the name of the endpoint from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="82148-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="82148-119">-PassThru</span></span>
<span data-ttu-id="82148-120">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="82148-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="82148-121">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="82148-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="82148-122">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="82148-122">-ProfileName</span></span>
<span data-ttu-id="82148-123">Annak a profilnak a neve, amelyből a parancsmag eltávolítja az egyéni tartományt.</span><span class="sxs-lookup"><span data-stu-id="82148-123">Specifies the name of the profile from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="82148-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82148-124">-ResourceGroupName</span></span>
<span data-ttu-id="82148-125">Annak az erőforrás-csoportnak a neve, amelyből a parancsmag eltávolítja az egyéni tartományt.</span><span class="sxs-lookup"><span data-stu-id="82148-125">Specifies the name of the resource group from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="82148-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="82148-126">-Confirm</span></span>
<span data-ttu-id="82148-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="82148-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82148-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82148-128">-WhatIf</span></span>
<span data-ttu-id="82148-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="82148-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82148-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="82148-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82148-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82148-131">CommonParameters</span></span>
<span data-ttu-id="82148-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="82148-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82148-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82148-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82148-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="82148-134">INPUTS</span></span>

### <span data-ttu-id="82148-135">Microsoft. Azure. Command. CDN. models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="82148-135">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>
<span data-ttu-id="82148-136">Paraméterek: CdnCustomDomain (ByValue)</span><span class="sxs-lookup"><span data-stu-id="82148-136">Parameters: CdnCustomDomain (ByValue)</span></span>

### <span data-ttu-id="82148-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="82148-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="82148-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="82148-138">OUTPUTS</span></span>

### <span data-ttu-id="82148-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="82148-139">System.Boolean</span></span>

## <span data-ttu-id="82148-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="82148-140">NOTES</span></span>

## <span data-ttu-id="82148-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="82148-141">RELATED LINKS</span></span>

[<span data-ttu-id="82148-142">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="82148-142">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="82148-143">Új – AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="82148-143">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="82148-144">Teszt-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="82148-144">Test-AzureRmCdnCustomDomain</span></span>](./Test-AzureRmCdnCustomDomain.md)


