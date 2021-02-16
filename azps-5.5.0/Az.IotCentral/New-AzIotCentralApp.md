---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/new-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
ms.openlocfilehash: 1be2aa8e198ae096f445b9f1972d1e0b903ae729
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154882"
---
# <span data-ttu-id="b8532-101">New-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="b8532-101">New-AzIotCentralApp</span></span>

## <span data-ttu-id="b8532-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8532-102">SYNOPSIS</span></span>
<span data-ttu-id="b8532-103">Létrehoz egy új, központi IoT-alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="b8532-103">Creates a new IoT Central Application.</span></span>

## <span data-ttu-id="b8532-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b8532-104">SYNTAX</span></span>

```
New-AzIotCentralApp [-Subdomain] <String> [-DisplayName <String>] [-Template <String>] [-Sku <String>]
 [-Location <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8532-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b8532-105">DESCRIPTION</span></span>
<span data-ttu-id="b8532-106">Létrehoz egy új, központi IoT-alkalmazást a megadott tulajdonságokkal és metaadatokkal.</span><span class="sxs-lookup"><span data-stu-id="b8532-106">Creates a new IoT Central Application with the provided properties and metadata.</span></span> <span data-ttu-id="b8532-107">Az IoT Central bemutatása: https://docs.microsoft.com/en-us/azure/iot-central/ .</span><span class="sxs-lookup"><span data-stu-id="b8532-107">For an introduction to IoT Central, see https://docs.microsoft.com/en-us/azure/iot-central/.</span></span>

## <span data-ttu-id="b8532-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b8532-108">EXAMPLES</span></span>

### <span data-ttu-id="b8532-109">1. példa: Egyszerű Központi IoT-alkalmazás létrehozása.</span><span class="sxs-lookup"><span data-stu-id="b8532-109">Example 1 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain"
```

<span data-ttu-id="b8532-110">Példakimenet:</span><span class="sxs-lookup"><span data-stu-id="b8532-110">Example Output:</span></span>

<span data-ttu-id="b8532-111">ResourceId: /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type: Microsoft.IoTCentral/IoTApps Location : westus Tag : Sku : Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: MyAppResourceName Subdomain: MyAppSubdomain Template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8532-111">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : MyAppResourceName Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="b8532-112">Hozzon létre egy Központi IoT-alkalmazást az ST2 standard árazási szintben, az erőforráscsoport régiójában.</span><span class="sxs-lookup"><span data-stu-id="b8532-112">Create an IoT Central application in the standard pricing tier ST2, in the region of the resource group.</span></span>

