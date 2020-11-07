---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/new-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
ms.openlocfilehash: af622bbbed98a897df1774303f1417723ebfb32c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845261"
---
# <span data-ttu-id="92dd1-101">New-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="92dd1-101">New-AzIotCentralApp</span></span>

## <span data-ttu-id="92dd1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="92dd1-102">SYNOPSIS</span></span>
<span data-ttu-id="92dd1-103">Új IoT-os központi alkalmazást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="92dd1-103">Creates a new IoT Central Application.</span></span>

## <span data-ttu-id="92dd1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="92dd1-104">SYNTAX</span></span>

```
New-AzIotCentralApp [-Subdomain] <String> [-DisplayName <String>] [-Template <String>] [-Sku <String>]
 [-Location <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92dd1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="92dd1-105">DESCRIPTION</span></span>
<span data-ttu-id="92dd1-106">Új IoT-Közép alkalmazást hoz létre a megadott tulajdonságokkal és metaadatokkal.</span><span class="sxs-lookup"><span data-stu-id="92dd1-106">Creates a new IoT Central Application with the provided properties and metadata.</span></span> <span data-ttu-id="92dd1-107">A IoT Central ismertetése a következő témakörben található: https://docs.microsoft.com/en-us/azure/iot-central/</span><span class="sxs-lookup"><span data-stu-id="92dd1-107">For an introduction to IoT Central, see https://docs.microsoft.com/en-us/azure/iot-central/.</span></span>

## <span data-ttu-id="92dd1-108">Példák</span><span class="sxs-lookup"><span data-stu-id="92dd1-108">EXAMPLES</span></span>

### <span data-ttu-id="92dd1-109">Példa 1 egyszerű IoT központi alkalmazás létrehozása</span><span class="sxs-lookup"><span data-stu-id="92dd1-109">Example 1 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain"
```

<span data-ttu-id="92dd1-110">Példa kimenet:</span><span class="sxs-lookup"><span data-stu-id="92dd1-110">Example Output:</span></span>

<span data-ttu-id="92dd1-111">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName név: MyAppResourceName típus: Microsoft. IoTCentral/IoTApps hely: westus címke: SKU: Microsoft. Azure. Command. IotCentral. models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX: MyAppResourceName altartomány: iotc-default@1.0.0 MyAppSubdomain: SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="92dd1-111">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : MyAppResourceName Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="92dd1-112">Hozzon létre egy IoT-os központi alkalmazást a standard árképzési szint ST2 az erőforráscsoport területén.</span><span class="sxs-lookup"><span data-stu-id="92dd1-112">Create an IoT Central application in the standard pricing tier ST2, in the region of the resource group.</span></span>

