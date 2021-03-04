---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/remove-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOriginGroup.md
ms.openlocfilehash: a954b6c259b9e793ca4e35e99ecb4c710ab7a4e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919025"
---
# <span data-ttu-id="98fd4-101">Remove-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="98fd4-101">Remove-AzCdnOriginGroup</span></span>

## <span data-ttu-id="98fd4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98fd4-102">SYNOPSIS</span></span>
<span data-ttu-id="98fd4-103">CDN-forráscsoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="98fd4-103">Removes a CDN origin group</span></span>

## <span data-ttu-id="98fd4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="98fd4-104">SYNTAX</span></span>

### <span data-ttu-id="98fd4-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="98fd4-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnOriginGroup -OriginGroupName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="98fd4-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="98fd4-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCdnOriginGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98fd4-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="98fd4-107">ByObjectParameterSet</span></span>
```
Remove-AzCdnOriginGroup [-PassThru] -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98fd4-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="98fd4-108">DESCRIPTION</span></span>
<span data-ttu-id="98fd4-109">Remove-AzCdnOriginGroup eltávolítja a CDN-forráscsoportot a megadott végpontról.</span><span class="sxs-lookup"><span data-stu-id="98fd4-109">Remove-AzCdnOriginGroup will remove a CDN origin group from the specified endpoint.</span></span> 

## <span data-ttu-id="98fd4-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="98fd4-110">EXAMPLES</span></span>

### <span data-ttu-id="98fd4-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="98fd4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="98fd4-112">Ez a parancsmag eltávolítja a megadott origincsoportot a megadott végpontról.</span><span class="sxs-lookup"><span data-stu-id="98fd4-112">This cmdlet will remove the specified origin group from the given endpoint.</span></span> 

## <span data-ttu-id="98fd4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98fd4-113">PARAMETERS</span></span>

### <span data-ttu-id="98fd4-114">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="98fd4-114">-CdnOriginGroup</span></span>
<span data-ttu-id="98fd4-115">A CDN-forráscsoport objektuma.</span><span class="sxs-lookup"><span data-stu-id="98fd4-115">The CDN origin group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.OriginGroup.PSOriginGroup
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98fd4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98fd4-116">-DefaultProfile</span></span>
<span data-ttu-id="98fd4-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="98fd4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98fd4-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="98fd4-118">-EndpointName</span></span>
<span data-ttu-id="98fd4-119">Azure CDN-végpont neve.</span><span class="sxs-lookup"><span data-stu-id="98fd4-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="98fd4-120">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="98fd4-120">-OriginGroupName</span></span>
<span data-ttu-id="98fd4-121">Azure CDN-forráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="98fd4-121">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="98fd4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="98fd4-122">-PassThru</span></span>
<span data-ttu-id="98fd4-123">Visszatérési objektum, ha meg van adva.</span><span class="sxs-lookup"><span data-stu-id="98fd4-123">Return object if specified.</span></span>

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

### <span data-ttu-id="98fd4-124">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="98fd4-124">-ProfileName</span></span>
<span data-ttu-id="98fd4-125">Azure CDN-profil neve.</span><span class="sxs-lookup"><span data-stu-id="98fd4-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="98fd4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98fd4-126">-ResourceGroupName</span></span>
<span data-ttu-id="98fd4-127">Az Azure CDN-profil erőforráscsoportja.</span><span class="sxs-lookup"><span data-stu-id="98fd4-127">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="98fd4-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98fd4-128">-ResourceId</span></span>
<span data-ttu-id="98fd4-129">Az Azure CDN-forráscsoport erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="98fd4-129">The resource id of the Azure CDN origin group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98fd4-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="98fd4-130">-Confirm</span></span>
<span data-ttu-id="98fd4-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="98fd4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98fd4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98fd4-132">-WhatIf</span></span>
<span data-ttu-id="98fd4-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="98fd4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98fd4-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="98fd4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98fd4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98fd4-135">CommonParameters</span></span>
<span data-ttu-id="98fd4-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98fd4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98fd4-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="98fd4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98fd4-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="98fd4-138">INPUTS</span></span>

### <span data-ttu-id="98fd4-139">Nincs</span><span class="sxs-lookup"><span data-stu-id="98fd4-139">None</span></span>

## <span data-ttu-id="98fd4-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="98fd4-140">OUTPUTS</span></span>

### <span data-ttu-id="98fd4-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="98fd4-141">System.Boolean</span></span>

## <span data-ttu-id="98fd4-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="98fd4-142">NOTES</span></span>

## <span data-ttu-id="98fd4-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="98fd4-143">RELATED LINKS</span></span>
