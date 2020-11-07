---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
ms.openlocfilehash: fbbd2b5047811f09a8142eea2a84e8f77c405be3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666403"
---
# <span data-ttu-id="b2809-101">Remove-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="b2809-101">Remove-AzFrontDoor</span></span>

## <span data-ttu-id="b2809-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b2809-102">SYNOPSIS</span></span>
<span data-ttu-id="b2809-103">A bejárati ajtó kiegyenlítő eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b2809-103">Remove Front Door load balancer</span></span>

## <span data-ttu-id="b2809-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b2809-104">SYNTAX</span></span>

### <span data-ttu-id="b2809-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b2809-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoor -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2809-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2809-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoor -InputObject <PSFrontDoor> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2809-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2809-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoor -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2809-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b2809-108">DESCRIPTION</span></span>
<span data-ttu-id="b2809-109">A **Remove-AzFrontDoor** parancsmag a jelenlegi előfizetés alatt eltávolítja az első ajtót.</span><span class="sxs-lookup"><span data-stu-id="b2809-109">The **Remove-AzFrontDoor** cmdlet removes a Front Door load balancer under the current subscription</span></span>

## <span data-ttu-id="b2809-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b2809-110">EXAMPLES</span></span>

### <span data-ttu-id="b2809-111">1. példa: a "frontdoor1" szó eltávolítása a jelenlegi előfizetés alatti "rg1" erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="b2809-111">Example 1: Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" -ResourceGroupName "rg1"
```

<span data-ttu-id="b2809-112">A jelenlegi előfizetés alatti "rg1" erőforráscsoport "frontdoor1" eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="b2809-112">Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="b2809-113">2. példa: a jelenlegi előfizetés alatti "rg1" erőforráscsoport összes FrontDoors eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="b2809-113">Example 2: Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1" | Remove-AzFrontDoor
```

<span data-ttu-id="b2809-114">Távolítsa el az összes FrontDoors az erőforráscsoport "rg1" csoportjában az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="b2809-114">Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="b2809-115">3. példa: az összes FrontDoors eltávolítása az aktuális előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="b2809-115">Example 3: Remove all FrontDoors under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor | Remove-AzFrontDoor
```

<span data-ttu-id="b2809-116">Az összes FrontDoors eltávolítása a jelenlegi előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="b2809-116">Remove all FrontDoors under the current subscription.</span></span>

### <span data-ttu-id="b2809-117">Példa 4: az összes FrontDoors eltávolítása a "frontdoor1" névvel a jelenlegi előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="b2809-117">Example 4: Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" | Remove-AzFrontDoor
```

<span data-ttu-id="b2809-118">Az összes FrontDoors eltávolítása a "frontdoor1" névvel a jelenlegi előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="b2809-118">Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>

## <span data-ttu-id="b2809-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b2809-119">PARAMETERS</span></span>

### <span data-ttu-id="b2809-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2809-120">-DefaultProfile</span></span>
<span data-ttu-id="b2809-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b2809-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2809-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2809-122">-InputObject</span></span>
<span data-ttu-id="b2809-123">A törlendő bejárati ajtó objektuma.</span><span class="sxs-lookup"><span data-stu-id="b2809-123">The Front Door object to delete.</span></span>

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

### <span data-ttu-id="b2809-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b2809-124">-Name</span></span>
<span data-ttu-id="b2809-125">A törlendő bejárati ajtó neve.</span><span class="sxs-lookup"><span data-stu-id="b2809-125">The name of the Front Door to delete.</span></span>

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

### <span data-ttu-id="b2809-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b2809-126">-PassThru</span></span>
<span data-ttu-id="b2809-127">Visszatérési objektum (ha meg van adva)</span><span class="sxs-lookup"><span data-stu-id="b2809-127">Return object (if specified).</span></span>

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

### <span data-ttu-id="b2809-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2809-128">-ResourceGroupName</span></span>
<span data-ttu-id="b2809-129">Az az erőforráscsoport, amelyhez az első ajtó tartozik.</span><span class="sxs-lookup"><span data-stu-id="b2809-129">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="b2809-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2809-130">-ResourceId</span></span>
<span data-ttu-id="b2809-131">A törlendő bejárati ajtó erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="b2809-131">Resource Id of the Front Door to delete</span></span>

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

### <span data-ttu-id="b2809-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b2809-132">-Confirm</span></span>
<span data-ttu-id="b2809-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b2809-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2809-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2809-134">-WhatIf</span></span>
<span data-ttu-id="b2809-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b2809-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2809-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b2809-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2809-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2809-137">CommonParameters</span></span>
<span data-ttu-id="b2809-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b2809-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2809-139">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b2809-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2809-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2809-140">INPUTS</span></span>

### <span data-ttu-id="b2809-141">Microsoft. Azure. Command. FrontDoor. models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="b2809-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="b2809-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b2809-142">System.String</span></span>

## <span data-ttu-id="b2809-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2809-143">OUTPUTS</span></span>

### <span data-ttu-id="b2809-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b2809-144">System.Boolean</span></span>

## <span data-ttu-id="b2809-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b2809-145">NOTES</span></span>

## <span data-ttu-id="b2809-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b2809-146">RELATED LINKS</span></span>

<span data-ttu-id="b2809-147">[Új – AzFrontDoor](./New-AzFrontDoor.md) 
 [Get-AzFrontDoor](./Get-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="b2809-147">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Get-AzFrontDoor](./Get-AzFrontDoor.md)</span></span>