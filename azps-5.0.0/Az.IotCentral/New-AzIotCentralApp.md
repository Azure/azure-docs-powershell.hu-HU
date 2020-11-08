---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/new-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
ms.openlocfilehash: 1be2aa8e198ae096f445b9f1972d1e0b903ae729
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187796"
---
# <span data-ttu-id="805ae-101">New-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="805ae-101">New-AzIotCentralApp</span></span>

## <span data-ttu-id="805ae-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="805ae-102">SYNOPSIS</span></span>
<span data-ttu-id="805ae-103">Új IoT-os központi alkalmazást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="805ae-103">Creates a new IoT Central Application.</span></span>

## <span data-ttu-id="805ae-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="805ae-104">SYNTAX</span></span>

```
New-AzIotCentralApp [-Subdomain] <String> [-DisplayName <String>] [-Template <String>] [-Sku <String>]
 [-Location <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="805ae-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="805ae-105">DESCRIPTION</span></span>
<span data-ttu-id="805ae-106">Új IoT-Közép alkalmazást hoz létre a megadott tulajdonságokkal és metaadatokkal.</span><span class="sxs-lookup"><span data-stu-id="805ae-106">Creates a new IoT Central Application with the provided properties and metadata.</span></span> <span data-ttu-id="805ae-107">A IoT Central ismertetése a következő témakörben található: https://docs.microsoft.com/en-us/azure/iot-central/</span><span class="sxs-lookup"><span data-stu-id="805ae-107">For an introduction to IoT Central, see https://docs.microsoft.com/en-us/azure/iot-central/.</span></span>

## <span data-ttu-id="805ae-108">Példák</span><span class="sxs-lookup"><span data-stu-id="805ae-108">EXAMPLES</span></span>

### <span data-ttu-id="805ae-109">Példa 1 egyszerű IoT központi alkalmazás létrehozása</span><span class="sxs-lookup"><span data-stu-id="805ae-109">Example 1 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain"
```

<span data-ttu-id="805ae-110">Példa kimenet:</span><span class="sxs-lookup"><span data-stu-id="805ae-110">Example Output:</span></span>

<span data-ttu-id="805ae-111">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName név: MyAppResourceName típus: Microsoft. IoTCentral/IoTApps hely: westus címke: SKU: Microsoft. Azure. Command. IotCentral. models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX: MyAppResourceName altartomány: iotc-default@1.0.0 MyAppSubdomain: SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="805ae-111">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : MyAppResourceName Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="805ae-112">Hozzon létre egy IoT-os központi alkalmazást a standard árképzési szint ST2 az erőforráscsoport területén.</span><span class="sxs-lookup"><span data-stu-id="805ae-112">Create an IoT Central application in the standard pricing tier ST2, in the region of the resource group.</span></span>

