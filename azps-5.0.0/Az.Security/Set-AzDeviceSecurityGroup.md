---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzDeviceSecurityGroup.md
ms.openlocfilehash: 269d333c9b74ed0e3e959ef609531bcea41b724c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186727"
---
# <span data-ttu-id="abcb0-101">Set-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="abcb0-101">Set-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="abcb0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="abcb0-102">SYNOPSIS</span></span>
<span data-ttu-id="abcb0-103">Eszköz biztonsági csoportjának létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="abcb0-103">Create or update device security group</span></span>

## <span data-ttu-id="abcb0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="abcb0-104">SYNTAX</span></span>

### <span data-ttu-id="abcb0-105">ResourceIdLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="abcb0-105">ResourceIdLevelResource (Default)</span></span>
```
Set-AzDeviceSecurityGroup -Name <String> -HubResourceId <String>
 [-ThresholdRule <PSThresholdCustomAlertRule[]>] [-TimeWindowRule <PSTimeWindowCustomAlertRule[]>]
 [-AllowlistRule <PSAllowlistCustomAlertRule[]>] [-DenylistRule <PSDenylistCustomAlertRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abcb0-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="abcb0-106">InputObject</span></span>
```
Set-AzDeviceSecurityGroup [-ThresholdRule <PSThresholdCustomAlertRule[]>]
 [-TimeWindowRule <PSTimeWindowCustomAlertRule[]>] [-AllowlistRule <PSAllowlistCustomAlertRule[]>]
 [-DenylistRule <PSDenylistCustomAlertRule[]>] -InputObject <PSDeviceSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abcb0-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="abcb0-107">ResourceId</span></span>
```
Set-AzDeviceSecurityGroup [-ThresholdRule <PSThresholdCustomAlertRule[]>]
 [-TimeWindowRule <PSTimeWindowCustomAlertRule[]>] [-AllowlistRule <PSAllowlistCustomAlertRule[]>]
 [-DenylistRule <PSDenylistCustomAlertRule[]>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abcb0-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="abcb0-108">DESCRIPTION</span></span>
<span data-ttu-id="abcb0-109">Az Set-AzDeviceSecurityGroup parancsmag a IOT biztonsági megoldásban meghatározott eszközönkénti biztonsági csoportot hoz létre vagy frissít.</span><span class="sxs-lookup"><span data-stu-id="abcb0-109">The Set-AzDeviceSecurityGroup cmdlet creates or updates a device security group defined in iot security solution.</span></span>

## <span data-ttu-id="abcb0-110">Példák</span><span class="sxs-lookup"><span data-stu-id="abcb0-110">EXAMPLES</span></span>

### <span data-ttu-id="abcb0-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="abcb0-111">Example 1</span></span>
```powershell
PS C:\> $TimeWindowSize = New-TimeSpan -Minutes 5
PS C:\> $TimeWindowRule = New-AzDeviceSecurityGroupTimeWindowRuleObject -Type "ActiveConnectionsNotInAllowedRange" -Enabled $true 
-MaxThreshold 30 -MinThreshold 0 -TimeWindowSize $TimeWindowSize
PS C:\> Set-AzDeviceSecurityGroup -Name "MySecurityGroup" 
-HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" 
-TimeWindowRule $TimeWindowRules

Id: "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub/providers/Microsoft.Security/deviceSecurityGroups/MySecurityGroup"
Name: "MySecurityGroup"
Type: "Microsoft.Security/deviceSecurityGroups"
ThresholdRules: []
TimeWindowRules: [
            {
              RuleType: "ActiveConnectionsNotInAllowedRange"
              DisplayName: "Number of active connections is not in allowed range"
              Description: "Get an alert when the number of active connections of a device in the time window is not in the allowed range"
              IsEnabled: true
              MinThreshold: 0
              MaxThreshold: 0
              TimeWindowSize: "PT5M"
            }]
AllowlistRules: [
            {
              RuleType": "ConnectionToIpNotAllowed",
              DisplayName: "Outbound connection to an ip that isn't allowed"
              Description: "Get an alert when an outbound connection is created between your device and an ip that isn't allowed"
              IsEnabled: false
              ValueType: "IpCidr"
              AllowlistValues: []
            },
            {
              RuleType: "LocalUserNotAllowed"
              DisplayName: "Login by a local user that isn't allowed"
              Description: "Get an alert when a local user that isn't allowed logins to the device"
              IsEnabled: false
              ValueType: "String"
              AllowlistValues: []
            }]
