---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOriginGroup.md
ms.openlocfilehash: 081d5a73d6bd3cefff6f0c3bc57d3e0190f785a7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194805"
---
# <span data-ttu-id="21c89-101">Remove-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="21c89-101">Remove-AzCdnOriginGroup</span></span>

## <span data-ttu-id="21c89-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="21c89-102">SYNOPSIS</span></span>
<span data-ttu-id="21c89-103">CDN-származási csoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="21c89-103">Removes a CDN origin group</span></span>

## <span data-ttu-id="21c89-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="21c89-104">SYNTAX</span></span>

### <span data-ttu-id="21c89-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="21c89-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnOriginGroup -OriginGroupName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="21c89-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="21c89-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCdnOriginGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21c89-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="21c89-107">ByObjectParameterSet</span></span>
```
Remove-AzCdnOriginGroup [-PassThru] -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21c89-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="21c89-108">DESCRIPTION</span></span>
<span data-ttu-id="21c89-109">A Remove-AzCdnOriginGroup a megadott végpontról eltávolítja a CDN-származási csoportot.</span><span class="sxs-lookup"><span data-stu-id="21c89-109">Remove-AzCdnOriginGroup will remove a CDN origin group from the specified endpoint.</span></span> 

## <span data-ttu-id="21c89-110">Példák</span><span class="sxs-lookup"><span data-stu-id="21c89-110">EXAMPLES</span></span>

### <span data-ttu-id="21c89-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="21c89-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="21c89-112">Ez a parancsmag eltávolítja a megadott származási csoportot a megadott végpontról.</span><span class="sxs-lookup"><span data-stu-id="21c89-112">This cmdlet will remove the specified origin group from the given endpoint.</span></span> 

## <span data-ttu-id="21c89-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="21c89-113">PARAMETERS</span></span>

### <span data-ttu-id="21c89-114">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="21c89-114">-CdnOriginGroup</span></span>
<span data-ttu-id="21c89-115">A CDN származási csoport objektuma.</span><span class="sxs-lookup"><span data-stu-id="21c89-115">The CDN origin group object.</span></span>

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

### <span data-ttu-id="21c89-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21c89-116">-DefaultProfile</span></span>
<span data-ttu-id="21c89-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="21c89-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21c89-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="21c89-118">-EndpointName</span></span>
<span data-ttu-id="21c89-119">Azure CDN végpont neve.</span><span class="sxs-lookup"><span data-stu-id="21c89-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="21c89-120">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="21c89-120">-OriginGroupName</span></span>
<span data-ttu-id="21c89-121">Azure CDN származási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="21c89-121">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="21c89-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="21c89-122">-PassThru</span></span>
<span data-ttu-id="21c89-123">Ha meg van adva a visszatérési objektum</span><span class="sxs-lookup"><span data-stu-id="21c89-123">Return object if specified.</span></span>

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

### <span data-ttu-id="21c89-124">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="21c89-124">-ProfileName</span></span>
<span data-ttu-id="21c89-125">Azure CDN-profil neve.</span><span class="sxs-lookup"><span data-stu-id="21c89-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="21c89-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21c89-126">-ResourceGroupName</span></span>
<span data-ttu-id="21c89-127">Az Azure CDN-profil erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="21c89-127">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="21c89-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21c89-128">-ResourceId</span></span>
<span data-ttu-id="21c89-129">Az Azure CDN Origin csoport erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="21c89-129">The resource id of the Azure CDN origin group.</span></span>

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

### <span data-ttu-id="21c89-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="21c89-130">-Confirm</span></span>
<span data-ttu-id="21c89-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="21c89-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21c89-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21c89-132">-WhatIf</span></span>
<span data-ttu-id="21c89-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="21c89-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21c89-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="21c89-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21c89-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21c89-135">CommonParameters</span></span>
<span data-ttu-id="21c89-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="21c89-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21c89-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="21c89-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21c89-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="21c89-138">INPUTS</span></span>

### <span data-ttu-id="21c89-139">Nincs</span><span class="sxs-lookup"><span data-stu-id="21c89-139">None</span></span>

## <span data-ttu-id="21c89-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="21c89-140">OUTPUTS</span></span>

### <span data-ttu-id="21c89-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="21c89-141">System.Boolean</span></span>

## <span data-ttu-id="21c89-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="21c89-142">NOTES</span></span>

## <span data-ttu-id="21c89-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="21c89-143">RELATED LINKS</span></span>
