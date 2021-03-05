---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/remove-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorWafPolicy.md
ms.openlocfilehash: 707f3157cead45d501cdfdaf357222cdaceac826
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015222"
---
# <span data-ttu-id="ead85-101">Remove-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="ead85-101">Remove-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="ead85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ead85-102">SYNOPSIS</span></span>
<span data-ttu-id="ead85-103">WaF-házirend eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ead85-103">Remove WAF policy</span></span>

## <span data-ttu-id="ead85-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ead85-104">SYNTAX</span></span>

### <span data-ttu-id="ead85-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ead85-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ead85-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ead85-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorWafPolicy -InputObject <PSPolicy> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ead85-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ead85-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorWafPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ead85-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ead85-108">DESCRIPTION</span></span>
<span data-ttu-id="ead85-109">A **Remove-AzFrontDoorWafPolicy** parancsmag eltávolít egy WAF-házirendet a jelenlegi előfizetés alatt</span><span class="sxs-lookup"><span data-stu-id="ead85-109">The **Remove-AzFrontDoorWafPolicy** cmdlet removes a WAF policy under the current subscription</span></span>

## <span data-ttu-id="ead85-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ead85-110">EXAMPLES</span></span>

### <span data-ttu-id="ead85-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="ead85-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName
```

<span data-ttu-id="ead85-112">Távolítsa el a $policyName waf $resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="ead85-112">Remove the WAF policy called $policyName in $resourceGroupName.</span></span>

### <span data-ttu-id="ead85-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="ead85-113">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName | Remove-AzFrontDoorWafPolicy
```

<span data-ttu-id="ead85-114">Távolítsa el az összes WaF-házirendet a $resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="ead85-114">Remove all WAF policy in $resourceGroupName.</span></span>

## <span data-ttu-id="ead85-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ead85-115">PARAMETERS</span></span>

### <span data-ttu-id="ead85-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ead85-116">-DefaultProfile</span></span>
<span data-ttu-id="ead85-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ead85-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ead85-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ead85-118">-InputObject</span></span>
<span data-ttu-id="ead85-119">A törölni kívánt WAF-házirendobjektum.</span><span class="sxs-lookup"><span data-stu-id="ead85-119">The WAF policy object to delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ead85-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ead85-120">-Name</span></span>
<span data-ttu-id="ead85-121">A törlendő WAF-házirend neve.</span><span class="sxs-lookup"><span data-stu-id="ead85-121">The name of the WAF policy to delete.</span></span>

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

### <span data-ttu-id="ead85-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ead85-122">-PassThru</span></span>
<span data-ttu-id="ead85-123">Visszatérési objektum (ha meg van adva).</span><span class="sxs-lookup"><span data-stu-id="ead85-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="ead85-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ead85-124">-ResourceGroupName</span></span>
<span data-ttu-id="ead85-125">Az az erőforráscsoport, amelyhez a waf-házirend tartozik.</span><span class="sxs-lookup"><span data-stu-id="ead85-125">The resource group to which the WAF policy belongs.</span></span>

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

### <span data-ttu-id="ead85-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ead85-126">-ResourceId</span></span>
<span data-ttu-id="ead85-127">A törlendő WaF-házirend erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="ead85-127">Resource Id of the WAF policy to delete</span></span>

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

### <span data-ttu-id="ead85-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ead85-128">-Confirm</span></span>
<span data-ttu-id="ead85-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ead85-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ead85-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ead85-130">-WhatIf</span></span>
<span data-ttu-id="ead85-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ead85-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ead85-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ead85-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ead85-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ead85-133">CommonParameters</span></span>
<span data-ttu-id="ead85-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ead85-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ead85-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ead85-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ead85-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ead85-136">INPUTS</span></span>

### <span data-ttu-id="ead85-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="ead85-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="ead85-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ead85-138">System.String</span></span>

## <span data-ttu-id="ead85-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ead85-139">OUTPUTS</span></span>

### <span data-ttu-id="ead85-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ead85-140">System.Boolean</span></span>

## <span data-ttu-id="ead85-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ead85-141">NOTES</span></span>

## <span data-ttu-id="ead85-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ead85-142">RELATED LINKS</span></span>

<span data-ttu-id="ead85-143">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="ead85-143">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)</span></span>