### <span data-ttu-id="b8532-113">2. példa: Egyszerű Központi IoT-alkalmazás létrehozása.</span><span class="sxs-lookup"><span data-stu-id="b8532-113">Example 2 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain" -Sku "ST2" -DisplayName "My Custom Display Name" -Template "iotc-default" -Location "westus"
```

<span data-ttu-id="b8532-114">Példakimenet:</span><span class="sxs-lookup"><span data-stu-id="b8532-114">Example Output:</span></span>

<span data-ttu-id="b8532-115">ResourceId: /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type: Microsoft.IoTCentral/IoTApps Location : westus Tag : Sku : Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My Custom Display Name Subdomain : MyAppSubdomain Template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXX ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8532-115">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="b8532-116">Hozzon létre egy Központi IoT-alkalmazást a "westus" régió st2 standard árazási szintjéhez, az iotc-alapértelmezett sablon alapján egy egyéni megjelenítendő névvel.</span><span class="sxs-lookup"><span data-stu-id="b8532-116">Create an IoT Central application with the standard pricing tier ST2 in the 'westus' region, with a custom display name, based on the iotc-default template.</span></span>

## <span data-ttu-id="b8532-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8532-117">PARAMETERS</span></span>

### <span data-ttu-id="b8532-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8532-118">-AsJob</span></span>
<span data-ttu-id="b8532-119">Futtassa a parancsmagot feladatként a háttérben.</span><span class="sxs-lookup"><span data-stu-id="b8532-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="b8532-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8532-120">-DefaultProfile</span></span>
<span data-ttu-id="b8532-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b8532-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8532-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b8532-122">-DisplayName</span></span>
<span data-ttu-id="b8532-123">Az IoT Central alkalmazás egyéni megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="b8532-123">Custom display name for the IoT Central application.</span></span>
<span data-ttu-id="b8532-124">Az alapértelmezett érték az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="b8532-124">Default is resource name.</span></span>

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

### <span data-ttu-id="b8532-125">-Location</span><span class="sxs-lookup"><span data-stu-id="b8532-125">-Location</span></span>
<span data-ttu-id="b8532-126">Az IoT Central alkalmazás helye.</span><span class="sxs-lookup"><span data-stu-id="b8532-126">Location of your IoT Central application.</span></span>
<span data-ttu-id="b8532-127">Az alapértelmezett érték a célerőforrás-csoport helye.</span><span class="sxs-lookup"><span data-stu-id="b8532-127">Default is the location of target resource group.</span></span>

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

### <span data-ttu-id="b8532-128">-Name</span><span class="sxs-lookup"><span data-stu-id="b8532-128">-Name</span></span>
<span data-ttu-id="b8532-129">Az Iot Központi alkalmazáserőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="b8532-129">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8532-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8532-130">-ResourceGroupName</span></span>
<span data-ttu-id="b8532-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b8532-131">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8532-132">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="b8532-132">-Sku</span></span>
<span data-ttu-id="b8532-133">Az IoT Central-alkalmazások árazási rétege.</span><span class="sxs-lookup"><span data-stu-id="b8532-133">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="b8532-134">Az alapértelmezett érték az ST2.</span><span class="sxs-lookup"><span data-stu-id="b8532-134">Default value is ST2.</span></span>

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

### <span data-ttu-id="b8532-135">-Subdomain</span><span class="sxs-lookup"><span data-stu-id="b8532-135">-Subdomain</span></span>
<span data-ttu-id="b8532-136">Subdomain for the IoT Central URL.</span><span class="sxs-lookup"><span data-stu-id="b8532-136">Subdomain for the IoT Central URL.</span></span>
<span data-ttu-id="b8532-137">Minden alkalmazásnak egyedi altartománysal kell rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="b8532-137">Each application must have a unique subdomain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8532-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="b8532-138">-Tag</span></span>
<span data-ttu-id="b8532-139">Iot Central Application Resource Tags.</span><span class="sxs-lookup"><span data-stu-id="b8532-139">Iot Central Application Resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8532-140">-Template</span><span class="sxs-lookup"><span data-stu-id="b8532-140">-Template</span></span>
<span data-ttu-id="b8532-141">IoT Central alkalmazássablon neve.</span><span class="sxs-lookup"><span data-stu-id="b8532-141">IoT Central application template name.</span></span>
<span data-ttu-id="b8532-142">Az alapértelmezett érték egy egyéni alkalmazás.</span><span class="sxs-lookup"><span data-stu-id="b8532-142">Default is a custom application.</span></span>

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

### <span data-ttu-id="b8532-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8532-143">-Confirm</span></span>
<span data-ttu-id="b8532-144">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b8532-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8532-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8532-145">-WhatIf</span></span>
<span data-ttu-id="b8532-146">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b8532-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8532-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b8532-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8532-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8532-148">CommonParameters</span></span>
<span data-ttu-id="b8532-149">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8532-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8532-150">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b8532-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8532-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b8532-151">INPUTS</span></span>

### <span data-ttu-id="b8532-152">System.String</span><span class="sxs-lookup"><span data-stu-id="b8532-152">System.String</span></span>

### <span data-ttu-id="b8532-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="b8532-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b8532-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8532-154">OUTPUTS</span></span>

### <span data-ttu-id="b8532-155">Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="b8532-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="b8532-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b8532-156">NOTES</span></span>

## <span data-ttu-id="b8532-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b8532-157">RELATED LINKS</span></span>
