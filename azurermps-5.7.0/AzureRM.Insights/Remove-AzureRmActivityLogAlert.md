---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActivityLogAlert.md
ms.openlocfilehash: b712363b2b4e1d610f00f1111c48145debe084a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500587"
---
# <span data-ttu-id="2e551-101">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2e551-101">Remove-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="2e551-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2e551-102">SYNOPSIS</span></span>
<span data-ttu-id="2e551-103">Tevékenység-naplózási riasztás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="2e551-103">Removes an activity log alert.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e551-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2e551-104">SYNTAX</span></span>

### <span data-ttu-id="2e551-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2e551-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e551-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="2e551-106">RemoveByInputObject</span></span>
```
Remove-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e551-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="2e551-107">RemoveByResourceId</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e551-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2e551-108">DESCRIPTION</span></span>
<span data-ttu-id="2e551-109">Az **Eltávolítás – AzureRmActivityLogAlert** parancsmag eltávolítja a műveletnapló riasztását.</span><span class="sxs-lookup"><span data-stu-id="2e551-109">The **Remove-AzureRmActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="2e551-110">Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges javításának megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="2e551-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

<span data-ttu-id="2e551-111">Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges létrehozása, módosítása vagy eltávolítása előtt.</span><span class="sxs-lookup"><span data-stu-id="2e551-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="2e551-112">Példák</span><span class="sxs-lookup"><span data-stu-id="2e551-112">EXAMPLES</span></span>

### <span data-ttu-id="2e551-113">1. példa: tevékenység-naplózási riasztás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="2e551-113">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzureRmActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="2e551-114">Tevékenység-naplózási riasztás eltávolítása a név és az erőforrás csoport nevében bemenetként.</span><span class="sxs-lookup"><span data-stu-id="2e551-114">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="2e551-115">2. példa: tevékenység-naplózási riasztás eltávolítása PSActivityLogAlertResource adatbevitelsel</span><span class="sxs-lookup"><span data-stu-id="2e551-115">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzureRmActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="2e551-116">Tevékenység-naplózási riasztás eltávolítása PSActivityLogAlertResource adatbevitel útján</span><span class="sxs-lookup"><span data-stu-id="2e551-116">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="2e551-117">3. példa: a ActivityLogAlert eltávolítása a ResourceId paraméterrel</span><span class="sxs-lookup"><span data-stu-id="2e551-117">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Remove-AzureRmActivityLogAlert
```

<span data-ttu-id="2e551-118">Ez a parancs eltávolítja a ActivityLogAlert a ResourceId paraméterrel a pipe-ról.</span><span class="sxs-lookup"><span data-stu-id="2e551-118">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="2e551-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2e551-119">PARAMETERS</span></span>

### <span data-ttu-id="2e551-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e551-120">-DefaultProfile</span></span>
<span data-ttu-id="2e551-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2e551-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e551-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e551-122">-InputObject</span></span>
<span data-ttu-id="2e551-123">A hívás InputObject (címkék) tulajdonságát adja meg a szükséges név és az erőforrás csoport nevének kinyeréséhez.</span><span class="sxs-lookup"><span data-stu-id="2e551-123">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: PSActivityLogAlertResource
Parameter Sets: RemoveByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e551-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2e551-124">-Name</span></span>
<span data-ttu-id="2e551-125">A műveletnapló riasztásának neve.</span><span class="sxs-lookup"><span data-stu-id="2e551-125">The name of the activity log alert.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e551-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e551-126">-ResourceGroupName</span></span>
<span data-ttu-id="2e551-127">Annak az erőforráscsoportnek a neve, amelyben az értesítési erőforrás létezik.</span><span class="sxs-lookup"><span data-stu-id="2e551-127">The name of the resource group where the alert resource exists.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e551-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e551-128">-ResourceId</span></span>
<span data-ttu-id="2e551-129">A hívás ResourceId-címkék tulajdonságát adja meg a szükséges név, az erőforráscsoport nevének kinyeréséhez.</span><span class="sxs-lookup"><span data-stu-id="2e551-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e551-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2e551-130">-Confirm</span></span>
<span data-ttu-id="2e551-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2e551-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e551-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e551-132">-WhatIf</span></span>
<span data-ttu-id="2e551-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2e551-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2e551-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2e551-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e551-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e551-135">CommonParameters</span></span>
<span data-ttu-id="2e551-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2e551-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e551-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e551-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e551-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e551-138">INPUTS</span></span>

### <span data-ttu-id="2e551-139">Nincs</span><span class="sxs-lookup"><span data-stu-id="2e551-139">None</span></span>
<span data-ttu-id="2e551-140">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="2e551-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2e551-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e551-141">OUTPUTS</span></span>

### <span data-ttu-id="2e551-142">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2e551-142">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="2e551-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2e551-143">NOTES</span></span>

## <span data-ttu-id="2e551-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e551-144">RELATED LINKS</span></span>

[<span data-ttu-id="2e551-145">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2e551-145">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="2e551-146">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2e551-146">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="2e551-147">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2e551-147">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="2e551-148">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2e551-148">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="2e551-149">Új – AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="2e551-149">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="2e551-150">Új – AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="2e551-150">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

