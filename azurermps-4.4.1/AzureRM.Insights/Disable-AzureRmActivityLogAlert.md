---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Disable-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Disable-AzureRmActivityLogAlert.md
ms.openlocfilehash: cf920fe8fbe235a2c003bebc0cdecf1a480926ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680539"
---
# <span data-ttu-id="5d2ef-101">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5d2ef-101">Disable-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="5d2ef-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5d2ef-102">SYNOPSIS</span></span>
<span data-ttu-id="5d2ef-103">Letiltja a műveletnapló riasztását, és beállítja annak címkéit.</span><span class="sxs-lookup"><span data-stu-id="5d2ef-103">Disables an activity log alert and sets its tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d2ef-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5d2ef-104">SYNTAX</span></span>

### <span data-ttu-id="5d2ef-105">Az alapértelmezett paraméterek a műveletnapló riasztásának letiltásához</span><span class="sxs-lookup"><span data-stu-id="5d2ef-105">Default parameters for disable an activity log alert</span></span>
```
Disable-AzureRmActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d2ef-106">Paraméterek a tevékenység-naplózási riasztások letiltásához a pipe-ról</span><span class="sxs-lookup"><span data-stu-id="5d2ef-106">Parameters to disable an activity log alerts taking value from the pipe</span></span>
```
Disable-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d2ef-107">A műveletnapló letiltására szolgáló paraméterek a ResourceId a pipe-ról</span><span class="sxs-lookup"><span data-stu-id="5d2ef-107">Parameters to disable an activity log alerts taking the value of ResourceId from the pipe</span></span>
```
Disable-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d2ef-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5d2ef-108">DESCRIPTION</span></span>
<span data-ttu-id="5d2ef-109">A **disable-AzureRmActivityLogAlert** parancsmag letiltja és aktivitási naplót jelenít meg, és lehetővé teszi a címkék beállítását.</span><span class="sxs-lookup"><span data-stu-id="5d2ef-109">The **Disable-AzureRmActivityLogAlert** cmdlet disables and activity log alert and allows setting its tags.</span></span>
<span data-ttu-id="5d2ef-110">Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges javításának megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="5d2ef-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="5d2ef-111">Példák</span><span class="sxs-lookup"><span data-stu-id="5d2ef-111">EXAMPLES</span></span>

### <span data-ttu-id="5d2ef-112">1. példa: tevékenység-naplózási riasztás letiltása</span><span class="sxs-lookup"><span data-stu-id="5d2ef-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Disable-AzureRmActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="5d2ef-113">Ez a parancs letiltja a alert1 nevű műveletnapló riasztást az erőforráscsoport default-ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="5d2ef-113">This command disables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

<span data-ttu-id="5d2ef-114">Ez a parancs megváltoztatja a alert1 nevű műveletnapló-riasztás címkék tulajdonságát, és letiltja azt.</span><span class="sxs-lookup"><span data-stu-id="5d2ef-114">This command changes the tags property of the activity log alert called alert1 and disables it.</span></span>

### <span data-ttu-id="5d2ef-115">2. példa: tevékenység-naplózási riasztás letiltása PSActivityLogAlertResource-objektum használatával bemenetként</span><span class="sxs-lookup"><span data-stu-id="5d2ef-115">Example 2: Disable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Disable-AzureRmActivityLogAlert -InputObject $obj
```

<span data-ttu-id="5d2ef-116">Ez a parancs letiltja a alert1 nevű műveletnapló riasztást.</span><span class="sxs-lookup"><span data-stu-id="5d2ef-116">This command disables an activity log alert called alert1.</span></span> <span data-ttu-id="5d2ef-117">Ehhez a PSActivityLogAlertResource objektumot használja bemeneti argumentumként.</span><span class="sxs-lookup"><span data-stu-id="5d2ef-117">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="5d2ef-118">3. példa: a ActivityLogAlert letiltása a ResourceId paraméterrel</span><span class="sxs-lookup"><span data-stu-id="5d2ef-118">Example 3: Disable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Disable-AzureRmActivityLogAlert
```

<span data-ttu-id="5d2ef-119">Ez a parancs letiltja a ActivityLogAlert a ResourceId paraméterrel a pipe-ról.</span><span class="sxs-lookup"><span data-stu-id="5d2ef-119">This command disables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="5d2ef-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5d2ef-120">PARAMETERS</span></span>

### <span data-ttu-id="5d2ef-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5d2ef-121">-Name</span></span>
<span data-ttu-id="5d2ef-122">A műveletnapló riasztásának neve.</span><span class="sxs-lookup"><span data-stu-id="5d2ef-122">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for disable an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d2ef-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d2ef-123">-ResourceGroupName</span></span>
<span data-ttu-id="5d2ef-124">Annak az erőforráscsoportnek a neve, amelyben az értesítési erőforrás létezik.</span><span class="sxs-lookup"><span data-stu-id="5d2ef-124">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for disable an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d2ef-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d2ef-125">-InputObject</span></span>
<span data-ttu-id="5d2ef-126">A hívás InputObject tulajdonságát állítja be a kötelező név, az erőforráscsoport neve és a választható címke tulajdonságai kinyeréséhez.</span><span class="sxs-lookup"><span data-stu-id="5d2ef-126">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tag properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: Parameters to disable an activity log alerts taking value from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d2ef-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d2ef-127">-ResourceId</span></span>
<span data-ttu-id="5d2ef-128">A hívás ResourceId-címkék tulajdonságát adja meg a szükséges név, az erőforráscsoport nevének kinyeréséhez.</span><span class="sxs-lookup"><span data-stu-id="5d2ef-128">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters to disable an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d2ef-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5d2ef-129">-Confirm</span></span>
<span data-ttu-id="5d2ef-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5d2ef-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d2ef-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d2ef-131">-DefaultProfile</span></span>
<span data-ttu-id="5d2ef-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5d2ef-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d2ef-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d2ef-133">-WhatIf</span></span>
<span data-ttu-id="5d2ef-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5d2ef-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5d2ef-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5d2ef-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d2ef-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d2ef-136">CommonParameters</span></span>
<span data-ttu-id="5d2ef-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5d2ef-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d2ef-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d2ef-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d2ef-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d2ef-139">INPUTS</span></span>

## <span data-ttu-id="5d2ef-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d2ef-140">OUTPUTS</span></span>

### <span data-ttu-id="5d2ef-141">Microsoft. Azure. commands. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="5d2ef-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="5d2ef-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5d2ef-142">NOTES</span></span>

## <span data-ttu-id="5d2ef-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5d2ef-143">RELATED LINKS</span></span>

[<span data-ttu-id="5d2ef-144">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5d2ef-144">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="5d2ef-145">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5d2ef-145">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="5d2ef-146">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5d2ef-146">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="5d2ef-147">Új – AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="5d2ef-147">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="5d2ef-148">Új – AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="5d2ef-148">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

[<span data-ttu-id="5d2ef-149">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5d2ef-149">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)
