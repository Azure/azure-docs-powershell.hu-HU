---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActivityLogAlert.md
ms.openlocfilehash: aff7540a11df1da5922c9bf2f9817309c3157365
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195620"
---
# <span data-ttu-id="aacae-101">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="aacae-101">Remove-AzActivityLogAlert</span></span>

## <span data-ttu-id="aacae-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aacae-102">SYNOPSIS</span></span>
<span data-ttu-id="aacae-103">Tevékenység-naplózási riasztás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="aacae-103">Removes an activity log alert.</span></span>

## <span data-ttu-id="aacae-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aacae-104">SYNTAX</span></span>

### <span data-ttu-id="aacae-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="aacae-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzActivityLogAlert -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aacae-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="aacae-106">RemoveByInputObject</span></span>
```
Remove-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aacae-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="aacae-107">RemoveByResourceId</span></span>
```
Remove-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aacae-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="aacae-108">DESCRIPTION</span></span>
<span data-ttu-id="aacae-109">Az **Eltávolítás – AzActivityLogAlert** parancsmag eltávolítja a műveletnapló riasztását.</span><span class="sxs-lookup"><span data-stu-id="aacae-109">The **Remove-AzActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="aacae-110">Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges javításának megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="aacae-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>
<span data-ttu-id="aacae-111">Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges létrehozása, módosítása vagy eltávolítása előtt.</span><span class="sxs-lookup"><span data-stu-id="aacae-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="aacae-112">Példák</span><span class="sxs-lookup"><span data-stu-id="aacae-112">EXAMPLES</span></span>

### <span data-ttu-id="aacae-113">1. példa: tevékenység-naplózási riasztás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="aacae-113">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="aacae-114">Tevékenység-naplózási riasztás eltávolítása a név és az erőforrás csoport nevében bemenetként.</span><span class="sxs-lookup"><span data-stu-id="aacae-114">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="aacae-115">2. példa: tevékenység-naplózási riasztás eltávolítása PSActivityLogAlertResource adatbevitelsel</span><span class="sxs-lookup"><span data-stu-id="aacae-115">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="aacae-116">Tevékenység-naplózási riasztás eltávolítása PSActivityLogAlertResource adatbevitel útján</span><span class="sxs-lookup"><span data-stu-id="aacae-116">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="aacae-117">3. példa: a ActivityLogAlert eltávolítása a ResourceId paraméterrel</span><span class="sxs-lookup"><span data-stu-id="aacae-117">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Remove-AzActivityLogAlert
```

<span data-ttu-id="aacae-118">Ez a parancs eltávolítja a ActivityLogAlert a ResourceId paraméterrel a pipe-ról.</span><span class="sxs-lookup"><span data-stu-id="aacae-118">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="aacae-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aacae-119">PARAMETERS</span></span>

### <span data-ttu-id="aacae-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aacae-120">-DefaultProfile</span></span>
<span data-ttu-id="aacae-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="aacae-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aacae-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aacae-122">-InputObject</span></span>
<span data-ttu-id="aacae-123">A hívás InputObject (címkék) tulajdonságát adja meg a szükséges név és az erőforrás csoport nevének kinyeréséhez.</span><span class="sxs-lookup"><span data-stu-id="aacae-123">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

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

### <span data-ttu-id="aacae-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="aacae-124">-Name</span></span>
<span data-ttu-id="aacae-125">A műveletnapló riasztásának neve.</span><span class="sxs-lookup"><span data-stu-id="aacae-125">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="aacae-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aacae-126">-ResourceGroupName</span></span>
<span data-ttu-id="aacae-127">Annak az erőforráscsoportnek a neve, amelyben az értesítési erőforrás létezik.</span><span class="sxs-lookup"><span data-stu-id="aacae-127">The name of the resource group where the alert resource exists.</span></span>

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

### <span data-ttu-id="aacae-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aacae-128">-ResourceId</span></span>
<span data-ttu-id="aacae-129">A hívás ResourceId-címkék tulajdonságát adja meg a szükséges név, az erőforráscsoport nevének kinyeréséhez.</span><span class="sxs-lookup"><span data-stu-id="aacae-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="aacae-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="aacae-130">-Confirm</span></span>
<span data-ttu-id="aacae-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="aacae-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aacae-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aacae-132">-WhatIf</span></span>
<span data-ttu-id="aacae-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="aacae-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aacae-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aacae-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aacae-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aacae-135">CommonParameters</span></span>
<span data-ttu-id="aacae-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aacae-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aacae-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="aacae-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aacae-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aacae-138">INPUTS</span></span>

### <span data-ttu-id="aacae-139">System. String</span><span class="sxs-lookup"><span data-stu-id="aacae-139">System.String</span></span>

### <span data-ttu-id="aacae-140">Microsoft. Azure. commands. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="aacae-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="aacae-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aacae-141">OUTPUTS</span></span>

### <span data-ttu-id="aacae-142">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="aacae-142">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="aacae-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aacae-143">NOTES</span></span>

## <span data-ttu-id="aacae-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aacae-144">RELATED LINKS</span></span>

[<span data-ttu-id="aacae-145">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="aacae-145">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="aacae-146">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="aacae-146">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="aacae-147">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="aacae-147">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="aacae-148">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="aacae-148">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="aacae-149">Új – AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="aacae-149">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="aacae-150">Új – AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="aacae-150">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)
