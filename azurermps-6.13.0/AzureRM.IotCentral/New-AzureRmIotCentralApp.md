---
external help file: Microsoft.Azure.Commands.IotCentral.dll-Help.xml
Module Name: AzureRM.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iotcentral/new-azurermiotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/New-AzureRmIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/New-AzureRmIotCentralApp.md
ms.openlocfilehash: d0bb10324c1a97b6228a26a7ab079edb4845d48a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505380"
---
# <span data-ttu-id="17816-101">New-AzureRmIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="17816-101">New-AzureRmIotCentralApp</span></span>

## <span data-ttu-id="17816-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="17816-102">SYNOPSIS</span></span>
<span data-ttu-id="17816-103">Új IoT-os központi alkalmazást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="17816-103">Creates a new IoT Central Application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17816-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="17816-104">SYNTAX</span></span>

```
New-AzureRmIotCentralApp [-Subdomain] <String> [-DisplayName <String>] [-Template <String>] [-Sku <String>]
 [-Location <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17816-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="17816-105">DESCRIPTION</span></span>
<span data-ttu-id="17816-106">Új IoT-Közép alkalmazást hoz létre a megadott tulajdonságokkal és metaadatokkal.</span><span class="sxs-lookup"><span data-stu-id="17816-106">Creates a new IoT Central Application with the provided properties and metadata.</span></span> <span data-ttu-id="17816-107">A IoT Central ismertetése a következő témakörben található: https://docs.microsoft.com/en-us/azure/iot-central/</span><span class="sxs-lookup"><span data-stu-id="17816-107">For an introduction to IoT Central, see https://docs.microsoft.com/en-us/azure/iot-central/.</span></span>

## <span data-ttu-id="17816-108">Példák</span><span class="sxs-lookup"><span data-stu-id="17816-108">EXAMPLES</span></span>

### <span data-ttu-id="17816-109">Példa 1 egyszerű IoT központi alkalmazás létrehozása</span><span class="sxs-lookup"><span data-stu-id="17816-109">Example 1 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain"
```

<span data-ttu-id="17816-110">Példa kimenet:</span><span class="sxs-lookup"><span data-stu-id="17816-110">Example Output:</span></span>

<span data-ttu-id="17816-111">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName név: MyAppResourceName típus: Microsoft. IoTCentral/IoTApps hely: westus címke: SKU: Microsoft. Azure. Command. IotCentral. models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX: MyAppResourceName altartomány: iotc-default@1.0.0 MyAppSubdomain: SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="17816-111">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : MyAppResourceName Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="17816-112">Hozzon létre egy IoT központi alkalmazást az S1 standard árképzési rétegben, az erőforráscsoport területén.</span><span class="sxs-lookup"><span data-stu-id="17816-112">Create an IoT Central application in the standard pricing tier S1, in the region of the resource group.</span></span>