### <span data-ttu-id="92dd1-113">2. példa: egyszerű IoT központi alkalmazás létrehozása</span><span class="sxs-lookup"><span data-stu-id="92dd1-113">Example 2 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain" -Sku "ST2" -DisplayName "My Custom Display Name" -Template "iotc-default" -Location "westus"
```

<span data-ttu-id="92dd1-114">Példa kimenet:</span><span class="sxs-lookup"><span data-stu-id="92dd1-114">Example Output:</span></span>

<span data-ttu-id="92dd1-115">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName név: MyAppResourceName típus: Microsoft. IoTCentral/IoTApps hely: westus címke: SKU: Microsoft. Azure. Command. IotCentral. models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX: az egyéni megjelenítendő név altartománya: MyAppSubdomain sablon: SubscriptionId iotc-default@1.0.0 : XXXXXXXX-XXXX-XXXXXXXXXXXX</span><span class="sxs-lookup"><span data-stu-id="92dd1-115">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="92dd1-116">Hozzon létre egy IoT-os központi alkalmazást a szokásos árképzési szint ST2 az "westus" tartományban, egyéni megjelenítendő névvel az IOTC-default sablon alapján.</span><span class="sxs-lookup"><span data-stu-id="92dd1-116">Create an IoT Central application with the standard pricing tier ST2 in the 'westus' region, with a custom display name, based on the iotc-default template.</span></span>

## <span data-ttu-id="92dd1-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="92dd1-117">PARAMETERS</span></span>

### <span data-ttu-id="92dd1-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="92dd1-118">-AsJob</span></span>
<span data-ttu-id="92dd1-119">A parancsmagot feladatként futtathatja a háttérben.</span><span class="sxs-lookup"><span data-stu-id="92dd1-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="92dd1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92dd1-120">-DefaultProfile</span></span>
<span data-ttu-id="92dd1-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="92dd1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92dd1-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="92dd1-122">-DisplayName</span></span>
<span data-ttu-id="92dd1-123">Az IoT központi alkalmazás egyéni megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="92dd1-123">Custom display name for the IoT Central application.</span></span>
<span data-ttu-id="92dd1-124">Az alapértelmezett érték az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="92dd1-124">Default is resource name.</span></span>

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

### <span data-ttu-id="92dd1-125">-Hely</span><span class="sxs-lookup"><span data-stu-id="92dd1-125">-Location</span></span>
<span data-ttu-id="92dd1-126">A IoT központi alkalmazásának helye.</span><span class="sxs-lookup"><span data-stu-id="92dd1-126">Location of your IoT Central application.</span></span>
<span data-ttu-id="92dd1-127">Az alapértelmezett érték a cél erőforráscsoport helye.</span><span class="sxs-lookup"><span data-stu-id="92dd1-127">Default is the location of target resource group.</span></span>

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

### <span data-ttu-id="92dd1-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="92dd1-128">-Name</span></span>
<span data-ttu-id="92dd1-129">Az IOT központi alkalmazás-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="92dd1-129">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="92dd1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92dd1-130">-ResourceGroupName</span></span>
<span data-ttu-id="92dd1-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="92dd1-131">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="92dd1-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="92dd1-132">-Sku</span></span>
<span data-ttu-id="92dd1-133">Az IoT központi alkalmazásainak árazási szintje.</span><span class="sxs-lookup"><span data-stu-id="92dd1-133">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="92dd1-134">Az alapértelmezett érték a ST2.</span><span class="sxs-lookup"><span data-stu-id="92dd1-134">Default value is ST2.</span></span>

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

### <span data-ttu-id="92dd1-135">-Aldomain</span><span class="sxs-lookup"><span data-stu-id="92dd1-135">-Subdomain</span></span>
<span data-ttu-id="92dd1-136">Az IoT központi URL-címének altartománya.</span><span class="sxs-lookup"><span data-stu-id="92dd1-136">Subdomain for the IoT Central URL.</span></span>
<span data-ttu-id="92dd1-137">Minden alkalmazásnak egyedi altartománnyal kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="92dd1-137">Each application must have a unique subdomain.</span></span>

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

### <span data-ttu-id="92dd1-138">-Címke</span><span class="sxs-lookup"><span data-stu-id="92dd1-138">-Tag</span></span>
<span data-ttu-id="92dd1-139">IOT központi alkalmazás-erőforrás címkéi</span><span class="sxs-lookup"><span data-stu-id="92dd1-139">Iot Central Application Resource Tags.</span></span>

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

### <span data-ttu-id="92dd1-140">-Sablon</span><span class="sxs-lookup"><span data-stu-id="92dd1-140">-Template</span></span>
<span data-ttu-id="92dd1-141">Az IoT központi alkalmazásspecifikus sablon neve</span><span class="sxs-lookup"><span data-stu-id="92dd1-141">IoT Central application template name.</span></span>
<span data-ttu-id="92dd1-142">Az alapértelmezett beállítás egy egyéni alkalmazás.</span><span class="sxs-lookup"><span data-stu-id="92dd1-142">Default is a custom application.</span></span>

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

### <span data-ttu-id="92dd1-143">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="92dd1-143">-Confirm</span></span>
<span data-ttu-id="92dd1-144">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="92dd1-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92dd1-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92dd1-145">-WhatIf</span></span>
<span data-ttu-id="92dd1-146">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="92dd1-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92dd1-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="92dd1-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92dd1-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92dd1-148">CommonParameters</span></span>
<span data-ttu-id="92dd1-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="92dd1-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92dd1-150">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92dd1-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92dd1-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="92dd1-151">INPUTS</span></span>

### <span data-ttu-id="92dd1-152">System. String</span><span class="sxs-lookup"><span data-stu-id="92dd1-152">System.String</span></span>

### <span data-ttu-id="92dd1-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="92dd1-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="92dd1-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="92dd1-154">OUTPUTS</span></span>

### <span data-ttu-id="92dd1-155">Microsoft. Azure. Command. IotCentral. models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="92dd1-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="92dd1-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="92dd1-156">NOTES</span></span>

## <span data-ttu-id="92dd1-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="92dd1-157">RELATED LINKS</span></span>
