---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/remove-azurermfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoor.md
ms.openlocfilehash: 8eae5034080bd1035cfe7e8331ca015820688e63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93671969"
---
# <span data-ttu-id="99044-101">Remove-AzureRmFrontDoor</span><span class="sxs-lookup"><span data-stu-id="99044-101">Remove-AzureRmFrontDoor</span></span>

## <span data-ttu-id="99044-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="99044-102">SYNOPSIS</span></span>
<span data-ttu-id="99044-103">A bejárati ajtó kiegyenlítő eltávolítása</span><span class="sxs-lookup"><span data-stu-id="99044-103">Remove Front Door load balancer</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99044-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="99044-104">SYNTAX</span></span>

### <span data-ttu-id="99044-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="99044-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzureRmFrontDoor -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99044-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="99044-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmFrontDoor -InputObject <PSFrontDoor> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99044-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="99044-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmFrontDoor -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99044-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="99044-108">DESCRIPTION</span></span>
<span data-ttu-id="99044-109">A **Remove-AzureRmFrontDoor** parancsmag a jelenlegi előfizetés alatt eltávolítja az első ajtót.</span><span class="sxs-lookup"><span data-stu-id="99044-109">The **Remove-AzureRmFrontDoor** cmdlet removes a Front Door load balancer under the current subscription</span></span>

## <span data-ttu-id="99044-110">Példák</span><span class="sxs-lookup"><span data-stu-id="99044-110">EXAMPLES</span></span>

### <span data-ttu-id="99044-111">1. példa: a "frontdoor1" szó eltávolítása a jelenlegi előfizetés alatti "rg1" erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="99044-111">Example 1: Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzureRmFrontDoor -Name "frontdoor1" -ResourceGroupName "rg1"
```

<span data-ttu-id="99044-112">A jelenlegi előfizetés alatti "rg1" erőforráscsoport "frontdoor1" eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="99044-112">Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="99044-113">2. példa: a jelenlegi előfizetés alatti "rg1" erőforráscsoport összes FrontDoors eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="99044-113">Example 2: Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor -ResourceGroupName "rg1" | Remove-AzureRmFrontDoor
```

<span data-ttu-id="99044-114">Távolítsa el az összes FrontDoors az erőforráscsoport "rg1" csoportjában az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="99044-114">Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="99044-115">3. példa: az összes FrontDoors eltávolítása az aktuális előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="99044-115">Example 3: Remove all FrontDoors under the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor | Remove-AzureRmFrontDoor
```

<span data-ttu-id="99044-116">Az összes FrontDoors eltávolítása a jelenlegi előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="99044-116">Remove all FrontDoors under the current subscription.</span></span>

### <span data-ttu-id="99044-117">Példa 4: az összes FrontDoors eltávolítása a "frontdoor1" névvel a jelenlegi előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="99044-117">Example 4: Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzureRmFrontDoor -Name "frontdoor1" | Remove-AzureRmFrontDoor
```

<span data-ttu-id="99044-118">Az összes FrontDoors eltávolítása a "frontdoor1" névvel a jelenlegi előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="99044-118">Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>

## <span data-ttu-id="99044-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="99044-119">PARAMETERS</span></span>

### <span data-ttu-id="99044-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99044-120">-DefaultProfile</span></span>
<span data-ttu-id="99044-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="99044-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99044-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99044-122">-InputObject</span></span>
<span data-ttu-id="99044-123">A törlendő bejárati ajtó objektuma.</span><span class="sxs-lookup"><span data-stu-id="99044-123">The Front Door object to delete.</span></span>

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

### <span data-ttu-id="99044-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="99044-124">-Name</span></span>
<span data-ttu-id="99044-125">A törlendő bejárati ajtó neve.</span><span class="sxs-lookup"><span data-stu-id="99044-125">The name of the Front Door to delete.</span></span>

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

### <span data-ttu-id="99044-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99044-126">-PassThru</span></span>
<span data-ttu-id="99044-127">Visszatérési objektum (ha meg van adva)</span><span class="sxs-lookup"><span data-stu-id="99044-127">Return object (if specified).</span></span>

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

### <span data-ttu-id="99044-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99044-128">-ResourceGroupName</span></span>
<span data-ttu-id="99044-129">Az az erőforráscsoport, amelyhez az első ajtó tartozik.</span><span class="sxs-lookup"><span data-stu-id="99044-129">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="99044-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99044-130">-ResourceId</span></span>
<span data-ttu-id="99044-131">A törlendő bejárati ajtó erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="99044-131">Resource Id of the Front Door to delete</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99044-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="99044-132">-Confirm</span></span>
<span data-ttu-id="99044-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="99044-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99044-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99044-134">-WhatIf</span></span>
<span data-ttu-id="99044-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="99044-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99044-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="99044-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99044-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99044-137">CommonParameters</span></span>
<span data-ttu-id="99044-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="99044-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99044-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99044-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99044-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="99044-140">INPUTS</span></span>

### <span data-ttu-id="99044-141">Microsoft. Azure. Command. FrontDoor. models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="99044-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="99044-142">System. String</span><span class="sxs-lookup"><span data-stu-id="99044-142">System.String</span></span>

### <span data-ttu-id="99044-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="99044-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="99044-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="99044-144">OUTPUTS</span></span>

### <span data-ttu-id="99044-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="99044-145">System.Boolean</span></span>

## <span data-ttu-id="99044-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="99044-146">NOTES</span></span>

## <span data-ttu-id="99044-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="99044-147">RELATED LINKS</span></span>

<span data-ttu-id="99044-148">[Új – AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="99044-148">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md)</span></span>
