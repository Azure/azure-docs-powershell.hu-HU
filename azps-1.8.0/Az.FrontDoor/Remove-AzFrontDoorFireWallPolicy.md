---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorFireWallPolicy.md
ms.openlocfilehash: f081d403a47f457c48320238436d72ca4ebd15fe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836122"
---
# <span data-ttu-id="d57a7-101">Remove-AzFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="d57a7-101">Remove-AzFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="d57a7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d57a7-102">SYNOPSIS</span></span>
<span data-ttu-id="d57a7-103">A WAF házirend eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d57a7-103">Remove WAF policy</span></span>

## <span data-ttu-id="d57a7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d57a7-104">SYNTAX</span></span>

### <span data-ttu-id="d57a7-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d57a7-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d57a7-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d57a7-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorFireWallPolicy -InputObject <PSPolicy> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d57a7-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d57a7-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorFireWallPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d57a7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d57a7-108">DESCRIPTION</span></span>
<span data-ttu-id="d57a7-109">A **Remove-AzFrontDoorFireWallPolicy** parancsmag a jelenlegi előfizetés alatti WAF-házirendet távolítja el.</span><span class="sxs-lookup"><span data-stu-id="d57a7-109">The **Remove-AzFrontDoorFireWallPolicy** cmdlet removes a WAF policy under the current subscription</span></span>

## <span data-ttu-id="d57a7-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d57a7-110">EXAMPLES</span></span>

### <span data-ttu-id="d57a7-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d57a7-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorFireWallPolicy -Name $policyName -ResourceGroupName $resourceGroupName
```

<span data-ttu-id="d57a7-112">Távolítsa el a $resourceGroupName $policyName nevű WAF-házirendet.</span><span class="sxs-lookup"><span data-stu-id="d57a7-112">Remove the WAF policy called $policyName in $resourceGroupName.</span></span>

### <span data-ttu-id="d57a7-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="d57a7-113">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorFireWallPolicy -ResourceGroupName $resourceGroupName | Remove-AzFrontDoorFireWallPolicy
```

<span data-ttu-id="d57a7-114">Távolítsa el az összes WAF-házirendet a $resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="d57a7-114">Remove all WAF policy in $resourceGroupName.</span></span>

## <span data-ttu-id="d57a7-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d57a7-115">PARAMETERS</span></span>

### <span data-ttu-id="d57a7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d57a7-116">-DefaultProfile</span></span>
<span data-ttu-id="d57a7-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d57a7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d57a7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d57a7-118">-InputObject</span></span>
<span data-ttu-id="d57a7-119">A WAF házirend-objektum.</span><span class="sxs-lookup"><span data-stu-id="d57a7-119">The WAF policy object to delete.</span></span>

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

### <span data-ttu-id="d57a7-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d57a7-120">-Name</span></span>
<span data-ttu-id="d57a7-121">A törlendő WAF-házirend neve.</span><span class="sxs-lookup"><span data-stu-id="d57a7-121">The name of the WAF policy to delete.</span></span>

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

### <span data-ttu-id="d57a7-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d57a7-122">-PassThru</span></span>
<span data-ttu-id="d57a7-123">Visszatérési objektum (ha meg van adva)</span><span class="sxs-lookup"><span data-stu-id="d57a7-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="d57a7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d57a7-124">-ResourceGroupName</span></span>
<span data-ttu-id="d57a7-125">Az az erőforráscsoport, amelyhez a WAF-házirend tartozik.</span><span class="sxs-lookup"><span data-stu-id="d57a7-125">The resource group to which the WAF policy belongs.</span></span>

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

### <span data-ttu-id="d57a7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d57a7-126">-ResourceId</span></span>
<span data-ttu-id="d57a7-127">A törlendő WAF-házirend erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="d57a7-127">Resource Id of the WAF policy to delete</span></span>

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

### <span data-ttu-id="d57a7-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d57a7-128">-Confirm</span></span>
<span data-ttu-id="d57a7-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d57a7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d57a7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d57a7-130">-WhatIf</span></span>
<span data-ttu-id="d57a7-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d57a7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d57a7-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d57a7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d57a7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d57a7-133">CommonParameters</span></span>
<span data-ttu-id="d57a7-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d57a7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d57a7-135">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d57a7-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d57a7-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d57a7-136">INPUTS</span></span>

### <span data-ttu-id="d57a7-137">Microsoft. Azure. Command. FrontDoor. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="d57a7-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="d57a7-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d57a7-138">System.String</span></span>

## <span data-ttu-id="d57a7-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d57a7-139">OUTPUTS</span></span>

### <span data-ttu-id="d57a7-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d57a7-140">System.Boolean</span></span>

## <span data-ttu-id="d57a7-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d57a7-141">NOTES</span></span>

## <span data-ttu-id="d57a7-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d57a7-142">RELATED LINKS</span></span>

<span data-ttu-id="d57a7-143">[Új – AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
 [Get-AzFrontDoorFireWallPolicy](./Get-AzFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="d57a7-143">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Get-AzFrontDoorFireWallPolicy](./Get-AzFrontDoorFireWallPolicy.md)</span></span>
