---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 5727E2CA-0A0B-4050-9F4A-7E06758D9B53
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnCustomDomain.md
ms.openlocfilehash: 0645b3f5286526ba72db35fd8b9e048c895f4108
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186254"
---
# <span data-ttu-id="c1edf-101">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="c1edf-101">Remove-AzCdnCustomDomain</span></span>

## <span data-ttu-id="c1edf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c1edf-102">SYNOPSIS</span></span>
<span data-ttu-id="c1edf-103">Eltávolít egy egyéni tartományt.</span><span class="sxs-lookup"><span data-stu-id="c1edf-103">Removes a custom domain.</span></span>

## <span data-ttu-id="c1edf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c1edf-104">SYNTAX</span></span>

### <span data-ttu-id="c1edf-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c1edf-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c1edf-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1edf-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnCustomDomain -CdnCustomDomain <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1edf-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c1edf-107">DESCRIPTION</span></span>
<span data-ttu-id="c1edf-108">A **Remove-AzCdnCustomDomain** parancsmag az egyéni tartományt egy Azure Content Delivery Network (CDN) végpontból távolítja el.</span><span class="sxs-lookup"><span data-stu-id="c1edf-108">The **Remove-AzCdnCustomDomain** cmdlet removes the custom domain from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="c1edf-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c1edf-109">EXAMPLES</span></span>

## <span data-ttu-id="c1edf-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c1edf-110">PARAMETERS</span></span>

### <span data-ttu-id="c1edf-111">-CdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="c1edf-111">-CdnCustomDomain</span></span>
<span data-ttu-id="c1edf-112">A parancsmag által eltávolított egyéni tartomány meghatározása.</span><span class="sxs-lookup"><span data-stu-id="c1edf-112">Specifies the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c1edf-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="c1edf-113">-CustomDomainName</span></span>
<span data-ttu-id="c1edf-114">Annak az egyéni tartománynak az erőforrás nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="c1edf-114">Specifies the resource name of the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c1edf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1edf-115">-DefaultProfile</span></span>
<span data-ttu-id="c1edf-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c1edf-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c1edf-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="c1edf-117">-EndpointName</span></span>
<span data-ttu-id="c1edf-118">Annak a végpontnak a neve, amelyből a parancsmag eltávolítja az egyéni tartományt.</span><span class="sxs-lookup"><span data-stu-id="c1edf-118">Specifies the name of the endpoint from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="c1edf-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c1edf-119">-PassThru</span></span>
<span data-ttu-id="c1edf-120">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="c1edf-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c1edf-121">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="c1edf-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c1edf-122">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="c1edf-122">-ProfileName</span></span>
<span data-ttu-id="c1edf-123">Annak a profilnak a neve, amelyből a parancsmag eltávolítja az egyéni tartományt.</span><span class="sxs-lookup"><span data-stu-id="c1edf-123">Specifies the name of the profile from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="c1edf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1edf-124">-ResourceGroupName</span></span>
<span data-ttu-id="c1edf-125">Annak az erőforrás-csoportnak a neve, amelyből a parancsmag eltávolítja az egyéni tartományt.</span><span class="sxs-lookup"><span data-stu-id="c1edf-125">Specifies the name of the resource group from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="c1edf-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c1edf-126">-Confirm</span></span>
<span data-ttu-id="c1edf-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c1edf-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1edf-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1edf-128">-WhatIf</span></span>
<span data-ttu-id="c1edf-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c1edf-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1edf-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c1edf-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1edf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1edf-131">CommonParameters</span></span>
<span data-ttu-id="c1edf-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c1edf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1edf-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c1edf-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1edf-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1edf-134">INPUTS</span></span>

### <span data-ttu-id="c1edf-135">Microsoft. Azure. Command. CDN. models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="c1edf-135">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="c1edf-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c1edf-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c1edf-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1edf-137">OUTPUTS</span></span>

### <span data-ttu-id="c1edf-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c1edf-138">System.Boolean</span></span>

## <span data-ttu-id="c1edf-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c1edf-139">NOTES</span></span>

## <span data-ttu-id="c1edf-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c1edf-140">RELATED LINKS</span></span>

[<span data-ttu-id="c1edf-141">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="c1edf-141">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="c1edf-142">Új – AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="c1edf-142">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="c1edf-143">Teszt-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="c1edf-143">Test-AzCdnCustomDomain</span></span>](./Test-AzCdnCustomDomain.md)


