---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
ms.openlocfilehash: 133afe9b64fd9161bb7d39fadf6349803f9e2282
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332225"
---
# <span data-ttu-id="6d11c-101">Remove-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="6d11c-101">Remove-AzFrontDoor</span></span>

## <span data-ttu-id="6d11c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d11c-102">SYNOPSIS</span></span>
<span data-ttu-id="6d11c-103">A Front Door terheléselosztási eszközének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="6d11c-103">Remove Front Door load balancer</span></span>

## <span data-ttu-id="6d11c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6d11c-104">SYNTAX</span></span>

### <span data-ttu-id="6d11c-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6d11c-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoor -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d11c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d11c-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoor -InputObject <PSFrontDoor> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d11c-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d11c-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoor -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d11c-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6d11c-108">DESCRIPTION</span></span>
<span data-ttu-id="6d11c-109">A **Remove-AzFrontDoor** parancsmag eltávolítja a Front Door terheléselegyenlőt az aktuális előfizetés alatt</span><span class="sxs-lookup"><span data-stu-id="6d11c-109">The **Remove-AzFrontDoor** cmdlet removes a Front Door load balancer under the current subscription</span></span>

## <span data-ttu-id="6d11c-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6d11c-110">EXAMPLES</span></span>

### <span data-ttu-id="6d11c-111">1. példa: Távolítsa el a "frontdoor1" csoportot az "rg1" erőforráscsoportból az aktuális előfizetés alatt.</span><span class="sxs-lookup"><span data-stu-id="6d11c-111">Example 1: Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" -ResourceGroupName "rg1"
```

<span data-ttu-id="6d11c-112">Távolítsa el a "frontdoor1" csoportot az "rg1" erőforráscsoportból az aktuális előfizetés alatt.</span><span class="sxs-lookup"><span data-stu-id="6d11c-112">Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="6d11c-113">2. példa: Távolítsa el az aktuális előfizetés alatti "rg1" erőforráscsoport összes FrontDoorját.</span><span class="sxs-lookup"><span data-stu-id="6d11c-113">Example 2: Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1" | Remove-AzFrontDoor
```

<span data-ttu-id="6d11c-114">Távolítsa el az aktuális előfizetés alatti "rg1" erőforráscsoport összes FrontDoorját.</span><span class="sxs-lookup"><span data-stu-id="6d11c-114">Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="6d11c-115">3. példa: Távolítsa el az aktuális előfizetés összes FrontDoors eszközét.</span><span class="sxs-lookup"><span data-stu-id="6d11c-115">Example 3: Remove all FrontDoors under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor | Remove-AzFrontDoor
```

<span data-ttu-id="6d11c-116">Távolítsa el az aktuális előfizetés összes FrontDoors eszközét.</span><span class="sxs-lookup"><span data-stu-id="6d11c-116">Remove all FrontDoors under the current subscription.</span></span>

### <span data-ttu-id="6d11c-117">4. példa: Távolítsa el az aktuális előfizetés alatt az összes "frontdoor1" nevű FrontDoorsot.</span><span class="sxs-lookup"><span data-stu-id="6d11c-117">Example 4: Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" | Remove-AzFrontDoor
```

<span data-ttu-id="6d11c-118">Távolítsa el az aktuális előfizetés alatt a "frontdoor1" nevű FrontDoorsokat.</span><span class="sxs-lookup"><span data-stu-id="6d11c-118">Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>

## <span data-ttu-id="6d11c-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d11c-119">PARAMETERS</span></span>

### <span data-ttu-id="6d11c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d11c-120">-DefaultProfile</span></span>
<span data-ttu-id="6d11c-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6d11c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d11c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d11c-122">-InputObject</span></span>
<span data-ttu-id="6d11c-123">The Front Door object to delete.</span><span class="sxs-lookup"><span data-stu-id="6d11c-123">The Front Door object to delete.</span></span>

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

### <span data-ttu-id="6d11c-124">-Name</span><span class="sxs-lookup"><span data-stu-id="6d11c-124">-Name</span></span>
<span data-ttu-id="6d11c-125">A törlendni kívánt előlapi ház neve.</span><span class="sxs-lookup"><span data-stu-id="6d11c-125">The name of the Front Door to delete.</span></span>

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

### <span data-ttu-id="6d11c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d11c-126">-PassThru</span></span>
<span data-ttu-id="6d11c-127">Visszatérési objektum (ha meg van adva).</span><span class="sxs-lookup"><span data-stu-id="6d11c-127">Return object (if specified).</span></span>

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

### <span data-ttu-id="6d11c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d11c-128">-ResourceGroupName</span></span>
<span data-ttu-id="6d11c-129">Az erőforráscsoport, amelyhez a Front Door tartozik.</span><span class="sxs-lookup"><span data-stu-id="6d11c-129">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="6d11c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d11c-130">-ResourceId</span></span>
<span data-ttu-id="6d11c-131">A törlendő front door erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="6d11c-131">Resource Id of the Front Door to delete</span></span>

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

### <span data-ttu-id="6d11c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d11c-132">-Confirm</span></span>
<span data-ttu-id="6d11c-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6d11c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d11c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d11c-134">-WhatIf</span></span>
<span data-ttu-id="6d11c-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6d11c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d11c-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6d11c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d11c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d11c-137">CommonParameters</span></span>
<span data-ttu-id="6d11c-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d11c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d11c-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6d11c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d11c-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6d11c-140">INPUTS</span></span>

### <span data-ttu-id="6d11c-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="6d11c-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="6d11c-142">System.String</span><span class="sxs-lookup"><span data-stu-id="6d11c-142">System.String</span></span>

## <span data-ttu-id="6d11c-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d11c-143">OUTPUTS</span></span>

### <span data-ttu-id="6d11c-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6d11c-144">System.Boolean</span></span>

## <span data-ttu-id="6d11c-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6d11c-145">NOTES</span></span>

## <span data-ttu-id="6d11c-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6d11c-146">RELATED LINKS</span></span>

<span data-ttu-id="6d11c-147">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Get-AzFrontDoor](./Get-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="6d11c-147">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Get-AzFrontDoor](./Get-AzFrontDoor.md)</span></span>