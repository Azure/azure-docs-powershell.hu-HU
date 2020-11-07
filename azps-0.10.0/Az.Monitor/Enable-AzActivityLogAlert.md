---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/enable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
ms.openlocfilehash: e2b09005714021bc8b428b93214f30a16a279ce8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842070"
---
# <span data-ttu-id="6a300-101">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="6a300-101">Enable-AzActivityLogAlert</span></span>

## <span data-ttu-id="6a300-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6a300-102">SYNOPSIS</span></span>
<span data-ttu-id="6a300-103">Engedélyezi a műveletnapló riasztását, és beállítja annak címkéit.</span><span class="sxs-lookup"><span data-stu-id="6a300-103">Enables an activity log alert and sets its Tags.</span></span>

## <span data-ttu-id="6a300-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6a300-104">SYNTAX</span></span>

### <span data-ttu-id="6a300-105">EnableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6a300-105">EnableByNameAndResourceGroup</span></span>
```
Enable-AzActivityLogAlert -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a300-106">EnableByInputObject</span><span class="sxs-lookup"><span data-stu-id="6a300-106">EnableByInputObject</span></span>
```
Enable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a300-107">EnableByResourceId</span><span class="sxs-lookup"><span data-stu-id="6a300-107">EnableByResourceId</span></span>
```
Enable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6a300-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6a300-108">DESCRIPTION</span></span>
<span data-ttu-id="6a300-109">Az **enable-AzActivityLogAlert** parancsmag lehetővé teszi a műveletnapló riasztását és a címkék beállítását.</span><span class="sxs-lookup"><span data-stu-id="6a300-109">The **Enable-AzActivityLogAlert** cmdlet allows enabling an activity log alert and setting its tags.</span></span>
<span data-ttu-id="6a300-110">Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges javításának megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="6a300-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="6a300-111">Példák</span><span class="sxs-lookup"><span data-stu-id="6a300-111">EXAMPLES</span></span>

### <span data-ttu-id="6a300-112">1. példa: tevékenység-naplózási riasztás engedélyezése</span><span class="sxs-lookup"><span data-stu-id="6a300-112">Example 1: Enable an activity log alert</span></span>
```
PS C:\>Enable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="6a300-113">Ez a parancs engedélyezi a alert1 nevű műveletnapló riasztást az erőforráscsoport alapértelmezett ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="6a300-113">This command enables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

### <span data-ttu-id="6a300-114">2. példa: tevékenység-naplózási riasztás engedélyezése PSActivityLogAlertResource objektummal bemenetként</span><span class="sxs-lookup"><span data-stu-id="6a300-114">Example 2: Enable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Enable-AzActivityLogAlert -InputObject $obj
```

<span data-ttu-id="6a300-115">Ez a parancs lehetővé teszi a alert1 nevű műveletnapló riasztást.</span><span class="sxs-lookup"><span data-stu-id="6a300-115">This command enables an activity log alert called alert1.</span></span> <span data-ttu-id="6a300-116">Ehhez a PSActivityLogAlertResource objektumot használja bemeneti argumentumként.</span><span class="sxs-lookup"><span data-stu-id="6a300-116">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="6a300-117">3. példa: a ActivityLogAlert engedélyezése a ResourceId paraméterrel</span><span class="sxs-lookup"><span data-stu-id="6a300-117">Example 3: Enable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Enable-AzActivityLogAlert
```

<span data-ttu-id="6a300-118">Ez a parancs engedélyezi az ActivityLogAlert a ResourceId paraméterrel a csőben.</span><span class="sxs-lookup"><span data-stu-id="6a300-118">This command enables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="6a300-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6a300-119">PARAMETERS</span></span>

### <span data-ttu-id="6a300-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a300-120">-DefaultProfile</span></span>
<span data-ttu-id="6a300-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6a300-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6a300-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a300-122">-InputObject</span></span>
<span data-ttu-id="6a300-123">A hívás InputObject tulajdonságát állítja be a kötelező név, az erőforráscsoport neve és a választható címkék tulajdonságai kinyeréséhez.</span><span class="sxs-lookup"><span data-stu-id="6a300-123">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tags properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: EnableByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a300-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6a300-124">-Name</span></span>
<span data-ttu-id="6a300-125">A műveletnapló riasztásának neve.</span><span class="sxs-lookup"><span data-stu-id="6a300-125">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a300-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a300-126">-ResourceGroupName</span></span>
<span data-ttu-id="6a300-127">Annak az erőforráscsoportnek a neve, amelyben az értesítési erőforrás létezik.</span><span class="sxs-lookup"><span data-stu-id="6a300-127">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a300-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a300-128">-ResourceId</span></span>
<span data-ttu-id="6a300-129">A hívás ResourceId-címkék tulajdonságát adja meg a szükséges név, az erőforráscsoport nevének kinyeréséhez.</span><span class="sxs-lookup"><span data-stu-id="6a300-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a300-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6a300-130">-Confirm</span></span>
<span data-ttu-id="6a300-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6a300-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a300-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a300-132">-WhatIf</span></span>
<span data-ttu-id="6a300-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6a300-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6a300-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6a300-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a300-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a300-135">CommonParameters</span></span>
<span data-ttu-id="6a300-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6a300-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a300-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6a300-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a300-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a300-138">INPUTS</span></span>

### <span data-ttu-id="6a300-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6a300-139">System.String</span></span>

### <span data-ttu-id="6a300-140">Microsoft. Azure. commands. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="6a300-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="6a300-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a300-141">OUTPUTS</span></span>

### <span data-ttu-id="6a300-142">Microsoft. Azure. commands. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="6a300-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="6a300-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6a300-143">NOTES</span></span>

## <span data-ttu-id="6a300-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a300-144">RELATED LINKS</span></span>

[<span data-ttu-id="6a300-145">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="6a300-145">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="6a300-146">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="6a300-146">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="6a300-147">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="6a300-147">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="6a300-148">Új – AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="6a300-148">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="6a300-149">Új – AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="6a300-149">New-AzActivityLogAlertCondition</span></span>](./Get-AzActivityLogAlertCondition.md)

[<span data-ttu-id="6a300-150">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="6a300-150">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)
