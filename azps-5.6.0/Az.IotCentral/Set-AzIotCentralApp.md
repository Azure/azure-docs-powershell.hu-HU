---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/powershell/module/az.iotcentral/set-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
ms.openlocfilehash: f99faf1ce7420212e87c894c8f5aadeb16578334
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942569"
---
# <span data-ttu-id="47b5b-101">Set-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="47b5b-101">Set-AzIotCentralApp</span></span>

## <span data-ttu-id="47b5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47b5b-102">SYNOPSIS</span></span>
<span data-ttu-id="47b5b-103">Frissíti egy központi IoT-alkalmazás metaadatait.</span><span class="sxs-lookup"><span data-stu-id="47b5b-103">Updates the metadata for an IoT Central Application.</span></span>

## <span data-ttu-id="47b5b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="47b5b-104">SYNTAX</span></span>

### <span data-ttu-id="47b5b-105">ResourceIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="47b5b-105">ResourceIdParameterSet (Default)</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>]
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="47b5b-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="47b5b-106">InputObjectParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>]
 -InputObject <PSIotCentralApp> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="47b5b-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="47b5b-107">InteractiveIotCentralParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="47b5b-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="47b5b-108">DESCRIPTION</span></span>
<span data-ttu-id="47b5b-109">Frissítse egy központi IoT-alkalmazás metaadatait.</span><span class="sxs-lookup"><span data-stu-id="47b5b-109">Update the metadata for an IoT Central Application.</span></span> 

## <span data-ttu-id="47b5b-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="47b5b-110">EXAMPLES</span></span>

### <span data-ttu-id="47b5b-111">1. példa a megjelenítendő név frissítésére</span><span class="sxs-lookup"><span data-stu-id="47b5b-111">Example 1 Update Display Name</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

<span data-ttu-id="47b5b-112">Frissítse a megjelenítendő nevet egy meglévő, központi IoT-alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="47b5b-112">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="47b5b-113">Példakimenet:</span><span class="sxs-lookup"><span data-stu-id="47b5b-113">Example Output:</span></span>

<span data-ttu-id="47b5b-114">ResourceId: /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type: Microsoft.IoTCentral/IoTApps Location : westus Tag : Sku : Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My New Custom Display Name Subdomain : MyAppSubdomain Template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXX ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47b5b-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My New Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="47b5b-115">2. példa az altartomány frissítésére</span><span class="sxs-lookup"><span data-stu-id="47b5b-115">Example 2 Update Subdomain</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "new-subdomain"
```

<span data-ttu-id="47b5b-116">Frissítse a megjelenítendő nevet egy meglévő, központi IoT-alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="47b5b-116">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="47b5b-117">Példakimenet:</span><span class="sxs-lookup"><span data-stu-id="47b5b-117">Example Output:</span></span>

<span data-ttu-id="47b5b-118">ResourceId: /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type: Microsoft.IoTCentral/IoTApps Location : westus Tag : Sku : Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: Display Name Subdomain : new-subdomain Template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXX ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47b5b-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : new-subdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="47b5b-119">Example 3 Update App Sku Info</span><span class="sxs-lookup"><span data-stu-id="47b5b-119">Example 3 Update App Sku Info</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Sku "ST2"
```

<span data-ttu-id="47b5b-120">Frissítse a termékváltozatot egy meglévő, központi IoT-alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="47b5b-120">Update the sku on an existing IoT Central Application.</span></span>

<span data-ttu-id="47b5b-121">Példakimenet:</span><span class="sxs-lookup"><span data-stu-id="47b5b-121">Example Output:</span></span>

<span data-ttu-id="47b5b-122">ResourceId: /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type: Microsoft.IoTCentral/IoTApps Location: westus Tag : Sku : Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: Display Name Subdomain : MyAppSubdomain Template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXX ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47b5b-122">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="47b5b-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47b5b-123">PARAMETERS</span></span>

### <span data-ttu-id="47b5b-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47b5b-124">-AsJob</span></span>
<span data-ttu-id="47b5b-125">Futtassa a parancsmagot feladatként a háttérben.</span><span class="sxs-lookup"><span data-stu-id="47b5b-125">Run cmdlet as a job in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47b5b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47b5b-126">-DefaultProfile</span></span>
<span data-ttu-id="47b5b-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="47b5b-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47b5b-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="47b5b-128">-DisplayName</span></span>
<span data-ttu-id="47b5b-129">Az Iot Központi alkalmazás egyéni megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="47b5b-129">Custom Display Name of the Iot Central Application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47b5b-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47b5b-130">-InputObject</span></span>
<span data-ttu-id="47b5b-131">Iot Central Application Input Object.</span><span class="sxs-lookup"><span data-stu-id="47b5b-131">Iot Central Application Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47b5b-132">-Name</span><span class="sxs-lookup"><span data-stu-id="47b5b-132">-Name</span></span>
<span data-ttu-id="47b5b-133">Az Iot Központi alkalmazáserőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="47b5b-133">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47b5b-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47b5b-134">-ResourceGroupName</span></span>
<span data-ttu-id="47b5b-135">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="47b5b-135">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47b5b-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47b5b-136">-ResourceId</span></span>
<span data-ttu-id="47b5b-137">Iot Central Application Resource Id.</span><span class="sxs-lookup"><span data-stu-id="47b5b-137">Iot Central Application Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47b5b-138">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="47b5b-138">-Sku</span></span>
<span data-ttu-id="47b5b-139">Az IoT Central-alkalmazások árazási rétege.</span><span class="sxs-lookup"><span data-stu-id="47b5b-139">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="47b5b-140">Az alapértelmezett érték az ST2.</span><span class="sxs-lookup"><span data-stu-id="47b5b-140">Default value is ST2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47b5b-141">-Subdomain</span><span class="sxs-lookup"><span data-stu-id="47b5b-141">-Subdomain</span></span>
<span data-ttu-id="47b5b-142">Az IoT központi alkalmazás altartománya.</span><span class="sxs-lookup"><span data-stu-id="47b5b-142">Subdomain of the IoT Central Application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47b5b-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="47b5b-143">-Tag</span></span>
<span data-ttu-id="47b5b-144">Iot Central Application Resource Tags.</span><span class="sxs-lookup"><span data-stu-id="47b5b-144">Iot Central Application Resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47b5b-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47b5b-145">-Confirm</span></span>
<span data-ttu-id="47b5b-146">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="47b5b-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47b5b-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47b5b-147">-WhatIf</span></span>
<span data-ttu-id="47b5b-148">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="47b5b-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47b5b-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="47b5b-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47b5b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47b5b-150">CommonParameters</span></span>
<span data-ttu-id="47b5b-151">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47b5b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47b5b-152">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47b5b-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47b5b-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="47b5b-153">INPUTS</span></span>

### <span data-ttu-id="47b5b-154">System.String</span><span class="sxs-lookup"><span data-stu-id="47b5b-154">System.String</span></span>

### <span data-ttu-id="47b5b-155">Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="47b5b-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="47b5b-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="47b5b-156">OUTPUTS</span></span>

### <span data-ttu-id="47b5b-157">Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="47b5b-157">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="47b5b-158">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="47b5b-158">NOTES</span></span>

## <span data-ttu-id="47b5b-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="47b5b-159">RELATED LINKS</span></span>
