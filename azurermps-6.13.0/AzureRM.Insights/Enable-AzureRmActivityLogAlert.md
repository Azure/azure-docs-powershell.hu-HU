---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/enable-azurermactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Enable-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Enable-AzureRmActivityLogAlert.md
ms.openlocfilehash: abfa4fa78ecc43921ce779b73575f68654759fe4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497460"
---
# <span data-ttu-id="3470e-101">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="3470e-101">Enable-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="3470e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3470e-102">SYNOPSIS</span></span>
<span data-ttu-id="3470e-103">Engedélyezi a műveletnapló riasztását, és beállítja annak címkéit.</span><span class="sxs-lookup"><span data-stu-id="3470e-103">Enables an activity log alert and sets its Tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3470e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3470e-104">SYNTAX</span></span>

### <span data-ttu-id="3470e-105">EnableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3470e-105">EnableByNameAndResourceGroup</span></span>
```
Enable-AzureRmActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3470e-106">EnableByInputObject</span><span class="sxs-lookup"><span data-stu-id="3470e-106">EnableByInputObject</span></span>
```
Enable-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3470e-107">EnableByResourceId</span><span class="sxs-lookup"><span data-stu-id="3470e-107">EnableByResourceId</span></span>
```
Enable-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3470e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3470e-108">DESCRIPTION</span></span>
<span data-ttu-id="3470e-109">Az **enable-AzureRmActivityLogAlert** parancsmag lehetővé teszi a műveletnapló riasztását és a címkék beállítását.</span><span class="sxs-lookup"><span data-stu-id="3470e-109">The **Enable-AzureRmActivityLogAlert** cmdlet allows enabling an activity log alert and setting its tags.</span></span>
<span data-ttu-id="3470e-110">Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges javításának megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="3470e-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="3470e-111">Példák</span><span class="sxs-lookup"><span data-stu-id="3470e-111">EXAMPLES</span></span>

### <span data-ttu-id="3470e-112">1. példa: tevékenység-naplózási riasztás letiltása</span><span class="sxs-lookup"><span data-stu-id="3470e-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Enable-AzureRmActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="3470e-113">Ez a parancs engedélyezi a alert1 nevű műveletnapló riasztást az erőforráscsoport alapértelmezett ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="3470e-113">This command enables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

### <span data-ttu-id="3470e-114">2. példa: tevékenység-naplózási riasztás engedélyezése PSActivityLogAlertResource objektummal bemenetként</span><span class="sxs-lookup"><span data-stu-id="3470e-114">Example 2: Enable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Enable-AzureRmActivityLogAlert -InputObject $obj
```

<span data-ttu-id="3470e-115">Ez a parancs lehetővé teszi a alert1 nevű műveletnapló riasztást.</span><span class="sxs-lookup"><span data-stu-id="3470e-115">This command enables an activity log alert called alert1.</span></span> <span data-ttu-id="3470e-116">Ehhez a PSActivityLogAlertResource objektumot használja bemeneti argumentumként.</span><span class="sxs-lookup"><span data-stu-id="3470e-116">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="3470e-117">3. példa: a ActivityLogAlert engedélyezése a ResourceId paraméterrel</span><span class="sxs-lookup"><span data-stu-id="3470e-117">Example 3: Enable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Enable-AzureRmActivityLogAlert
```

<span data-ttu-id="3470e-118">Ez a parancs engedélyezi az ActivityLogAlert a ResourceId paraméterrel a csőben.</span><span class="sxs-lookup"><span data-stu-id="3470e-118">This command enables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="3470e-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3470e-119">PARAMETERS</span></span>

### <span data-ttu-id="3470e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3470e-120">-DefaultProfile</span></span>
<span data-ttu-id="3470e-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3470e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3470e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3470e-122">-InputObject</span></span>
<span data-ttu-id="3470e-123">A hívás InputObject tulajdonságát állítja be a kötelező név, az erőforráscsoport neve és a választható címkék tulajdonságai kinyeréséhez.</span><span class="sxs-lookup"><span data-stu-id="3470e-123">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tags properties.</span></span>

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

### <span data-ttu-id="3470e-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3470e-124">-Name</span></span>
<span data-ttu-id="3470e-125">A műveletnapló riasztásának neve.</span><span class="sxs-lookup"><span data-stu-id="3470e-125">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="3470e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3470e-126">-ResourceGroupName</span></span>
<span data-ttu-id="3470e-127">Annak az erőforráscsoportnek a neve, amelyben az értesítési erőforrás létezik.</span><span class="sxs-lookup"><span data-stu-id="3470e-127">The name of the resource group where the alert resource is going to exist.</span></span>

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

### <span data-ttu-id="3470e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3470e-128">-ResourceId</span></span>
<span data-ttu-id="3470e-129">A hívás ResourceId-címkék tulajdonságát adja meg a szükséges név, az erőforráscsoport nevének kinyeréséhez.</span><span class="sxs-lookup"><span data-stu-id="3470e-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="3470e-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3470e-130">-Confirm</span></span>
<span data-ttu-id="3470e-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3470e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3470e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3470e-132">-WhatIf</span></span>
<span data-ttu-id="3470e-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3470e-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3470e-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3470e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3470e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3470e-135">CommonParameters</span></span>
<span data-ttu-id="3470e-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3470e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3470e-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3470e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3470e-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3470e-138">INPUTS</span></span>

### <span data-ttu-id="3470e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3470e-139">System.String</span></span>

### <span data-ttu-id="3470e-140">Microsoft. Azure. commands. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="3470e-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>
<span data-ttu-id="3470e-141">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3470e-141">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="3470e-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3470e-142">OUTPUTS</span></span>

### <span data-ttu-id="3470e-143">Microsoft. Azure. commands. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="3470e-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="3470e-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3470e-144">NOTES</span></span>

## <span data-ttu-id="3470e-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3470e-145">RELATED LINKS</span></span>

[<span data-ttu-id="3470e-146">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="3470e-146">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="3470e-147">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="3470e-147">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="3470e-148">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="3470e-148">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="3470e-149">Új – AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="3470e-149">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="3470e-150">Új – AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="3470e-150">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

[<span data-ttu-id="3470e-151">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="3470e-151">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)
