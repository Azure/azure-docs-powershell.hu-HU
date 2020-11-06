---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/remove-azurermfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoorFireWallPolicy.md
ms.openlocfilehash: 4dda510402b9395db24507f22d90da0f1fb6a44c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491918"
---
# <span data-ttu-id="e7a0d-101">Remove-AzureRmFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="e7a0d-101">Remove-AzureRmFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="e7a0d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e7a0d-102">SYNOPSIS</span></span>
<span data-ttu-id="e7a0d-103">A WAF házirend eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e7a0d-103">Remove WAF policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7a0d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e7a0d-104">SYNTAX</span></span>

### <span data-ttu-id="e7a0d-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e7a0d-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzureRmFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7a0d-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7a0d-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmFrontDoorFireWallPolicy -InputObject <PSPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7a0d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7a0d-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmFrontDoorFireWallPolicy -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7a0d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e7a0d-108">DESCRIPTION</span></span>
<span data-ttu-id="e7a0d-109">A **Remove-AzureRmFrontDoor** parancsmag a jelenlegi előfizetés alatti WAF-házirendet távolítja el.</span><span class="sxs-lookup"><span data-stu-id="e7a0d-109">The **Remove-AzureRmFrontDoor** cmdlet removes a WAF policy under the current subscription</span></span>

## <span data-ttu-id="e7a0d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e7a0d-110">EXAMPLES</span></span>

### <span data-ttu-id="e7a0d-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e7a0d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmFrontDoorFireWallPolicy -Name $name -ResourceGroupName $resourceGroup
```

<span data-ttu-id="e7a0d-112">Távolítsa el a $resourceGroup $name nevű WAF-házirendet.</span><span class="sxs-lookup"><span data-stu-id="e7a0d-112">Remove the WAF policy called $name in $resourceGroup.</span></span>

### <span data-ttu-id="e7a0d-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="e7a0d-113">Example 2</span></span>
```powershell
PS C:\> Get--AzureRmFrontDoorFireWallPolicy -ResourceGroupName $resourceGroup | Remove-AzureRmFrontDoorFireWallPolicy
```

<span data-ttu-id="e7a0d-114">Távolítsa el az összes WAF-házirendet a $resourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e7a0d-114">Remove all WAF policy in $resourceGroup.</span></span>

## <span data-ttu-id="e7a0d-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e7a0d-115">PARAMETERS</span></span>

### <span data-ttu-id="e7a0d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7a0d-116">-DefaultProfile</span></span>
<span data-ttu-id="e7a0d-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e7a0d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7a0d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7a0d-118">-InputObject</span></span>
<span data-ttu-id="e7a0d-119">A WAF házirend-objektum.</span><span class="sxs-lookup"><span data-stu-id="e7a0d-119">The WAF policy object to delete.</span></span>

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

### <span data-ttu-id="e7a0d-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e7a0d-120">-Name</span></span>
<span data-ttu-id="e7a0d-121">A törlendő WAF-házirend neve.</span><span class="sxs-lookup"><span data-stu-id="e7a0d-121">The name of the WAF policy to delete.</span></span>

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

### <span data-ttu-id="e7a0d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7a0d-122">-PassThru</span></span>
<span data-ttu-id="e7a0d-123">Visszatérési objektum (ha meg van adva)</span><span class="sxs-lookup"><span data-stu-id="e7a0d-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="e7a0d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7a0d-124">-ResourceGroupName</span></span>
<span data-ttu-id="e7a0d-125">Az az erőforráscsoport, amelyhez a WAF-házirend tartozik.</span><span class="sxs-lookup"><span data-stu-id="e7a0d-125">The resource group to which the WAF policy belongs.</span></span>

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

### <span data-ttu-id="e7a0d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7a0d-126">-ResourceId</span></span>
<span data-ttu-id="e7a0d-127">A törlendő WAF-házirend erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="e7a0d-127">Resource Id of the WAF policy to delete</span></span>

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

### <span data-ttu-id="e7a0d-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e7a0d-128">-Confirm</span></span>
<span data-ttu-id="e7a0d-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e7a0d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7a0d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7a0d-130">-WhatIf</span></span>
<span data-ttu-id="e7a0d-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e7a0d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7a0d-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e7a0d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7a0d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7a0d-133">CommonParameters</span></span>
<span data-ttu-id="e7a0d-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e7a0d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7a0d-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7a0d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7a0d-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7a0d-136">INPUTS</span></span>

### <span data-ttu-id="e7a0d-137">Microsoft. Azure. Command. FrontDoor. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="e7a0d-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="e7a0d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e7a0d-138">System.String</span></span>

### <span data-ttu-id="e7a0d-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e7a0d-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e7a0d-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7a0d-140">OUTPUTS</span></span>

### <span data-ttu-id="e7a0d-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e7a0d-141">System.Boolean</span></span>

## <span data-ttu-id="e7a0d-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e7a0d-142">NOTES</span></span>

## <span data-ttu-id="e7a0d-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e7a0d-143">RELATED LINKS</span></span>

<span data-ttu-id="e7a0d-144">[Új – AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="e7a0d-144">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md)</span></span>
