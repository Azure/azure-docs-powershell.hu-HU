---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
ms.openlocfilehash: 133afe9b64fd9161bb7d39fadf6349803f9e2282
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182231"
---
# <span data-ttu-id="65fe6-101">Remove-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="65fe6-101">Remove-AzFrontDoor</span></span>

## <span data-ttu-id="65fe6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="65fe6-102">SYNOPSIS</span></span>
<span data-ttu-id="65fe6-103">A bejárati ajtó kiegyenlítő eltávolítása</span><span class="sxs-lookup"><span data-stu-id="65fe6-103">Remove Front Door load balancer</span></span>

## <span data-ttu-id="65fe6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="65fe6-104">SYNTAX</span></span>

### <span data-ttu-id="65fe6-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="65fe6-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoor -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65fe6-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="65fe6-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoor -InputObject <PSFrontDoor> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65fe6-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="65fe6-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoor -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65fe6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="65fe6-108">DESCRIPTION</span></span>
<span data-ttu-id="65fe6-109">A **Remove-AzFrontDoor** parancsmag a jelenlegi előfizetés alatt eltávolítja az első ajtót.</span><span class="sxs-lookup"><span data-stu-id="65fe6-109">The **Remove-AzFrontDoor** cmdlet removes a Front Door load balancer under the current subscription</span></span>

## <span data-ttu-id="65fe6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="65fe6-110">EXAMPLES</span></span>

### <span data-ttu-id="65fe6-111">1. példa: a "frontdoor1" szó eltávolítása a jelenlegi előfizetés alatti "rg1" erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="65fe6-111">Example 1: Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" -ResourceGroupName "rg1"
```

<span data-ttu-id="65fe6-112">A jelenlegi előfizetés alatti "rg1" erőforráscsoport "frontdoor1" eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="65fe6-112">Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="65fe6-113">2. példa: a jelenlegi előfizetés alatti "rg1" erőforráscsoport összes FrontDoors eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="65fe6-113">Example 2: Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1" | Remove-AzFrontDoor
```

<span data-ttu-id="65fe6-114">Távolítsa el az összes FrontDoors az erőforráscsoport "rg1" csoportjában az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="65fe6-114">Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="65fe6-115">3. példa: az összes FrontDoors eltávolítása az aktuális előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="65fe6-115">Example 3: Remove all FrontDoors under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor | Remove-AzFrontDoor
```

<span data-ttu-id="65fe6-116">Az összes FrontDoors eltávolítása a jelenlegi előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="65fe6-116">Remove all FrontDoors under the current subscription.</span></span>

### <span data-ttu-id="65fe6-117">Példa 4: az összes FrontDoors eltávolítása a "frontdoor1" névvel a jelenlegi előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="65fe6-117">Example 4: Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" | Remove-AzFrontDoor
```

<span data-ttu-id="65fe6-118">Az összes FrontDoors eltávolítása a "frontdoor1" névvel a jelenlegi előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="65fe6-118">Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>

## <span data-ttu-id="65fe6-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="65fe6-119">PARAMETERS</span></span>

### <span data-ttu-id="65fe6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65fe6-120">-DefaultProfile</span></span>
<span data-ttu-id="65fe6-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="65fe6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65fe6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65fe6-122">-InputObject</span></span>
<span data-ttu-id="65fe6-123">A törlendő bejárati ajtó objektuma.</span><span class="sxs-lookup"><span data-stu-id="65fe6-123">The Front Door object to delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65fe6-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="65fe6-124">-Name</span></span>
<span data-ttu-id="65fe6-125">A törlendő bejárati ajtó neve.</span><span class="sxs-lookup"><span data-stu-id="65fe6-125">The name of the Front Door to delete.</span></span>

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

### <span data-ttu-id="65fe6-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="65fe6-126">-PassThru</span></span>
<span data-ttu-id="65fe6-127">Visszatérési objektum (ha meg van adva)</span><span class="sxs-lookup"><span data-stu-id="65fe6-127">Return object (if specified).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65fe6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65fe6-128">-ResourceGroupName</span></span>
<span data-ttu-id="65fe6-129">Az az erőforráscsoport, amelyhez az első ajtó tartozik.</span><span class="sxs-lookup"><span data-stu-id="65fe6-129">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="65fe6-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65fe6-130">-ResourceId</span></span>
<span data-ttu-id="65fe6-131">A törlendő bejárati ajtó erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="65fe6-131">Resource Id of the Front Door to delete</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65fe6-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="65fe6-132">-Confirm</span></span>
<span data-ttu-id="65fe6-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="65fe6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65fe6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65fe6-134">-WhatIf</span></span>
<span data-ttu-id="65fe6-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="65fe6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65fe6-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="65fe6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65fe6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65fe6-137">CommonParameters</span></span>
<span data-ttu-id="65fe6-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="65fe6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65fe6-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="65fe6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65fe6-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="65fe6-140">INPUTS</span></span>

### <span data-ttu-id="65fe6-141">Microsoft. Azure. Command. FrontDoor. models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="65fe6-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="65fe6-142">System. String</span><span class="sxs-lookup"><span data-stu-id="65fe6-142">System.String</span></span>

## <span data-ttu-id="65fe6-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="65fe6-143">OUTPUTS</span></span>

### <span data-ttu-id="65fe6-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="65fe6-144">System.Boolean</span></span>

## <span data-ttu-id="65fe6-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="65fe6-145">NOTES</span></span>

## <span data-ttu-id="65fe6-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="65fe6-146">RELATED LINKS</span></span>

<span data-ttu-id="65fe6-147">[Új – AzFrontDoor](./New-AzFrontDoor.md) 
 [Get-AzFrontDoor](./Get-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="65fe6-147">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Get-AzFrontDoor](./Get-AzFrontDoor.md)</span></span>