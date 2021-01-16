---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOrigin.md
ms.openlocfilehash: 8198d189d9619528bdc7fb80d30285ce9126dfed
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336785"
---
# <span data-ttu-id="92276-101">Remove-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="92276-101">Remove-AzCdnOrigin</span></span>

## <span data-ttu-id="92276-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92276-102">SYNOPSIS</span></span>
<span data-ttu-id="92276-103">CDN-forrás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="92276-103">Removes a CDN origin</span></span>

## <span data-ttu-id="92276-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="92276-104">SYNTAX</span></span>

### <span data-ttu-id="92276-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="92276-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnOrigin -OriginName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="92276-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="92276-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCdnOrigin -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92276-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="92276-107">ByObjectParameterSet</span></span>
```
Remove-AzCdnOrigin [-PassThru] -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92276-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="92276-108">DESCRIPTION</span></span>
<span data-ttu-id="92276-109">Remove-AzCdnOrigin egy CDN-forrást a megadott végpontról.</span><span class="sxs-lookup"><span data-stu-id="92276-109">Remove-AzCdnOrigin will delete a CDN origin from the given endpoint.</span></span> <span data-ttu-id="92276-110">Ha a forrás az egyetlen forrás a megadott végponton belül, akkor a törlés sikertelen lesz, mivel legalább 1 forrásra van szükség.</span><span class="sxs-lookup"><span data-stu-id="92276-110">If the origin is the only origin within the specified endpoint, then the deletion will fail since at least 1 origin is needed.</span></span> 

## <span data-ttu-id="92276-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="92276-111">EXAMPLES</span></span>

### <span data-ttu-id="92276-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="92276-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzCdnOrigin -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginName $originName 
```
<span data-ttu-id="92276-113">Ez a parancsmag eltávolítja a megadott origint a megadott végpontról.</span><span class="sxs-lookup"><span data-stu-id="92276-113">This cmdlet will remove the specified origin from the given endpoint.</span></span> 

## <span data-ttu-id="92276-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92276-114">PARAMETERS</span></span>

### <span data-ttu-id="92276-115">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="92276-115">-CdnOrigin</span></span>
<span data-ttu-id="92276-116">A CDN-forrásobjektum.</span><span class="sxs-lookup"><span data-stu-id="92276-116">The CDN origin object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92276-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92276-117">-DefaultProfile</span></span>
<span data-ttu-id="92276-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="92276-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92276-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="92276-119">-EndpointName</span></span>
<span data-ttu-id="92276-120">Azure CDN-végpont neve.</span><span class="sxs-lookup"><span data-stu-id="92276-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="92276-121">-OriginName</span><span class="sxs-lookup"><span data-stu-id="92276-121">-OriginName</span></span>
<span data-ttu-id="92276-122">Azure CDN-forrás neve.</span><span class="sxs-lookup"><span data-stu-id="92276-122">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="92276-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92276-123">-PassThru</span></span>
<span data-ttu-id="92276-124">Visszatérési objektum, ha meg van adva.</span><span class="sxs-lookup"><span data-stu-id="92276-124">Return object if specified.</span></span>

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

### <span data-ttu-id="92276-125">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="92276-125">-ProfileName</span></span>
<span data-ttu-id="92276-126">Azure CDN-profil neve.</span><span class="sxs-lookup"><span data-stu-id="92276-126">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="92276-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92276-127">-ResourceGroupName</span></span>
<span data-ttu-id="92276-128">Az Azure CDN-profil erőforráscsoportja.</span><span class="sxs-lookup"><span data-stu-id="92276-128">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="92276-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92276-129">-ResourceId</span></span>
<span data-ttu-id="92276-130">Az Azure CDN-forrás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="92276-130">The resource id of the Azure CDN origin.</span></span>

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

### <span data-ttu-id="92276-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92276-131">-Confirm</span></span>
<span data-ttu-id="92276-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="92276-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92276-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92276-133">-WhatIf</span></span>
<span data-ttu-id="92276-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="92276-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92276-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="92276-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92276-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92276-136">CommonParameters</span></span>
<span data-ttu-id="92276-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92276-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92276-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92276-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92276-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="92276-139">INPUTS</span></span>

### <span data-ttu-id="92276-140">Nincs</span><span class="sxs-lookup"><span data-stu-id="92276-140">None</span></span>

## <span data-ttu-id="92276-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="92276-141">OUTPUTS</span></span>

### <span data-ttu-id="92276-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="92276-142">System.Boolean</span></span>

## <span data-ttu-id="92276-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="92276-143">NOTES</span></span>

## <span data-ttu-id="92276-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="92276-144">RELATED LINKS</span></span>