### <span data-ttu-id="805ae-113">2. példa: egyszerű IoT központi alkalmazás létrehozása</span><span class="sxs-lookup"><span data-stu-id="805ae-113">Example 2 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain" -Sku "ST2" -DisplayName "My Custom Display Name" -Template "iotc-default" -Location "westus"
```

<span data-ttu-id="805ae-114">Példa kimenet:</span><span class="sxs-lookup"><span data-stu-id="805ae-114">Example Output:</span></span>

<span data-ttu-id="805ae-115">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName név: MyAppResourceName típus: Microsoft. IoTCentral/IoTApps hely: westus címke: SKU: Microsoft. Azure. Command. IotCentral. models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX: az egyéni megjelenítendő név altartománya: MyAppSubdomain sablon: SubscriptionId iotc-default@1.0.0 : XXXXXXXX-XXXX-XXXXXXXXXXXX</span><span class="sxs-lookup"><span data-stu-id="805ae-115">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="805ae-116">Hozzon létre egy IoT-os központi alkalmazást a szokásos árképzési szint ST2 az "westus" tartományban, egyéni megjelenítendő névvel az IOTC-default sablon alapján.</span><span class="sxs-lookup"><span data-stu-id="805ae-116">Create an IoT Central application with the standard pricing tier ST2 in the 'westus' region, with a custom display name, based on the iotc-default template.</span></span>

## <span data-ttu-id="805ae-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="805ae-117">PARAMETERS</span></span>

### <span data-ttu-id="805ae-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="805ae-118">-AsJob</span></span>
<span data-ttu-id="805ae-119">A parancsmagot feladatként futtathatja a háttérben.</span><span class="sxs-lookup"><span data-stu-id="805ae-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="805ae-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="805ae-120">-DefaultProfile</span></span>
<span data-ttu-id="805ae-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="805ae-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="805ae-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="805ae-122">-DisplayName</span></span>
<span data-ttu-id="805ae-123">Az IoT központi alkalmazás egyéni megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="805ae-123">Custom display name for the IoT Central application.</span></span>
<span data-ttu-id="805ae-124">Az alapértelmezett érték az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="805ae-124">Default is resource name.</span></span>

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

### <span data-ttu-id="805ae-125">-Hely</span><span class="sxs-lookup"><span data-stu-id="805ae-125">-Location</span></span>
<span data-ttu-id="805ae-126">A IoT központi alkalmazásának helye.</span><span class="sxs-lookup"><span data-stu-id="805ae-126">Location of your IoT Central application.</span></span>
<span data-ttu-id="805ae-127">Az alapértelmezett érték a cél erőforráscsoport helye.</span><span class="sxs-lookup"><span data-stu-id="805ae-127">Default is the location of target resource group.</span></span>

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

### <span data-ttu-id="805ae-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="805ae-128">-Name</span></span>
<span data-ttu-id="805ae-129">Az IOT központi alkalmazás-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="805ae-129">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="805ae-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="805ae-130">-ResourceGroupName</span></span>
<span data-ttu-id="805ae-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="805ae-131">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="805ae-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="805ae-132">-Sku</span></span>
<span data-ttu-id="805ae-133">Az IoT központi alkalmazásainak árazási szintje.</span><span class="sxs-lookup"><span data-stu-id="805ae-133">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="805ae-134">Az alapértelmezett érték a ST2.</span><span class="sxs-lookup"><span data-stu-id="805ae-134">Default value is ST2.</span></span>

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

### <span data-ttu-id="805ae-135">-Aldomain</span><span class="sxs-lookup"><span data-stu-id="805ae-135">-Subdomain</span></span>
<span data-ttu-id="805ae-136">Az IoT központi URL-címének altartománya.</span><span class="sxs-lookup"><span data-stu-id="805ae-136">Subdomain for the IoT Central URL.</span></span>
<span data-ttu-id="805ae-137">Minden alkalmazásnak egyedi altartománnyal kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="805ae-137">Each application must have a unique subdomain.</span></span>

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

### <span data-ttu-id="805ae-138">-Címke</span><span class="sxs-lookup"><span data-stu-id="805ae-138">-Tag</span></span>
<span data-ttu-id="805ae-139">IOT központi alkalmazás-erőforrás címkéi</span><span class="sxs-lookup"><span data-stu-id="805ae-139">Iot Central Application Resource Tags.</span></span>

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

### <span data-ttu-id="805ae-140">-Sablon</span><span class="sxs-lookup"><span data-stu-id="805ae-140">-Template</span></span>
<span data-ttu-id="805ae-141">Az IoT központi alkalmazásspecifikus sablon neve</span><span class="sxs-lookup"><span data-stu-id="805ae-141">IoT Central application template name.</span></span>
<span data-ttu-id="805ae-142">Az alapértelmezett beállítás egy egyéni alkalmazás.</span><span class="sxs-lookup"><span data-stu-id="805ae-142">Default is a custom application.</span></span>

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

### <span data-ttu-id="805ae-143">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="805ae-143">-Confirm</span></span>
<span data-ttu-id="805ae-144">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="805ae-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="805ae-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="805ae-145">-WhatIf</span></span>
<span data-ttu-id="805ae-146">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="805ae-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="805ae-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="805ae-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="805ae-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="805ae-148">CommonParameters</span></span>
<span data-ttu-id="805ae-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="805ae-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="805ae-150">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="805ae-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="805ae-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="805ae-151">INPUTS</span></span>

### <span data-ttu-id="805ae-152">System. String</span><span class="sxs-lookup"><span data-stu-id="805ae-152">System.String</span></span>

### <span data-ttu-id="805ae-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="805ae-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="805ae-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="805ae-154">OUTPUTS</span></span>

### <span data-ttu-id="805ae-155">Microsoft. Azure. Command. IotCentral. models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="805ae-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="805ae-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="805ae-156">NOTES</span></span>

## <span data-ttu-id="805ae-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="805ae-157">RELATED LINKS</span></span>
