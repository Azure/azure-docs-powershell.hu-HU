---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
ms.openlocfilehash: 133afe9b64fd9161bb7d39fadf6349803f9e2282
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153162"
---
# <span data-ttu-id="82bac-101">Remove-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="82bac-101">Remove-AzFrontDoor</span></span>

## <span data-ttu-id="82bac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82bac-102">SYNOPSIS</span></span>
<span data-ttu-id="82bac-103">A Front Door terheléselosztási eszközének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="82bac-103">Remove Front Door load balancer</span></span>

## <span data-ttu-id="82bac-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="82bac-104">SYNTAX</span></span>

### <span data-ttu-id="82bac-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="82bac-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoor -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82bac-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="82bac-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoor -InputObject <PSFrontDoor> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82bac-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="82bac-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoor -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82bac-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="82bac-108">DESCRIPTION</span></span>
<span data-ttu-id="82bac-109">A **Remove-AzFrontDoor** parancsmag eltávolítja a Front Door terheléselegyenlőt az aktuális előfizetés alatt</span><span class="sxs-lookup"><span data-stu-id="82bac-109">The **Remove-AzFrontDoor** cmdlet removes a Front Door load balancer under the current subscription</span></span>

## <span data-ttu-id="82bac-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="82bac-110">EXAMPLES</span></span>

### <span data-ttu-id="82bac-111">1. példa: Távolítsa el a "frontdoor1" csoportot az "rg1" erőforráscsoportból az aktuális előfizetés alatt.</span><span class="sxs-lookup"><span data-stu-id="82bac-111">Example 1: Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" -ResourceGroupName "rg1"
```

<span data-ttu-id="82bac-112">Távolítsa el a "frontdoor1" csoportot az "rg1" erőforráscsoportból az aktuális előfizetés alatt.</span><span class="sxs-lookup"><span data-stu-id="82bac-112">Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="82bac-113">2. példa: Távolítsa el az aktuális előfizetés alatti "rg1" erőforráscsoport összes FrontDoorját.</span><span class="sxs-lookup"><span data-stu-id="82bac-113">Example 2: Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1" | Remove-AzFrontDoor
```

<span data-ttu-id="82bac-114">Távolítsa el az aktuális előfizetés alatti "rg1" erőforráscsoport összes FrontDoorját.</span><span class="sxs-lookup"><span data-stu-id="82bac-114">Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="82bac-115">3. példa: Távolítsa el az aktuális előfizetés összes FrontDoors eszközét.</span><span class="sxs-lookup"><span data-stu-id="82bac-115">Example 3: Remove all FrontDoors under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor | Remove-AzFrontDoor
```

<span data-ttu-id="82bac-116">Távolítsa el az aktuális előfizetés összes FrontDoors eszközét.</span><span class="sxs-lookup"><span data-stu-id="82bac-116">Remove all FrontDoors under the current subscription.</span></span>

### <span data-ttu-id="82bac-117">4. példa: Az aktuális előfizetés alatt távolítsa el az összes "frontdoor1" nevű FrontDoorsot.</span><span class="sxs-lookup"><span data-stu-id="82bac-117">Example 4: Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" | Remove-AzFrontDoor
```

<span data-ttu-id="82bac-118">Távolítsa el az aktuális előfizetés alatt a "frontdoor1" nevű FrontDoorsokat.</span><span class="sxs-lookup"><span data-stu-id="82bac-118">Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>

## <span data-ttu-id="82bac-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82bac-119">PARAMETERS</span></span>

### <span data-ttu-id="82bac-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82bac-120">-DefaultProfile</span></span>
<span data-ttu-id="82bac-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="82bac-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82bac-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82bac-122">-InputObject</span></span>
<span data-ttu-id="82bac-123">The Front Door object to delete.</span><span class="sxs-lookup"><span data-stu-id="82bac-123">The Front Door object to delete.</span></span>

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

### <span data-ttu-id="82bac-124">-Name</span><span class="sxs-lookup"><span data-stu-id="82bac-124">-Name</span></span>
<span data-ttu-id="82bac-125">A törlendni kívánt előlapi ház neve.</span><span class="sxs-lookup"><span data-stu-id="82bac-125">The name of the Front Door to delete.</span></span>

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

### <span data-ttu-id="82bac-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="82bac-126">-PassThru</span></span>
<span data-ttu-id="82bac-127">Visszatérési objektum (ha meg van adva).</span><span class="sxs-lookup"><span data-stu-id="82bac-127">Return object (if specified).</span></span>

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

### <span data-ttu-id="82bac-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82bac-128">-ResourceGroupName</span></span>
<span data-ttu-id="82bac-129">Az az erőforráscsoport, amelyhez a Front Door tartozik.</span><span class="sxs-lookup"><span data-stu-id="82bac-129">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="82bac-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82bac-130">-ResourceId</span></span>
<span data-ttu-id="82bac-131">A törlendő front door erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="82bac-131">Resource Id of the Front Door to delete</span></span>

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

### <span data-ttu-id="82bac-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82bac-132">-Confirm</span></span>
<span data-ttu-id="82bac-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="82bac-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82bac-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82bac-134">-WhatIf</span></span>
<span data-ttu-id="82bac-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="82bac-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82bac-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="82bac-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82bac-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82bac-137">CommonParameters</span></span>
<span data-ttu-id="82bac-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82bac-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82bac-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="82bac-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82bac-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="82bac-140">INPUTS</span></span>

### <span data-ttu-id="82bac-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="82bac-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="82bac-142">System.String</span><span class="sxs-lookup"><span data-stu-id="82bac-142">System.String</span></span>

## <span data-ttu-id="82bac-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="82bac-143">OUTPUTS</span></span>

### <span data-ttu-id="82bac-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="82bac-144">System.Boolean</span></span>

## <span data-ttu-id="82bac-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="82bac-145">NOTES</span></span>

## <span data-ttu-id="82bac-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="82bac-146">RELATED LINKS</span></span>

<span data-ttu-id="82bac-147">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Get-AzFrontDoor](./Get-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="82bac-147">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Get-AzFrontDoor](./Get-AzFrontDoor.md)</span></span>