DenylistRules: []
```

<span data-ttu-id="abcb0-112">A meglévő eszköz biztonsági csoportjának frissítése a IoT hub "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" és a "ActiveConnectionsNotInAllowedRange" szabály típusával</span><span class="sxs-lookup"><span data-stu-id="abcb0-112">Update existing device security group from IoT Hub "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" with rule type "ActiveConnectionsNotInAllowedRange"</span></span>

## <span data-ttu-id="abcb0-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="abcb0-113">PARAMETERS</span></span>

### <span data-ttu-id="abcb0-114">-AllowlistRule</span><span class="sxs-lookup"><span data-stu-id="abcb0-114">-AllowlistRule</span></span>
<span data-ttu-id="abcb0-115">A lista szabályainak engedélyezése</span><span class="sxs-lookup"><span data-stu-id="abcb0-115">Allow list rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule[]
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule[]
Parameter Sets: InputObject, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abcb0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abcb0-116">-DefaultProfile</span></span>
<span data-ttu-id="abcb0-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="abcb0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abcb0-118">-DenylistRule</span><span class="sxs-lookup"><span data-stu-id="abcb0-118">-DenylistRule</span></span>
<span data-ttu-id="abcb0-119">A lista szabályainak elutasítása</span><span class="sxs-lookup"><span data-stu-id="abcb0-119">Deny list rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule[]
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule[]
Parameter Sets: InputObject, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abcb0-120">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="abcb0-120">-HubResourceId</span></span>
<span data-ttu-id="abcb0-121">IoT hub erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="abcb0-121">IoT Hub resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abcb0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="abcb0-122">-InputObject</span></span>
<span data-ttu-id="abcb0-123">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="abcb0-123">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="abcb0-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="abcb0-124">-Name</span></span>
<span data-ttu-id="abcb0-125">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="abcb0-125">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abcb0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="abcb0-126">-ResourceId</span></span>
<span data-ttu-id="abcb0-127">Annak a biztonsági erőforrásnak az azonosítója, amelyre a parancsot be szeretné hívni.</span><span class="sxs-lookup"><span data-stu-id="abcb0-127">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abcb0-128">-ThresholdRule</span><span class="sxs-lookup"><span data-stu-id="abcb0-128">-ThresholdRule</span></span>
<span data-ttu-id="abcb0-129">Küszöb szabályok.</span><span class="sxs-lookup"><span data-stu-id="abcb0-129">Threshold rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule[]
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule[]
Parameter Sets: InputObject, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abcb0-130">-TimeWindowRule</span><span class="sxs-lookup"><span data-stu-id="abcb0-130">-TimeWindowRule</span></span>
<span data-ttu-id="abcb0-131">Az idő ablak szabályai</span><span class="sxs-lookup"><span data-stu-id="abcb0-131">Time window rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule[]
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule[]
Parameter Sets: InputObject, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abcb0-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="abcb0-132">-Confirm</span></span>
<span data-ttu-id="abcb0-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="abcb0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abcb0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abcb0-134">-WhatIf</span></span>
<span data-ttu-id="abcb0-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="abcb0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abcb0-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="abcb0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abcb0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abcb0-137">CommonParameters</span></span>
<span data-ttu-id="abcb0-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="abcb0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abcb0-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="abcb0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abcb0-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="abcb0-140">INPUTS</span></span>

### <span data-ttu-id="abcb0-141">Microsoft. Azure. commands. Security. models. DeviceSecurityGroups. PSThresholdCustomAlertRule []</span><span class="sxs-lookup"><span data-stu-id="abcb0-141">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule[]</span></span>

### <span data-ttu-id="abcb0-142">Microsoft. Azure. commands. Security. models. DeviceSecurityGroups. PSTimeWindowCustomAlertRule []</span><span class="sxs-lookup"><span data-stu-id="abcb0-142">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule[]</span></span>

### <span data-ttu-id="abcb0-143">Microsoft. Azure. commands. Security. models. DeviceSecurityGroups. PSAllowlistCustomAlertRule []</span><span class="sxs-lookup"><span data-stu-id="abcb0-143">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule[]</span></span>

### <span data-ttu-id="abcb0-144">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule []</span><span class="sxs-lookup"><span data-stu-id="abcb0-144">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule[]</span></span>

### <span data-ttu-id="abcb0-145">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="abcb0-145">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

### <span data-ttu-id="abcb0-146">System. String</span><span class="sxs-lookup"><span data-stu-id="abcb0-146">System.String</span></span>

## <span data-ttu-id="abcb0-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="abcb0-147">OUTPUTS</span></span>

### <span data-ttu-id="abcb0-148">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="abcb0-148">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

## <span data-ttu-id="abcb0-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="abcb0-149">NOTES</span></span>

## <span data-ttu-id="abcb0-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="abcb0-150">RELATED LINKS</span></span>
