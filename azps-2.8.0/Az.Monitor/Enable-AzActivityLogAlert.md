---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/enable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
ms.openlocfilehash: 2b5c036ee8a0667fb2b7f7e8d8fecace80d4a1ad
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100406485"
---
# <span data-ttu-id="14b61-101">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="14b61-101">Enable-AzActivityLogAlert</span></span>

## <span data-ttu-id="14b61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14b61-102">SYNOPSIS</span></span>
<span data-ttu-id="14b61-103">Engedélyezi a tevékenységnapló riasztását, és beállítja a címkéket.</span><span class="sxs-lookup"><span data-stu-id="14b61-103">Enables an activity log alert and sets its Tags.</span></span>

## <span data-ttu-id="14b61-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="14b61-104">SYNTAX</span></span>

### <span data-ttu-id="14b61-105">EnableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="14b61-105">EnableByNameAndResourceGroup</span></span>
```
Enable-AzActivityLogAlert -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14b61-106">EnableByInputObject</span><span class="sxs-lookup"><span data-stu-id="14b61-106">EnableByInputObject</span></span>
```
Enable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14b61-107">EnableByResourceId</span><span class="sxs-lookup"><span data-stu-id="14b61-107">EnableByResourceId</span></span>
```
Enable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="14b61-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="14b61-108">DESCRIPTION</span></span>
<span data-ttu-id="14b61-109">Az **Enable-AzActivityLogAlert** parancsmag lehetővé teszi a tevékenységnapló-riasztások engedélyezését és a címkék beállítását.</span><span class="sxs-lookup"><span data-stu-id="14b61-109">The **Enable-AzActivityLogAlert** cmdlet allows enabling an activity log alert and setting its tags.</span></span>
<span data-ttu-id="14b61-110">Ez a parancsmag implementálja a ShouldProcess mintát, azaz megerősítést kérhet a felhasználótól, mielőtt ténylegesen javítja az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="14b61-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="14b61-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="14b61-111">EXAMPLES</span></span>

### <span data-ttu-id="14b61-112">1. példa: Tevékenységnapló-riasztás engedélyezése</span><span class="sxs-lookup"><span data-stu-id="14b61-112">Example 1: Enable an activity log alert</span></span>
```
PS C:\>Enable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="14b61-113">Ez a parancs engedélyezi a Tevékenységnapló riasztás1 nevű riasztását a Default-ActivityLogsAlerts erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="14b61-113">This command enables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

### <span data-ttu-id="14b61-114">2. példa: Tevékenységnapló-riasztás engedélyezése a PSActivityLogAlertResource objektummal bevitelként</span><span class="sxs-lookup"><span data-stu-id="14b61-114">Example 2: Enable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Enable-AzActivityLogAlert -InputObject $obj
```

<span data-ttu-id="14b61-115">Ez a parancs egy riasztás1 nevű tevékenységnapló-riasztást tesz lehetővé.</span><span class="sxs-lookup"><span data-stu-id="14b61-115">This command enables an activity log alert called alert1.</span></span> <span data-ttu-id="14b61-116">Ehhez bemeneti argumentumként egy PSActivityLogAlertResource objektumot használ.</span><span class="sxs-lookup"><span data-stu-id="14b61-116">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="14b61-117">3. példa: A ActivityLogAlert engedélyezése az ResourceId paraméter használatával</span><span class="sxs-lookup"><span data-stu-id="14b61-117">Example 3: Enable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Enable-AzActivityLogAlert
```

<span data-ttu-id="14b61-118">Ez a parancs engedélyezi a ActivityLogAlert paramétert a folyamat ResourceId paraméterével.</span><span class="sxs-lookup"><span data-stu-id="14b61-118">This command enables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="14b61-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14b61-119">PARAMETERS</span></span>

### <span data-ttu-id="14b61-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14b61-120">-DefaultProfile</span></span>
<span data-ttu-id="14b61-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="14b61-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14b61-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14b61-122">-InputObject</span></span>
<span data-ttu-id="14b61-123">Beállítja a hívás InputObject tags tulajdonságát, hogy kinyerje a szükséges nevet, az erőforráscsoport nevét és a választható címketulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="14b61-123">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tags properties.</span></span>

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

### <span data-ttu-id="14b61-124">-Name</span><span class="sxs-lookup"><span data-stu-id="14b61-124">-Name</span></span>
<span data-ttu-id="14b61-125">A tevékenységnapló-riasztás neve.</span><span class="sxs-lookup"><span data-stu-id="14b61-125">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="14b61-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14b61-126">-ResourceGroupName</span></span>
<span data-ttu-id="14b61-127">Annak az erőforráscsoportnak a neve, amelyben a riasztási erőforrás fog létezni.</span><span class="sxs-lookup"><span data-stu-id="14b61-127">The name of the resource group where the alert resource is going to exist.</span></span>

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

### <span data-ttu-id="14b61-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14b61-128">-ResourceId</span></span>
<span data-ttu-id="14b61-129">Beállítja a hívás ResourceId tags tulajdonságát a szükséges név, az erőforráscsoport nevének tulajdonságainak kibontása érdekében.</span><span class="sxs-lookup"><span data-stu-id="14b61-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="14b61-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14b61-130">-Confirm</span></span>
<span data-ttu-id="14b61-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="14b61-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14b61-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14b61-132">-WhatIf</span></span>
<span data-ttu-id="14b61-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="14b61-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="14b61-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="14b61-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14b61-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14b61-135">CommonParameters</span></span>
<span data-ttu-id="14b61-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14b61-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14b61-137">További információt a [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14b61-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14b61-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="14b61-138">INPUTS</span></span>

### <span data-ttu-id="14b61-139">System.String</span><span class="sxs-lookup"><span data-stu-id="14b61-139">System.String</span></span>

### <span data-ttu-id="14b61-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="14b61-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="14b61-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="14b61-141">OUTPUTS</span></span>

### <span data-ttu-id="14b61-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="14b61-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="14b61-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="14b61-143">NOTES</span></span>

## <span data-ttu-id="14b61-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="14b61-144">RELATED LINKS</span></span>

[<span data-ttu-id="14b61-145">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="14b61-145">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="14b61-146">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="14b61-146">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="14b61-147">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="14b61-147">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="14b61-148">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="14b61-148">New-AzActionGroup</span></span>](./New-AzActionGroup.md)



[<span data-ttu-id="14b61-149">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="14b61-149">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)
