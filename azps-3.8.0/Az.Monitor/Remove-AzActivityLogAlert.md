---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActivityLogAlert.md
ms.openlocfilehash: 5a0841a3cb2cd01ebb7f44b41e89d0b30404dfd0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94002835"
---
# <span data-ttu-id="a20a2-101">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a20a2-101">Remove-AzActivityLogAlert</span></span>

## <span data-ttu-id="a20a2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a20a2-102">SYNOPSIS</span></span>
<span data-ttu-id="a20a2-103">Tevékenység-naplózási riasztás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="a20a2-103">Removes an activity log alert.</span></span>

## <span data-ttu-id="a20a2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a20a2-104">SYNTAX</span></span>

### <span data-ttu-id="a20a2-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a20a2-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzActivityLogAlert -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a20a2-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="a20a2-106">RemoveByInputObject</span></span>
```
Remove-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a20a2-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="a20a2-107">RemoveByResourceId</span></span>
```
Remove-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a20a2-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a20a2-108">DESCRIPTION</span></span>
<span data-ttu-id="a20a2-109">Az **Eltávolítás – AzActivityLogAlert** parancsmag eltávolítja a műveletnapló riasztását.</span><span class="sxs-lookup"><span data-stu-id="a20a2-109">The **Remove-AzActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="a20a2-110">Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges javításának megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="a20a2-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>
<span data-ttu-id="a20a2-111">Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges létrehozása, módosítása vagy eltávolítása előtt.</span><span class="sxs-lookup"><span data-stu-id="a20a2-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="a20a2-112">Példák</span><span class="sxs-lookup"><span data-stu-id="a20a2-112">EXAMPLES</span></span>

### <span data-ttu-id="a20a2-113">1. példa: tevékenység-naplózási riasztás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a20a2-113">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="a20a2-114">Tevékenység-naplózási riasztás eltávolítása a név és az erőforrás csoport nevében bemenetként.</span><span class="sxs-lookup"><span data-stu-id="a20a2-114">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="a20a2-115">2. példa: tevékenység-naplózási riasztás eltávolítása PSActivityLogAlertResource adatbevitelsel</span><span class="sxs-lookup"><span data-stu-id="a20a2-115">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="a20a2-116">Tevékenység-naplózási riasztás eltávolítása PSActivityLogAlertResource adatbevitel útján</span><span class="sxs-lookup"><span data-stu-id="a20a2-116">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="a20a2-117">3. példa: a ActivityLogAlert eltávolítása a ResourceId paraméterrel</span><span class="sxs-lookup"><span data-stu-id="a20a2-117">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Remove-AzActivityLogAlert
```

<span data-ttu-id="a20a2-118">Ez a parancs eltávolítja a ActivityLogAlert a ResourceId paraméterrel a pipe-ról.</span><span class="sxs-lookup"><span data-stu-id="a20a2-118">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="a20a2-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a20a2-119">PARAMETERS</span></span>

### <span data-ttu-id="a20a2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a20a2-120">-DefaultProfile</span></span>
<span data-ttu-id="a20a2-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a20a2-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a20a2-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a20a2-122">-InputObject</span></span>
<span data-ttu-id="a20a2-123">A hívás InputObject (címkék) tulajdonságát adja meg a szükséges név és az erőforrás csoport nevének kinyeréséhez.</span><span class="sxs-lookup"><span data-stu-id="a20a2-123">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

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

### <span data-ttu-id="a20a2-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a20a2-124">-Name</span></span>
<span data-ttu-id="a20a2-125">A műveletnapló riasztásának neve.</span><span class="sxs-lookup"><span data-stu-id="a20a2-125">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="a20a2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a20a2-126">-ResourceGroupName</span></span>
<span data-ttu-id="a20a2-127">Annak az erőforráscsoportnek a neve, amelyben az értesítési erőforrás létezik.</span><span class="sxs-lookup"><span data-stu-id="a20a2-127">The name of the resource group where the alert resource exists.</span></span>

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

### <span data-ttu-id="a20a2-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a20a2-128">-ResourceId</span></span>
<span data-ttu-id="a20a2-129">A hívás ResourceId-címkék tulajdonságát adja meg a szükséges név, az erőforráscsoport nevének kinyeréséhez.</span><span class="sxs-lookup"><span data-stu-id="a20a2-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="a20a2-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a20a2-130">-Confirm</span></span>
<span data-ttu-id="a20a2-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a20a2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a20a2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a20a2-132">-WhatIf</span></span>
<span data-ttu-id="a20a2-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a20a2-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a20a2-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a20a2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a20a2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a20a2-135">CommonParameters</span></span>
<span data-ttu-id="a20a2-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a20a2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a20a2-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a20a2-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a20a2-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a20a2-138">INPUTS</span></span>

### <span data-ttu-id="a20a2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a20a2-139">System.String</span></span>

### <span data-ttu-id="a20a2-140">Microsoft. Azure. commands. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="a20a2-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="a20a2-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a20a2-141">OUTPUTS</span></span>

### <span data-ttu-id="a20a2-142">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a20a2-142">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="a20a2-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a20a2-143">NOTES</span></span>

## <span data-ttu-id="a20a2-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a20a2-144">RELATED LINKS</span></span>

[<span data-ttu-id="a20a2-145">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a20a2-145">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="a20a2-146">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a20a2-146">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="a20a2-147">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a20a2-147">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="a20a2-148">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a20a2-148">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="a20a2-149">Új – AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="a20a2-149">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="a20a2-150">Új – AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="a20a2-150">New-AzActivityLogAlertCondition</span></span>](./Get-AzActivityLogAlertCondition.md)

