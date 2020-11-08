---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorWafPolicy.md
ms.openlocfilehash: ec68316ecac3921f37641b83f45b9bd922e90b46
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017748"
---
# <span data-ttu-id="747aa-101">Remove-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="747aa-101">Remove-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="747aa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="747aa-102">SYNOPSIS</span></span>
<span data-ttu-id="747aa-103">A WAF házirend eltávolítása</span><span class="sxs-lookup"><span data-stu-id="747aa-103">Remove WAF policy</span></span>

## <span data-ttu-id="747aa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="747aa-104">SYNTAX</span></span>

### <span data-ttu-id="747aa-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="747aa-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="747aa-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="747aa-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorWafPolicy -InputObject <PSPolicy> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="747aa-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="747aa-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorWafPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="747aa-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="747aa-108">DESCRIPTION</span></span>
<span data-ttu-id="747aa-109">A **Remove-AzFrontDoorWafPolicy** parancsmag a jelenlegi előfizetés alatti WAF-házirendet távolítja el.</span><span class="sxs-lookup"><span data-stu-id="747aa-109">The **Remove-AzFrontDoorWafPolicy** cmdlet removes a WAF policy under the current subscription</span></span>

## <span data-ttu-id="747aa-110">Példák</span><span class="sxs-lookup"><span data-stu-id="747aa-110">EXAMPLES</span></span>

### <span data-ttu-id="747aa-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="747aa-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName
```

<span data-ttu-id="747aa-112">Távolítsa el a $resourceGroupName $policyName nevű WAF-házirendet.</span><span class="sxs-lookup"><span data-stu-id="747aa-112">Remove the WAF policy called $policyName in $resourceGroupName.</span></span>

### <span data-ttu-id="747aa-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="747aa-113">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName | Remove-AzFrontDoorWafPolicy
```

<span data-ttu-id="747aa-114">Távolítsa el az összes WAF-házirendet a $resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="747aa-114">Remove all WAF policy in $resourceGroupName.</span></span>

## <span data-ttu-id="747aa-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="747aa-115">PARAMETERS</span></span>

### <span data-ttu-id="747aa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="747aa-116">-DefaultProfile</span></span>
<span data-ttu-id="747aa-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="747aa-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="747aa-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="747aa-118">-InputObject</span></span>
<span data-ttu-id="747aa-119">A WAF házirend-objektum.</span><span class="sxs-lookup"><span data-stu-id="747aa-119">The WAF policy object to delete.</span></span>

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

### <span data-ttu-id="747aa-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="747aa-120">-Name</span></span>
<span data-ttu-id="747aa-121">A törlendő WAF-házirend neve.</span><span class="sxs-lookup"><span data-stu-id="747aa-121">The name of the WAF policy to delete.</span></span>

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

### <span data-ttu-id="747aa-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="747aa-122">-PassThru</span></span>
<span data-ttu-id="747aa-123">Visszatérési objektum (ha meg van adva)</span><span class="sxs-lookup"><span data-stu-id="747aa-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="747aa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="747aa-124">-ResourceGroupName</span></span>
<span data-ttu-id="747aa-125">Az az erőforráscsoport, amelyhez a WAF-házirend tartozik.</span><span class="sxs-lookup"><span data-stu-id="747aa-125">The resource group to which the WAF policy belongs.</span></span>

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

### <span data-ttu-id="747aa-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="747aa-126">-ResourceId</span></span>
<span data-ttu-id="747aa-127">A törlendő WAF-házirend erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="747aa-127">Resource Id of the WAF policy to delete</span></span>

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

### <span data-ttu-id="747aa-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="747aa-128">-Confirm</span></span>
<span data-ttu-id="747aa-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="747aa-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="747aa-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="747aa-130">-WhatIf</span></span>
<span data-ttu-id="747aa-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="747aa-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="747aa-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="747aa-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="747aa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="747aa-133">CommonParameters</span></span>
<span data-ttu-id="747aa-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="747aa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="747aa-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="747aa-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="747aa-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="747aa-136">INPUTS</span></span>

### <span data-ttu-id="747aa-137">Microsoft. Azure. Command. FrontDoor. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="747aa-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="747aa-138">System. String</span><span class="sxs-lookup"><span data-stu-id="747aa-138">System.String</span></span>

## <span data-ttu-id="747aa-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="747aa-139">OUTPUTS</span></span>

### <span data-ttu-id="747aa-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="747aa-140">System.Boolean</span></span>

## <span data-ttu-id="747aa-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="747aa-141">NOTES</span></span>

## <span data-ttu-id="747aa-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="747aa-142">RELATED LINKS</span></span>

<span data-ttu-id="747aa-143">[Új – AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="747aa-143">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)</span></span>
