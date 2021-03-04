---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzDeviceSecurityGroup.md
ms.openlocfilehash: 19f610cb4b17e32e88ddb85b01d6de82926b7eba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940009"
---
# <span data-ttu-id="53bea-101">Set-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="53bea-101">Set-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="53bea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53bea-102">SYNOPSIS</span></span>
<span data-ttu-id="53bea-103">Eszközbiztonsági csoport létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="53bea-103">Create or update device security group</span></span>

## <span data-ttu-id="53bea-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="53bea-104">SYNTAX</span></span>

### <span data-ttu-id="53bea-105">ResourceIdLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="53bea-105">ResourceIdLevelResource (Default)</span></span>
```
Set-AzDeviceSecurityGroup -Name <String> -HubResourceId <String>
 [-ThresholdRule <PSThresholdCustomAlertRule[]>] [-TimeWindowRule <PSTimeWindowCustomAlertRule[]>]
 [-AllowlistRule <PSAllowlistCustomAlertRule[]>] [-DenylistRule <PSDenylistCustomAlertRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53bea-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="53bea-106">InputObject</span></span>
```
Set-AzDeviceSecurityGroup [-ThresholdRule <PSThresholdCustomAlertRule[]>]
 [-TimeWindowRule <PSTimeWindowCustomAlertRule[]>] [-AllowlistRule <PSAllowlistCustomAlertRule[]>]
 [-DenylistRule <PSDenylistCustomAlertRule[]>] -InputObject <PSDeviceSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53bea-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="53bea-107">ResourceId</span></span>
```
Set-AzDeviceSecurityGroup [-ThresholdRule <PSThresholdCustomAlertRule[]>]
 [-TimeWindowRule <PSTimeWindowCustomAlertRule[]>] [-AllowlistRule <PSAllowlistCustomAlertRule[]>]
 [-DenylistRule <PSDenylistCustomAlertRule[]>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53bea-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="53bea-108">DESCRIPTION</span></span>
<span data-ttu-id="53bea-109">A Set-AzDeviceSecurityGroup parancsmag létrehoz vagy frissíti az iot biztonsági megoldásban definiált eszközbiztonsági csoportot.</span><span class="sxs-lookup"><span data-stu-id="53bea-109">The Set-AzDeviceSecurityGroup cmdlet creates or updates a device security group defined in iot security solution.</span></span>

## <span data-ttu-id="53bea-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="53bea-110">EXAMPLES</span></span>

### <span data-ttu-id="53bea-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="53bea-111">Example 1</span></span>
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

<span data-ttu-id="53bea-112">A meglévő eszközbiztonsági csoport frissítése az IoT Hubról "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" "ActiveConnectionsNotInAllowedRange" szabálytípussal</span><span class="sxs-lookup"><span data-stu-id="53bea-112">Update existing device security group from IoT Hub "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" with rule type "ActiveConnectionsNotInAllowedRange"</span></span>

## <span data-ttu-id="53bea-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53bea-113">PARAMETERS</span></span>

### <span data-ttu-id="53bea-114">-AllowlistRule</span><span class="sxs-lookup"><span data-stu-id="53bea-114">-AllowlistRule</span></span>
<span data-ttu-id="53bea-115">Listaszabályok engedélyezése lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="53bea-115">Allow list rules.</span></span>

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

### <span data-ttu-id="53bea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53bea-116">-DefaultProfile</span></span>
<span data-ttu-id="53bea-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="53bea-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53bea-118">-DenylistRule</span><span class="sxs-lookup"><span data-stu-id="53bea-118">-DenylistRule</span></span>
<span data-ttu-id="53bea-119">Listaszabályok elutasítása</span><span class="sxs-lookup"><span data-stu-id="53bea-119">Deny list rules.</span></span>

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

### <span data-ttu-id="53bea-120">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="53bea-120">-HubResourceId</span></span>
<span data-ttu-id="53bea-121">IoT-központ erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="53bea-121">IoT Hub resource Id.</span></span>

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

### <span data-ttu-id="53bea-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53bea-122">-InputObject</span></span>
<span data-ttu-id="53bea-123">Bemeneti objektum.</span><span class="sxs-lookup"><span data-stu-id="53bea-123">Input Object.</span></span>

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

### <span data-ttu-id="53bea-124">-Name</span><span class="sxs-lookup"><span data-stu-id="53bea-124">-Name</span></span>
<span data-ttu-id="53bea-125">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="53bea-125">Resource name.</span></span>

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

### <span data-ttu-id="53bea-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53bea-126">-ResourceId</span></span>
<span data-ttu-id="53bea-127">Annak a biztonsági erőforrásnak az azonosítója, amelyről meg szeretné hívni a parancsot.</span><span class="sxs-lookup"><span data-stu-id="53bea-127">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="53bea-128">-ThresholdRule</span><span class="sxs-lookup"><span data-stu-id="53bea-128">-ThresholdRule</span></span>
<span data-ttu-id="53bea-129">Küszöbszabályok.</span><span class="sxs-lookup"><span data-stu-id="53bea-129">Threshold rules.</span></span>

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

### <span data-ttu-id="53bea-130">-TimeWindowRule</span><span class="sxs-lookup"><span data-stu-id="53bea-130">-TimeWindowRule</span></span>
<span data-ttu-id="53bea-131">Időkeret-szabályok.</span><span class="sxs-lookup"><span data-stu-id="53bea-131">Time window rules.</span></span>

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

### <span data-ttu-id="53bea-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53bea-132">-Confirm</span></span>
<span data-ttu-id="53bea-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="53bea-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53bea-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53bea-134">-WhatIf</span></span>
<span data-ttu-id="53bea-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="53bea-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53bea-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="53bea-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53bea-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53bea-137">CommonParameters</span></span>
<span data-ttu-id="53bea-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53bea-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53bea-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53bea-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53bea-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="53bea-140">INPUTS</span></span>

### <span data-ttu-id="53bea-141">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule[]</span><span class="sxs-lookup"><span data-stu-id="53bea-141">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule[]</span></span>

### <span data-ttu-id="53bea-142">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule[]</span><span class="sxs-lookup"><span data-stu-id="53bea-142">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule[]</span></span>

### <span data-ttu-id="53bea-143">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule[]</span><span class="sxs-lookup"><span data-stu-id="53bea-143">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule[]</span></span>

### <span data-ttu-id="53bea-144">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule[]</span><span class="sxs-lookup"><span data-stu-id="53bea-144">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule[]</span></span>

### <span data-ttu-id="53bea-145">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="53bea-145">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

### <span data-ttu-id="53bea-146">System.String</span><span class="sxs-lookup"><span data-stu-id="53bea-146">System.String</span></span>

## <span data-ttu-id="53bea-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="53bea-147">OUTPUTS</span></span>

### <span data-ttu-id="53bea-148">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="53bea-148">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

## <span data-ttu-id="53bea-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="53bea-149">NOTES</span></span>

## <span data-ttu-id="53bea-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="53bea-150">RELATED LINKS</span></span>
