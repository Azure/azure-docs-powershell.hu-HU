---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActivityLogAlert.md
ms.openlocfilehash: a69297afe49bb7cda0abc95cf97b371e04cac0ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924818"
---
# <span data-ttu-id="16d03-101">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="16d03-101">Remove-AzActivityLogAlert</span></span>

## <span data-ttu-id="16d03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16d03-102">SYNOPSIS</span></span>
<span data-ttu-id="16d03-103">Eltávolít egy tevékenységnapló-riasztást.</span><span class="sxs-lookup"><span data-stu-id="16d03-103">Removes an activity log alert.</span></span>

## <span data-ttu-id="16d03-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="16d03-104">SYNTAX</span></span>

### <span data-ttu-id="16d03-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="16d03-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzActivityLogAlert -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16d03-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="16d03-106">RemoveByInputObject</span></span>
```
Remove-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16d03-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="16d03-107">RemoveByResourceId</span></span>
```
Remove-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="16d03-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="16d03-108">DESCRIPTION</span></span>
<span data-ttu-id="16d03-109">A **Remove-AzActivityLogAlert** parancsmag eltávolítja a tevékenységnapló-riasztást.</span><span class="sxs-lookup"><span data-stu-id="16d03-109">The **Remove-AzActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="16d03-110">Ez a parancsmag implementálja a ShouldProcess mintát, azaz megerősítést kérhet a felhasználótól, mielőtt ténylegesen javítja az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="16d03-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>
<span data-ttu-id="16d03-111">Ez a parancsmag implementálja a ShouldProcess mintát, azaz megerősítést kérhet a felhasználótól, mielőtt ténylegesen létrehozza, módosítja vagy eltávolítja az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="16d03-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="16d03-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="16d03-112">EXAMPLES</span></span>

### <span data-ttu-id="16d03-113">1. példa: Tevékenységnapló-riasztás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="16d03-113">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="16d03-114">Eltávolít egy tevékenységnapló-riasztást, amely bemenetként a név és az erőforráscsoport nevét használja.</span><span class="sxs-lookup"><span data-stu-id="16d03-114">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="16d03-115">2. példa: Tevékenységnapló-riasztás eltávolítása a PSActivityLogAlertResource használatával bemenetként</span><span class="sxs-lookup"><span data-stu-id="16d03-115">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="16d03-116">Tevékenységnapló-riasztás eltávolítása a PSActivityLogAlertResource beviteli mező használatával.</span><span class="sxs-lookup"><span data-stu-id="16d03-116">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="16d03-117">3. példa: A ActivityLogAlert eltávolítása a ResourceId paraméterrel</span><span class="sxs-lookup"><span data-stu-id="16d03-117">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Remove-AzActivityLogAlert
```

<span data-ttu-id="16d03-118">Ez a parancs eltávolítja a ActivityLogAlert paramétert az Erőforrásazonosító paraméter használatával a pipe-ból.</span><span class="sxs-lookup"><span data-stu-id="16d03-118">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="16d03-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16d03-119">PARAMETERS</span></span>

### <span data-ttu-id="16d03-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16d03-120">-DefaultProfile</span></span>
<span data-ttu-id="16d03-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="16d03-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16d03-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16d03-122">-InputObject</span></span>
<span data-ttu-id="16d03-123">Beállítja a hívás InputObject tags tulajdonságát a szükséges név és az erőforráscsoport nevének tulajdonságainak kibontása érdekében.</span><span class="sxs-lookup"><span data-stu-id="16d03-123">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16d03-124">-Name</span><span class="sxs-lookup"><span data-stu-id="16d03-124">-Name</span></span>
<span data-ttu-id="16d03-125">A tevékenységnapló-riasztás neve.</span><span class="sxs-lookup"><span data-stu-id="16d03-125">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16d03-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16d03-126">-ResourceGroupName</span></span>
<span data-ttu-id="16d03-127">Annak az erőforráscsoportnak a neve, amelyben a riasztási erőforrás létezik.</span><span class="sxs-lookup"><span data-stu-id="16d03-127">The name of the resource group where the alert resource exists.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16d03-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16d03-128">-ResourceId</span></span>
<span data-ttu-id="16d03-129">Beállítja a hívás ResourceId tags tulajdonságát a szükséges név, az erőforráscsoport nevének tulajdonságainak kibontása érdekében.</span><span class="sxs-lookup"><span data-stu-id="16d03-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16d03-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="16d03-130">-Confirm</span></span>
<span data-ttu-id="16d03-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="16d03-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16d03-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16d03-132">-WhatIf</span></span>
<span data-ttu-id="16d03-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="16d03-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="16d03-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="16d03-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16d03-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16d03-135">CommonParameters</span></span>
<span data-ttu-id="16d03-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16d03-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16d03-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16d03-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16d03-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="16d03-138">INPUTS</span></span>

### <span data-ttu-id="16d03-139">System.String</span><span class="sxs-lookup"><span data-stu-id="16d03-139">System.String</span></span>

### <span data-ttu-id="16d03-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="16d03-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="16d03-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="16d03-141">OUTPUTS</span></span>

### <span data-ttu-id="16d03-142">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="16d03-142">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="16d03-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="16d03-143">NOTES</span></span>

## <span data-ttu-id="16d03-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="16d03-144">RELATED LINKS</span></span>

[<span data-ttu-id="16d03-145">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="16d03-145">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="16d03-146">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="16d03-146">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="16d03-147">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="16d03-147">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="16d03-148">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="16d03-148">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="16d03-149">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="16d03-149">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="16d03-150">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="16d03-150">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)

