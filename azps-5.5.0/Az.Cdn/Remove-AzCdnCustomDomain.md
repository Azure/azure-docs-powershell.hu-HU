---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 5727E2CA-0A0B-4050-9F4A-7E06758D9B53
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnCustomDomain.md
ms.openlocfilehash: 0645b3f5286526ba72db35fd8b9e048c895f4108
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167995"
---
# <span data-ttu-id="58141-101">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="58141-101">Remove-AzCdnCustomDomain</span></span>

## <span data-ttu-id="58141-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58141-102">SYNOPSIS</span></span>
<span data-ttu-id="58141-103">Eltávolít egy egyéni tartományt.</span><span class="sxs-lookup"><span data-stu-id="58141-103">Removes a custom domain.</span></span>

## <span data-ttu-id="58141-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="58141-104">SYNTAX</span></span>

### <span data-ttu-id="58141-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="58141-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="58141-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="58141-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnCustomDomain -CdnCustomDomain <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58141-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="58141-107">DESCRIPTION</span></span>
<span data-ttu-id="58141-108">A **Remove-AzCdnCustomDomain** parancsmag eltávolítja az egyéni tartományt egy Azure Content Delivery Network (CDN) végpontból.</span><span class="sxs-lookup"><span data-stu-id="58141-108">The **Remove-AzCdnCustomDomain** cmdlet removes the custom domain from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="58141-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="58141-109">EXAMPLES</span></span>

## <span data-ttu-id="58141-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58141-110">PARAMETERS</span></span>

### <span data-ttu-id="58141-111">-CdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="58141-111">-CdnCustomDomain</span></span>
<span data-ttu-id="58141-112">Azt az egyéni tartományt adja meg, amelyről a parancsmag eltávolít.</span><span class="sxs-lookup"><span data-stu-id="58141-112">Specifies the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="58141-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="58141-113">-CustomDomainName</span></span>
<span data-ttu-id="58141-114">A parancsmag által eltávolított egyéni tartomány erőforrásnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="58141-114">Specifies the resource name of the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="58141-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58141-115">-DefaultProfile</span></span>
<span data-ttu-id="58141-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="58141-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="58141-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="58141-117">-EndpointName</span></span>
<span data-ttu-id="58141-118">Annak a végpontnak a nevét adja meg, amelyből a parancsmag eltávolít egy egyéni tartományt.</span><span class="sxs-lookup"><span data-stu-id="58141-118">Specifies the name of the endpoint from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="58141-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="58141-119">-PassThru</span></span>
<span data-ttu-id="58141-120">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="58141-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="58141-121">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="58141-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="58141-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="58141-122">-ProfileName</span></span>
<span data-ttu-id="58141-123">Annak a profilnak a nevét adja meg, amelyből a parancsmag eltávolít egy egyéni tartományt.</span><span class="sxs-lookup"><span data-stu-id="58141-123">Specifies the name of the profile from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="58141-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58141-124">-ResourceGroupName</span></span>
<span data-ttu-id="58141-125">Annak az erőforráscsoportnak a nevét adja meg, amelyből a parancsmag eltávolít egy egyéni tartományt.</span><span class="sxs-lookup"><span data-stu-id="58141-125">Specifies the name of the resource group from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="58141-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58141-126">-Confirm</span></span>
<span data-ttu-id="58141-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="58141-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58141-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58141-128">-WhatIf</span></span>
<span data-ttu-id="58141-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="58141-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58141-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="58141-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58141-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58141-131">CommonParameters</span></span>
<span data-ttu-id="58141-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58141-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58141-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58141-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58141-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="58141-134">INPUTS</span></span>

### <span data-ttu-id="58141-135">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="58141-135">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="58141-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="58141-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="58141-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="58141-137">OUTPUTS</span></span>

### <span data-ttu-id="58141-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="58141-138">System.Boolean</span></span>

## <span data-ttu-id="58141-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="58141-139">NOTES</span></span>

## <span data-ttu-id="58141-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="58141-140">RELATED LINKS</span></span>

[<span data-ttu-id="58141-141">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="58141-141">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="58141-142">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="58141-142">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="58141-143">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="58141-143">Test-AzCdnCustomDomain</span></span>](./Test-AzCdnCustomDomain.md)


