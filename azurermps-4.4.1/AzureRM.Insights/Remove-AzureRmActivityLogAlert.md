---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActivityLogAlert.md
ms.openlocfilehash: adff43beed709db91b2f22bd1072728d3e7a0425
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680884"
---
# <span data-ttu-id="3965f-101">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="3965f-101">Remove-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="3965f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3965f-102">SYNOPSIS</span></span>
<span data-ttu-id="3965f-103">Tevékenység-naplózási riasztás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="3965f-103">Removes an activity log alert.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3965f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3965f-104">SYNTAX</span></span>

### <span data-ttu-id="3965f-105">A tevékenység-naplózási riasztás eltávolításának alapértelmezett paraméterei</span><span class="sxs-lookup"><span data-stu-id="3965f-105">Default parameters for remove an activity log alert</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3965f-106">A tevékenység naplóját tartalmazó riasztási riasztások eltávolítására szolgáló paraméterek</span><span class="sxs-lookup"><span data-stu-id="3965f-106">Parameters to remove an activity log alerts taking value from the pipe</span></span>
```
Remove-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3965f-107">A műveletnapló ResourceId értékét figyelembe vevő paraméterek a műveletnapló eltávolításához</span><span class="sxs-lookup"><span data-stu-id="3965f-107">Parameters to remove an activity log alerts taking the value of ResourceId from the pipe</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3965f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3965f-108">DESCRIPTION</span></span>
<span data-ttu-id="3965f-109">Az **Eltávolítás – AzureRmActivityLogAlert** parancsmag eltávolítja a műveletnapló riasztását.</span><span class="sxs-lookup"><span data-stu-id="3965f-109">The **Remove-AzureRmActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="3965f-110">Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges javításának megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="3965f-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="3965f-111">Példák</span><span class="sxs-lookup"><span data-stu-id="3965f-111">EXAMPLES</span></span>

### <span data-ttu-id="3965f-112">1. példa: tevékenység-naplózási riasztás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3965f-112">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzureRmActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="3965f-113">Tevékenység-naplózási riasztás eltávolítása a név és az erőforrás csoport nevében bemenetként.</span><span class="sxs-lookup"><span data-stu-id="3965f-113">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="3965f-114">2. példa: tevékenység-naplózási riasztás eltávolítása PSActivityLogAlertResource adatbevitelsel</span><span class="sxs-lookup"><span data-stu-id="3965f-114">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzureRmActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="3965f-115">Tevékenység-naplózási riasztás eltávolítása PSActivityLogAlertResource adatbevitel útján</span><span class="sxs-lookup"><span data-stu-id="3965f-115">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="3965f-116">3. példa: a ActivityLogAlert eltávolítása a ResourceId paraméterrel</span><span class="sxs-lookup"><span data-stu-id="3965f-116">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Remove-AzureRmActivityLogAlert
```

<span data-ttu-id="3965f-117">Ez a parancs eltávolítja a ActivityLogAlert a ResourceId paraméterrel a pipe-ról.</span><span class="sxs-lookup"><span data-stu-id="3965f-117">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="3965f-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3965f-118">PARAMETERS</span></span>

### <span data-ttu-id="3965f-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3965f-119">-Name</span></span>
<span data-ttu-id="3965f-120">A műveletnapló riasztásának neve.</span><span class="sxs-lookup"><span data-stu-id="3965f-120">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for remove an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3965f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3965f-121">-ResourceGroupName</span></span>
<span data-ttu-id="3965f-122">Annak az erőforráscsoportnek a neve, amelyben az értesítési erőforrás létezik.</span><span class="sxs-lookup"><span data-stu-id="3965f-122">The name of the resource group where the alert resource exists.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for remove an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3965f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3965f-123">-InputObject</span></span>
<span data-ttu-id="3965f-124">A hívás InputObject (címkék) tulajdonságát adja meg a szükséges név és az erőforrás csoport nevének kinyeréséhez.</span><span class="sxs-lookup"><span data-stu-id="3965f-124">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: Parameters to remove an activity log alerts taking value from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3965f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3965f-125">-ResourceId</span></span>
<span data-ttu-id="3965f-126">A hívás ResourceId-címkék tulajdonságát adja meg a szükséges név, az erőforráscsoport nevének kinyeréséhez.</span><span class="sxs-lookup"><span data-stu-id="3965f-126">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters to remove an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3965f-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3965f-127">-Confirm</span></span>
<span data-ttu-id="3965f-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3965f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3965f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3965f-129">-DefaultProfile</span></span>
<span data-ttu-id="3965f-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3965f-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3965f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3965f-131">-WhatIf</span></span>
<span data-ttu-id="3965f-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3965f-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3965f-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3965f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3965f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3965f-134">CommonParameters</span></span>
<span data-ttu-id="3965f-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3965f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3965f-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3965f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3965f-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3965f-137">INPUTS</span></span>

## <span data-ttu-id="3965f-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3965f-138">OUTPUTS</span></span>

### <span data-ttu-id="3965f-139">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="3965f-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="3965f-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3965f-140">NOTES</span></span>

## <span data-ttu-id="3965f-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3965f-141">RELATED LINKS</span></span>

[<span data-ttu-id="3965f-142">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="3965f-142">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="3965f-143">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="3965f-143">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="3965f-144">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="3965f-144">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="3965f-145">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="3965f-145">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="3965f-146">Új – AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="3965f-146">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="3965f-147">Új – AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="3965f-147">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

