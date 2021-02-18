---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/disable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Disable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Disable-AzActivityLogAlert.md
ms.openlocfilehash: 4ce3bc8c0efd5acd4e39d61c083c82bff960066e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100409222"
---
# <span data-ttu-id="5e4d4-101">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5e4d4-101">Disable-AzActivityLogAlert</span></span>

## <span data-ttu-id="5e4d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e4d4-102">SYNOPSIS</span></span>
<span data-ttu-id="5e4d4-103">Letilt egy tevékenységnapló-riasztást, és beállítja a címkéit.</span><span class="sxs-lookup"><span data-stu-id="5e4d4-103">Disables an activity log alert and sets its tags.</span></span>

## <span data-ttu-id="5e4d4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5e4d4-104">SYNTAX</span></span>

### <span data-ttu-id="5e4d4-105">DisableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5e4d4-105">DisableByNameAndResourceGroup</span></span>
```
Disable-AzActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e4d4-106">DisableByInputObject</span><span class="sxs-lookup"><span data-stu-id="5e4d4-106">DisableByInputObject</span></span>
```
Disable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e4d4-107">DisableByResourceId</span><span class="sxs-lookup"><span data-stu-id="5e4d4-107">DisableByResourceId</span></span>
```
Disable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5e4d4-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5e4d4-108">DESCRIPTION</span></span>
<span data-ttu-id="5e4d4-109">A **Disable-AzActivityLogAlert** parancsmag letiltja a tevékenységek naplóját, és lehetővé teszi a címkék beállítását.</span><span class="sxs-lookup"><span data-stu-id="5e4d4-109">The **Disable-AzActivityLogAlert** cmdlet disables and activity log alert and allows setting its tags.</span></span>
<span data-ttu-id="5e4d4-110">Ez a parancsmag implementálja a ShouldProcess mintát, azaz megerősítést kérhet a felhasználótól, mielőtt ténylegesen javítja az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="5e4d4-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="5e4d4-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5e4d4-111">EXAMPLES</span></span>

### <span data-ttu-id="5e4d4-112">1. példa: Tevékenységnapló-riasztás letiltása</span><span class="sxs-lookup"><span data-stu-id="5e4d4-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Disable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="5e4d4-113">Ez a parancs letiltja a Tevékenységnapló riasztás1 nevű riasztását a Default-ActivityLogsAlerts erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="5e4d4-113">This command disables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>
<span data-ttu-id="5e4d4-114">Ez a parancs módosítja a riasztás1 nevű tevékenységnapló-riasztás címketulajdonságát, és letiltja azt.</span><span class="sxs-lookup"><span data-stu-id="5e4d4-114">This command changes the tags property of the activity log alert called alert1 and disables it.</span></span>

### <span data-ttu-id="5e4d4-115">2. példa: Tevékenységnapló-riasztás letiltása a PSActivityLogAlertResource objektum használatával bevitelként</span><span class="sxs-lookup"><span data-stu-id="5e4d4-115">Example 2: Disable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Disable-AzActivityLogAlert -InputObject $obj
```

<span data-ttu-id="5e4d4-116">Ez a parancs letiltja az 1. tevékenységnapló-riasztást.</span><span class="sxs-lookup"><span data-stu-id="5e4d4-116">This command disables an activity log alert called alert1.</span></span> <span data-ttu-id="5e4d4-117">Ehhez bemeneti argumentumként egy PSActivityLogAlertResource objektumot használ.</span><span class="sxs-lookup"><span data-stu-id="5e4d4-117">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="5e4d4-118">3. példa: A ActivityLogAlert letiltása az ResourceId paraméter használatával</span><span class="sxs-lookup"><span data-stu-id="5e4d4-118">Example 3: Disable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Disable-AzActivityLogAlert
```

<span data-ttu-id="5e4d4-119">Ez a parancs letiltja a ActivityLogAlert paramétert a pipe ResourceId paraméterével.</span><span class="sxs-lookup"><span data-stu-id="5e4d4-119">This command disables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="5e4d4-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e4d4-120">PARAMETERS</span></span>

### <span data-ttu-id="5e4d4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e4d4-121">-DefaultProfile</span></span>
<span data-ttu-id="5e4d4-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5e4d4-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e4d4-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e4d4-123">-InputObject</span></span>
<span data-ttu-id="5e4d4-124">Beállítja a hívás InputObject tags tulajdonságát, hogy kinyerje a kötelező nevet, az erőforráscsoport nevét és a választható címketulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="5e4d4-124">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tag properties.</span></span>

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

### <span data-ttu-id="5e4d4-125">-Name</span><span class="sxs-lookup"><span data-stu-id="5e4d4-125">-Name</span></span>
<span data-ttu-id="5e4d4-126">A tevékenységnapló-riasztás neve.</span><span class="sxs-lookup"><span data-stu-id="5e4d4-126">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="5e4d4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e4d4-127">-ResourceGroupName</span></span>
<span data-ttu-id="5e4d4-128">Annak az erőforráscsoportnak a neve, amelyben a riasztási erőforrás létezni fog.</span><span class="sxs-lookup"><span data-stu-id="5e4d4-128">The name of the resource group where the alert resource is going to exist.</span></span>

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

### <span data-ttu-id="5e4d4-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e4d4-129">-ResourceId</span></span>
<span data-ttu-id="5e4d4-130">Beállítja a hívás ResourceId tags tulajdonságát a szükséges név, az erőforráscsoport nevének tulajdonságainak kibontása érdekében.</span><span class="sxs-lookup"><span data-stu-id="5e4d4-130">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="5e4d4-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5e4d4-131">-Confirm</span></span>
<span data-ttu-id="5e4d4-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5e4d4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e4d4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e4d4-133">-WhatIf</span></span>
<span data-ttu-id="5e4d4-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5e4d4-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5e4d4-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5e4d4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e4d4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e4d4-136">CommonParameters</span></span>
<span data-ttu-id="5e4d4-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e4d4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e4d4-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5e4d4-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e4d4-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5e4d4-139">INPUTS</span></span>

### <span data-ttu-id="5e4d4-140">System.String</span><span class="sxs-lookup"><span data-stu-id="5e4d4-140">System.String</span></span>

### <span data-ttu-id="5e4d4-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="5e4d4-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="5e4d4-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e4d4-142">OUTPUTS</span></span>

### <span data-ttu-id="5e4d4-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="5e4d4-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="5e4d4-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5e4d4-144">NOTES</span></span>

## <span data-ttu-id="5e4d4-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5e4d4-145">RELATED LINKS</span></span>

[<span data-ttu-id="5e4d4-146">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5e4d4-146">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="5e4d4-147">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5e4d4-147">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="5e4d4-148">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5e4d4-148">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="5e4d4-149">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="5e4d4-149">New-AzActionGroup</span></span>](./New-AzActionGroup.md)



[<span data-ttu-id="5e4d4-150">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5e4d4-150">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)