### <span data-ttu-id="17816-113">2. példa: egyszerű IoT központi alkalmazás létrehozása</span><span class="sxs-lookup"><span data-stu-id="17816-113">Example 2 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain" -Sku "S1" -DisplayName "My Custom Display Name" -Template "iotc-default" -Location "westus"
```

<span data-ttu-id="17816-114">Példa kimenet:</span><span class="sxs-lookup"><span data-stu-id="17816-114">Example Output:</span></span>

<span data-ttu-id="17816-115">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName név: MyAppResourceName típus: Microsoft. IoTCentral/IoTApps hely: westus címke: SKU: Microsoft. Azure. Command. IotCentral. models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX: az egyéni megjelenítendő név altartománya: MyAppSubdomain sablon: SubscriptionId iotc-default@1.0.0 : XXXXXXXX-XXXX-XXXXXXXXXXXX</span><span class="sxs-lookup"><span data-stu-id="17816-115">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="17816-116">Hozzon létre egy IoT-alapú központi alkalmazást az "westus" régióban az S1-es standard árképzési szinttel, az IOTC-default sablon alapján az egyéni megjelenítendő névvel.</span><span class="sxs-lookup"><span data-stu-id="17816-116">Create an IoT Central application with the standard pricing tier S1 in the 'westus' region, with a custom display name, based on the iotc-default template.</span></span>

## <span data-ttu-id="17816-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="17816-117">PARAMETERS</span></span>

### <span data-ttu-id="17816-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="17816-118">-AsJob</span></span>
<span data-ttu-id="17816-119">A parancsmagot feladatként futtathatja a háttérben.</span><span class="sxs-lookup"><span data-stu-id="17816-119">Run cmdlet as a job in the background.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17816-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17816-120">-DefaultProfile</span></span>
<span data-ttu-id="17816-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="17816-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17816-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="17816-122">-DisplayName</span></span>
<span data-ttu-id="17816-123">Az IoT központi alkalmazás egyéni megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="17816-123">Custom display name for the IoT Central application.</span></span>
<span data-ttu-id="17816-124">Az alapértelmezett érték az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="17816-124">Default is resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17816-125">-Hely</span><span class="sxs-lookup"><span data-stu-id="17816-125">-Location</span></span>
<span data-ttu-id="17816-126">A IoT központi alkalmazásának helye.</span><span class="sxs-lookup"><span data-stu-id="17816-126">Location of your IoT Central application.</span></span>
<span data-ttu-id="17816-127">Az alapértelmezett érték a cél erőforráscsoport helye.</span><span class="sxs-lookup"><span data-stu-id="17816-127">Default is the location of target resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17816-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="17816-128">-Name</span></span>
<span data-ttu-id="17816-129">Az IOT központi alkalmazás-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="17816-129">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17816-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17816-130">-ResourceGroupName</span></span>
<span data-ttu-id="17816-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="17816-131">Name of the Resource Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17816-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="17816-132">-Sku</span></span>
<span data-ttu-id="17816-133">Az IoT központi alkalmazásainak árazási szintje.</span><span class="sxs-lookup"><span data-stu-id="17816-133">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="17816-134">Az alapértelmezett érték az S1.</span><span class="sxs-lookup"><span data-stu-id="17816-134">Default value is S1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: S1

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17816-135">-Aldomain</span><span class="sxs-lookup"><span data-stu-id="17816-135">-Subdomain</span></span>
<span data-ttu-id="17816-136">Az IoT központi URL-címének altartománya.</span><span class="sxs-lookup"><span data-stu-id="17816-136">Subdomain for the IoT Central URL.</span></span>
<span data-ttu-id="17816-137">Minden alkalmazásnak egyedi altartománnyal kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="17816-137">Each application must have a unique subdomain.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17816-138">-Címke</span><span class="sxs-lookup"><span data-stu-id="17816-138">-Tag</span></span>
<span data-ttu-id="17816-139">IOT központi alkalmazás-erőforrás címkéi</span><span class="sxs-lookup"><span data-stu-id="17816-139">Iot Central Application Resource Tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17816-140">-Sablon</span><span class="sxs-lookup"><span data-stu-id="17816-140">-Template</span></span>
<span data-ttu-id="17816-141">Az IoT központi alkalmazásspecifikus sablon neve</span><span class="sxs-lookup"><span data-stu-id="17816-141">IoT Central application template name.</span></span>
<span data-ttu-id="17816-142">Az alapértelmezett beállítás egy egyéni alkalmazás.</span><span class="sxs-lookup"><span data-stu-id="17816-142">Default is a custom application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17816-143">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="17816-143">-Confirm</span></span>
<span data-ttu-id="17816-144">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="17816-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17816-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17816-145">-WhatIf</span></span>
<span data-ttu-id="17816-146">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="17816-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17816-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="17816-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17816-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17816-148">CommonParameters</span></span>
<span data-ttu-id="17816-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="17816-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17816-150">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17816-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17816-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="17816-151">INPUTS</span></span>

### <span data-ttu-id="17816-152">System. String</span><span class="sxs-lookup"><span data-stu-id="17816-152">System.String</span></span>
### <span data-ttu-id="17816-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="17816-153">System.Collections.Hashtable</span></span>
## <span data-ttu-id="17816-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="17816-154">OUTPUTS</span></span>

### <span data-ttu-id="17816-155">Microsoft. Azure. Command. IotCentral. models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="17816-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>
## <span data-ttu-id="17816-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="17816-156">NOTES</span></span>

## <span data-ttu-id="17816-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="17816-157">RELATED LINKS</span></span>
