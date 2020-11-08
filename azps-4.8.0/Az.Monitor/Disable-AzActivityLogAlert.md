---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/disable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Disable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Disable-AzActivityLogAlert.md
ms.openlocfilehash: bdd854d3f9cc17071e17fea232b1d872b0a5fe8a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183494"
---
# <span data-ttu-id="6d5cb-101">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="6d5cb-101">Disable-AzActivityLogAlert</span></span>

## <span data-ttu-id="6d5cb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6d5cb-102">SYNOPSIS</span></span>
<span data-ttu-id="6d5cb-103">Letiltja a műveletnapló riasztását, és beállítja annak címkéit.</span><span class="sxs-lookup"><span data-stu-id="6d5cb-103">Disables an activity log alert and sets its tags.</span></span>

## <span data-ttu-id="6d5cb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6d5cb-104">SYNTAX</span></span>

### <span data-ttu-id="6d5cb-105">DisableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6d5cb-105">DisableByNameAndResourceGroup</span></span>
```
Disable-AzActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d5cb-106">DisableByInputObject</span><span class="sxs-lookup"><span data-stu-id="6d5cb-106">DisableByInputObject</span></span>
```
Disable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d5cb-107">DisableByResourceId</span><span class="sxs-lookup"><span data-stu-id="6d5cb-107">DisableByResourceId</span></span>
```
Disable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6d5cb-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6d5cb-108">DESCRIPTION</span></span>
<span data-ttu-id="6d5cb-109">A **disable-AzActivityLogAlert** parancsmag letiltja és aktivitási naplót jelenít meg, és lehetővé teszi a címkék beállítását.</span><span class="sxs-lookup"><span data-stu-id="6d5cb-109">The **Disable-AzActivityLogAlert** cmdlet disables and activity log alert and allows setting its tags.</span></span>
<span data-ttu-id="6d5cb-110">Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges javításának megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="6d5cb-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="6d5cb-111">Példák</span><span class="sxs-lookup"><span data-stu-id="6d5cb-111">EXAMPLES</span></span>

### <span data-ttu-id="6d5cb-112">1. példa: tevékenység-naplózási riasztás letiltása</span><span class="sxs-lookup"><span data-stu-id="6d5cb-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Disable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="6d5cb-113">Ez a parancs letiltja a alert1 nevű műveletnapló riasztást az erőforráscsoport default-ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="6d5cb-113">This command disables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>
<span data-ttu-id="6d5cb-114">Ez a parancs megváltoztatja a alert1 nevű műveletnapló-riasztás címkék tulajdonságát, és letiltja azt.</span><span class="sxs-lookup"><span data-stu-id="6d5cb-114">This command changes the tags property of the activity log alert called alert1 and disables it.</span></span>

### <span data-ttu-id="6d5cb-115">2. példa: tevékenység-naplózási riasztás letiltása PSActivityLogAlertResource-objektum használatával bemenetként</span><span class="sxs-lookup"><span data-stu-id="6d5cb-115">Example 2: Disable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Disable-AzActivityLogAlert -InputObject $obj
```

<span data-ttu-id="6d5cb-116">Ez a parancs letiltja a alert1 nevű műveletnapló riasztást.</span><span class="sxs-lookup"><span data-stu-id="6d5cb-116">This command disables an activity log alert called alert1.</span></span> <span data-ttu-id="6d5cb-117">Ehhez a PSActivityLogAlertResource objektumot használja bemeneti argumentumként.</span><span class="sxs-lookup"><span data-stu-id="6d5cb-117">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="6d5cb-118">3. példa: a ActivityLogAlert letiltása a ResourceId paraméterrel</span><span class="sxs-lookup"><span data-stu-id="6d5cb-118">Example 3: Disable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Disable-AzActivityLogAlert
```

<span data-ttu-id="6d5cb-119">Ez a parancs letiltja a ActivityLogAlert a ResourceId paraméterrel a pipe-ról.</span><span class="sxs-lookup"><span data-stu-id="6d5cb-119">This command disables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="6d5cb-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6d5cb-120">PARAMETERS</span></span>

### <span data-ttu-id="6d5cb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d5cb-121">-DefaultProfile</span></span>
<span data-ttu-id="6d5cb-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6d5cb-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6d5cb-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d5cb-123">-InputObject</span></span>
<span data-ttu-id="6d5cb-124">A hívás InputObject tulajdonságát állítja be a kötelező név, az erőforráscsoport neve és a választható címke tulajdonságai kinyeréséhez.</span><span class="sxs-lookup"><span data-stu-id="6d5cb-124">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tag properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: DisableByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d5cb-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6d5cb-125">-Name</span></span>
<span data-ttu-id="6d5cb-126">A műveletnapló riasztásának neve.</span><span class="sxs-lookup"><span data-stu-id="6d5cb-126">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d5cb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d5cb-127">-ResourceGroupName</span></span>
<span data-ttu-id="6d5cb-128">Annak az erőforráscsoportnek a neve, amelyben az értesítési erőforrás létezik.</span><span class="sxs-lookup"><span data-stu-id="6d5cb-128">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d5cb-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d5cb-129">-ResourceId</span></span>
<span data-ttu-id="6d5cb-130">A hívás ResourceId-címkék tulajdonságát adja meg a szükséges név, az erőforráscsoport nevének kinyeréséhez.</span><span class="sxs-lookup"><span data-stu-id="6d5cb-130">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d5cb-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6d5cb-131">-Confirm</span></span>
<span data-ttu-id="6d5cb-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6d5cb-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d5cb-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d5cb-133">-WhatIf</span></span>
<span data-ttu-id="6d5cb-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6d5cb-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6d5cb-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6d5cb-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d5cb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d5cb-136">CommonParameters</span></span>
<span data-ttu-id="6d5cb-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6d5cb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d5cb-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6d5cb-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d5cb-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d5cb-139">INPUTS</span></span>

### <span data-ttu-id="6d5cb-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6d5cb-140">System.String</span></span>

### <span data-ttu-id="6d5cb-141">Microsoft. Azure. commands. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="6d5cb-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="6d5cb-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d5cb-142">OUTPUTS</span></span>

### <span data-ttu-id="6d5cb-143">Microsoft. Azure. commands. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="6d5cb-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="6d5cb-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6d5cb-144">NOTES</span></span>

## <span data-ttu-id="6d5cb-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6d5cb-145">RELATED LINKS</span></span>

[<span data-ttu-id="6d5cb-146">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="6d5cb-146">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="6d5cb-147">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="6d5cb-147">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="6d5cb-148">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="6d5cb-148">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="6d5cb-149">Új – AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="6d5cb-149">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="6d5cb-150">Új – AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="6d5cb-150">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)

[<span data-ttu-id="6d5cb-151">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="6d5cb-151">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)
