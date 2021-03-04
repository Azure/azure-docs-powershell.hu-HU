---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/powershell/module/az.iotcentral/get-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
ms.openlocfilehash: 2d79857df255bb960c51b87c536013921f3b1c00
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942585"
---
# <span data-ttu-id="6783b-101">Get-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="6783b-101">Get-AzIotCentralApp</span></span>

## <span data-ttu-id="6783b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6783b-102">SYNOPSIS</span></span>
<span data-ttu-id="6783b-103">Tulajdonságokat kap egy vagy több Központi IoT-alkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="6783b-103">Gets properties for either one or several IoT Central Applications.</span></span>

## <span data-ttu-id="6783b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6783b-104">SYNTAX</span></span>

### <span data-ttu-id="6783b-105">ListIotCentralAppsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6783b-105">ListIotCentralAppsParameterSet (Default)</span></span>
```
Get-AzIotCentralApp [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6783b-106">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="6783b-106">InteractiveIotCentralParameterSet</span></span>
```
Get-AzIotCentralApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6783b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6783b-107">ResourceIdParameterSet</span></span>
```
Get-AzIotCentralApp -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6783b-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6783b-108">DESCRIPTION</span></span>
<span data-ttu-id="6783b-109">A paraméterkészlettől függően egy adott Központi IoT-alkalmazás vagy egy erőforráscsoport vagy előfizetés összes alkalmazásának metaadatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6783b-109">Gets the metadata for either a specific IoT Central Application, or all the applications in a Resource Group or Subscription, depending on Parameter Set.</span></span> 

## <span data-ttu-id="6783b-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6783b-110">EXAMPLES</span></span>

### <span data-ttu-id="6783b-111">1. példa adott IoT-központi alkalmazás lekérte.</span><span class="sxs-lookup"><span data-stu-id="6783b-111">Example 1 Get Specific IoT Central Application.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="6783b-112">A megadott Központi IoT-alkalmazás metaadatainak lekérte.</span><span class="sxs-lookup"><span data-stu-id="6783b-112">Gets the metadata for the specified IoT Central Application.</span></span>

<span data-ttu-id="6783b-113">Példakimenet:</span><span class="sxs-lookup"><span data-stu-id="6783b-113">Example Output:</span></span>

<span data-ttu-id="6783b-114">ResourceId: /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type: Microsoft.IoTCentral/IoTApps Location: westus Tag : {[key, val]} Sku: Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralAppskuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My Custom Display Name Subdomain : MyAppSubdomain Template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6783b-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="6783b-115">2. példa: Az IoT Central Applications lekérte az előfizetést.</span><span class="sxs-lookup"><span data-stu-id="6783b-115">Example 2 Get IoT Central Applications in Subscription.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp
```

<span data-ttu-id="6783b-116">Az aktuális előfizetés összes Központi IoT-alkalmazásának metaadatait beveszi.</span><span class="sxs-lookup"><span data-stu-id="6783b-116">Gets the metadata for all the IoT Central Applications in the current Subscription.</span></span>

<span data-ttu-id="6783b-117">Példakimenet:</span><span class="sxs-lookup"><span data-stu-id="6783b-117">Example Output:</span></span>

<span data-ttu-id="6783b-118">ResourceId: /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type: Microsoft.IoTCentral/IoTApps Location: westus Tag : {[key, val]} Sku: Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralAppskuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My Custom Display Name Subdomain : MyAppSubdomain Template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6783b-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="6783b-119">ResourceId: /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName2 Name: MyAppResourceName2 Type: Microsoft.IoTCentral/IoTApps Location: westus Tag : {[key, val]} Sku: Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralAppskuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My Custom Display Name 2 Subdomain : MyAppSubdomain2 Template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName2</span><span class="sxs-lookup"><span data-stu-id="6783b-119">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName2</span></span>

### <span data-ttu-id="6783b-120">3. példa a Központi IoT-alkalmazások lekérte az Erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="6783b-120">Example 3 Get IoT Central Applications in Resource Group.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName"
```

<span data-ttu-id="6783b-121">A megadott erőforráscsoportban található összes Központi IoT-alkalmazás metaadatait beveszi.</span><span class="sxs-lookup"><span data-stu-id="6783b-121">Gets the metadata for all IoT Central Applications in the provided Resource Group.</span></span>

<span data-ttu-id="6783b-122">Példakimenet:</span><span class="sxs-lookup"><span data-stu-id="6783b-122">Example Output:</span></span>

<span data-ttu-id="6783b-123">ResourceId: /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type: Microsoft.IoTCentral/IoTApps Location: westus Tag : {[key, val]} Sku: Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralAppskuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My Custom Display Name Subdomain : MyAppSubdomain Template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6783b-123">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="6783b-124">ResourceId: /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName2 Name: MyAppResourceName2 Type: Microsoft.IoTCentral/IoTApps Location: westus Tag : {[key, val]} Sku: Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralAppskuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My Custom Display Name 2 Subdomain : MyAppSubdomain2 Template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6783b-124">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="6783b-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6783b-125">PARAMETERS</span></span>

### <span data-ttu-id="6783b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6783b-126">-DefaultProfile</span></span>
<span data-ttu-id="6783b-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6783b-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6783b-128">-Name</span><span class="sxs-lookup"><span data-stu-id="6783b-128">-Name</span></span>
<span data-ttu-id="6783b-129">Az Iot Központi alkalmazáserőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="6783b-129">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="6783b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6783b-130">-ResourceGroupName</span></span>
<span data-ttu-id="6783b-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6783b-131">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: ListIotCentralAppsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="6783b-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6783b-132">-ResourceId</span></span>
<span data-ttu-id="6783b-133">Iot Central Application Resource Id.</span><span class="sxs-lookup"><span data-stu-id="6783b-133">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="6783b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6783b-134">CommonParameters</span></span>
<span data-ttu-id="6783b-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6783b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6783b-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6783b-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6783b-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6783b-137">INPUTS</span></span>

### <span data-ttu-id="6783b-138">System.String</span><span class="sxs-lookup"><span data-stu-id="6783b-138">System.String</span></span>

## <span data-ttu-id="6783b-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6783b-139">OUTPUTS</span></span>

### <span data-ttu-id="6783b-140">Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="6783b-140">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="6783b-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6783b-141">NOTES</span></span>

## <span data-ttu-id="6783b-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6783b-142">RELATED LINKS</span></span>
