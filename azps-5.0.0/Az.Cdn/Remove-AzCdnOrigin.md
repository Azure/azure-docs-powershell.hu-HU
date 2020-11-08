---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOrigin.md
ms.openlocfilehash: 8198d189d9619528bdc7fb80d30285ce9126dfed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194806"
---
# <span data-ttu-id="916c0-101">Remove-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="916c0-101">Remove-AzCdnOrigin</span></span>

## <span data-ttu-id="916c0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="916c0-102">SYNOPSIS</span></span>
<span data-ttu-id="916c0-103">CDN-Origó eltávolítása</span><span class="sxs-lookup"><span data-stu-id="916c0-103">Removes a CDN origin</span></span>

## <span data-ttu-id="916c0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="916c0-104">SYNTAX</span></span>

### <span data-ttu-id="916c0-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="916c0-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnOrigin -OriginName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="916c0-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="916c0-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCdnOrigin -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="916c0-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="916c0-107">ByObjectParameterSet</span></span>
```
Remove-AzCdnOrigin [-PassThru] -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="916c0-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="916c0-108">DESCRIPTION</span></span>
<span data-ttu-id="916c0-109">A Remove-AzCdnOrigin egy CDN-kezdőpontot fog törölni a megadott végpontról.</span><span class="sxs-lookup"><span data-stu-id="916c0-109">Remove-AzCdnOrigin will delete a CDN origin from the given endpoint.</span></span> <span data-ttu-id="916c0-110">Ha a származási hely a megadott végponton belül az egyetlen eredete, akkor a törlés meghiúsul, mert legalább 1 származási pontra van szükség.</span><span class="sxs-lookup"><span data-stu-id="916c0-110">If the origin is the only origin within the specified endpoint, then the deletion will fail since at least 1 origin is needed.</span></span> 

## <span data-ttu-id="916c0-111">Példák</span><span class="sxs-lookup"><span data-stu-id="916c0-111">EXAMPLES</span></span>

### <span data-ttu-id="916c0-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="916c0-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzCdnOrigin -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginName $originName 
```
<span data-ttu-id="916c0-113">Ez a parancsmag eltávolítja a megadott kezdőpontot az adott végpontról.</span><span class="sxs-lookup"><span data-stu-id="916c0-113">This cmdlet will remove the specified origin from the given endpoint.</span></span> 

## <span data-ttu-id="916c0-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="916c0-114">PARAMETERS</span></span>

### <span data-ttu-id="916c0-115">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="916c0-115">-CdnOrigin</span></span>
<span data-ttu-id="916c0-116">A CDN Origin objektuma.</span><span class="sxs-lookup"><span data-stu-id="916c0-116">The CDN origin object.</span></span>

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

### <span data-ttu-id="916c0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="916c0-117">-DefaultProfile</span></span>
<span data-ttu-id="916c0-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="916c0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="916c0-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="916c0-119">-EndpointName</span></span>
<span data-ttu-id="916c0-120">Azure CDN végpont neve.</span><span class="sxs-lookup"><span data-stu-id="916c0-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="916c0-121">-OriginName</span><span class="sxs-lookup"><span data-stu-id="916c0-121">-OriginName</span></span>
<span data-ttu-id="916c0-122">Azure CDN Origin név.</span><span class="sxs-lookup"><span data-stu-id="916c0-122">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="916c0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="916c0-123">-PassThru</span></span>
<span data-ttu-id="916c0-124">Ha meg van adva a visszatérési objektum</span><span class="sxs-lookup"><span data-stu-id="916c0-124">Return object if specified.</span></span>

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

### <span data-ttu-id="916c0-125">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="916c0-125">-ProfileName</span></span>
<span data-ttu-id="916c0-126">Azure CDN-profil neve.</span><span class="sxs-lookup"><span data-stu-id="916c0-126">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="916c0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="916c0-127">-ResourceGroupName</span></span>
<span data-ttu-id="916c0-128">Az Azure CDN-profil erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="916c0-128">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="916c0-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="916c0-129">-ResourceId</span></span>
<span data-ttu-id="916c0-130">Az Azure CDN kezdőpontjának erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="916c0-130">The resource id of the Azure CDN origin.</span></span>

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

### <span data-ttu-id="916c0-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="916c0-131">-Confirm</span></span>
<span data-ttu-id="916c0-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="916c0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="916c0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="916c0-133">-WhatIf</span></span>
<span data-ttu-id="916c0-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="916c0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="916c0-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="916c0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="916c0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="916c0-136">CommonParameters</span></span>
<span data-ttu-id="916c0-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="916c0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="916c0-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="916c0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="916c0-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="916c0-139">INPUTS</span></span>

### <span data-ttu-id="916c0-140">Nincs</span><span class="sxs-lookup"><span data-stu-id="916c0-140">None</span></span>

## <span data-ttu-id="916c0-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="916c0-141">OUTPUTS</span></span>

### <span data-ttu-id="916c0-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="916c0-142">System.Boolean</span></span>

## <span data-ttu-id="916c0-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="916c0-143">NOTES</span></span>

## <span data-ttu-id="916c0-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="916c0-144">RELATED LINKS</span></span>
