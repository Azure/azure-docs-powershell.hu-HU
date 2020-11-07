---
external help file: Microsoft.Azure.Commands.IotCentral.dll-Help.xml
Module Name: AzureRM.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iotcentral/get-azurermiotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Get-AzureRmIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Get-AzureRmIotCentralApp.md
ms.openlocfilehash: fdf674b5ec2dfcefe8fcada92cfaf0fd1073f7f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680665"
---
# <span data-ttu-id="e7e5a-101">Get-AzureRmIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="e7e5a-101">Get-AzureRmIotCentralApp</span></span>

## <span data-ttu-id="e7e5a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e7e5a-102">SYNOPSIS</span></span>
<span data-ttu-id="e7e5a-103">Egy vagy több IoT-alapú központi alkalmazás tulajdonságait kapja.</span><span class="sxs-lookup"><span data-stu-id="e7e5a-103">Gets properties for either one or several IoT Central Applications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7e5a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e7e5a-104">SYNTAX</span></span>

### <span data-ttu-id="e7e5a-105">ListIotCentralAppsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e7e5a-105">ListIotCentralAppsParameterSet (Default)</span></span>
```
Get-AzureRmIotCentralApp [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e7e5a-106">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7e5a-106">InteractiveIotCentralParameterSet</span></span>
```
Get-AzureRmIotCentralApp [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7e5a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7e5a-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmIotCentralApp -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7e5a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e7e5a-108">DESCRIPTION</span></span>
<span data-ttu-id="e7e5a-109">Egy adott IoT központi alkalmazás metaadatait vagy egy erőforráscsoport vagy-előfizetés összes alkalmazását kapja meg, a beállított paramétertől függően.</span><span class="sxs-lookup"><span data-stu-id="e7e5a-109">Gets the metadata for either a specific IoT Central Application, or all the applications in a Resource Group or Subscription, depending on Parameter Set.</span></span> 

## <span data-ttu-id="e7e5a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e7e5a-110">EXAMPLES</span></span>

### <span data-ttu-id="e7e5a-111">1. példa: adott IoT központi alkalmazás beolvasása</span><span class="sxs-lookup"><span data-stu-id="e7e5a-111">Example 1 Get Specific IoT Central Application.</span></span>
```powershell
PS C:\> Get-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="e7e5a-112">A megadott IoT központi alkalmazás metaadatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e7e5a-112">Gets the metadata for the specified IoT Central Application.</span></span>

<span data-ttu-id="e7e5a-113">Példa kimenet:</span><span class="sxs-lookup"><span data-stu-id="e7e5a-113">Example Output:</span></span>

<span data-ttu-id="e7e5a-114">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName név: MyAppResourceName típus: Microsoft. IoTCentral/IoTApps hely: westus címke: {[kulcs, val]} SKU: Microsoft. Azure. Command. IotCentral. models. PSIotCentralAppSkuInfo. ApplicationId. XXXXXXXXXXXX: XXXXXXXX-XXXX-XXXX-XXXX-MYAPPSUBDOMAIN DisplayName: az egyéni megjelenítendő név altartománya: SubscriptionId sablon: XXXXXXXXXXXX iotc-default@1.0.0 : XXXXXXXX-XXXX-ResourceGroupName MyResourceGroupName:</span><span class="sxs-lookup"><span data-stu-id="e7e5a-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="e7e5a-115">2. példa: a IoT központi alkalmazásainak beszerzése az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="e7e5a-115">Example 2 Get IoT Central Applications in Subscription.</span></span>
```powershell
PS C:\> Get-AzureRmIotCentralApp
```

<span data-ttu-id="e7e5a-116">A jelenlegi előfizetésben az összes IoT központi alkalmazás metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="e7e5a-116">Gets the metadata for all the IoT Central Applications in the current Subscription.</span></span>

<span data-ttu-id="e7e5a-117">Példa kimenet:</span><span class="sxs-lookup"><span data-stu-id="e7e5a-117">Example Output:</span></span>

<span data-ttu-id="e7e5a-118">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName név: MyAppResourceName típus: Microsoft. IoTCentral/IoTApps hely: westus címke: {[kulcs, val]} SKU: Microsoft. Azure. Command. IotCentral. models. PSIotCentralAppSkuInfo. ApplicationId. XXXXXXXXXXXX: XXXXXXXX-XXXX-XXXX-XXXX-MYAPPSUBDOMAIN DisplayName: az egyéni megjelenítendő név altartománya: SubscriptionId sablon: XXXXXXXXXXXX iotc-default@1.0.0 : XXXXXXXX-XXXX-ResourceGroupName MyResourceGroupName:</span><span class="sxs-lookup"><span data-stu-id="e7e5a-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="e7e5a-119">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2 név: MyAppResourceName2 típus: Microsoft. IoTCentral/IoTApps hely: westus címke: {[kulcs, val]} SKU: Microsoft. Azure. Command. IotCentral. models. PSIotCentralAppSkuInfo. ApplicationId. XXXXXXXXXXXX: XXXXXXXX-XXXX-XXXX-XXXX-MYAPPSUBDOMAIN2 DisplayName: az egyéni megjelenítendő név 2 aldomain: SubscriptionId sablon: XXXXXXXXXXXX: XXXXXXXX-XXXX- iotc-default@1.0.0 ResourceGroupName MyResourceGroupName2:</span><span class="sxs-lookup"><span data-stu-id="e7e5a-119">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName2</span></span>

### <span data-ttu-id="e7e5a-120">3 Példa: a IoT központi alkalmazásai beolvasása az erőforráscsoport-ban</span><span class="sxs-lookup"><span data-stu-id="e7e5a-120">Example 3 Get IoT Central Applications in Resource Group.</span></span>
```powershell
PS C:\> Get-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName"
```

<span data-ttu-id="e7e5a-121">A megadott erőforráscsoport összes IoT-alkalmazásának metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="e7e5a-121">Gets the metadata for all IoT Central Applications in the provided Resource Group.</span></span>

<span data-ttu-id="e7e5a-122">Példa kimenet:</span><span class="sxs-lookup"><span data-stu-id="e7e5a-122">Example Output:</span></span>

<span data-ttu-id="e7e5a-123">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName név: MyAppResourceName típus: Microsoft. IoTCentral/IoTApps hely: westus címke: {[kulcs, val]} SKU: Microsoft. Azure. Command. IotCentral. models. PSIotCentralAppSkuInfo. ApplicationId. XXXXXXXXXXXX: XXXXXXXX-XXXX-XXXX-XXXX-MYAPPSUBDOMAIN DisplayName: az egyéni megjelenítendő név altartománya: SubscriptionId sablon: XXXXXXXXXXXX iotc-default@1.0.0 : XXXXXXXX-XXXX-ResourceGroupName MyResourceGroupName:</span><span class="sxs-lookup"><span data-stu-id="e7e5a-123">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="e7e5a-124">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2 név: MyAppResourceName2 típus: Microsoft. IoTCentral/IoTApps hely: westus címke: {[kulcs, val]} SKU: Microsoft. Azure. Command. IotCentral. models. PSIotCentralAppSkuInfo. ApplicationId. XXXXXXXXXXXX: XXXXXXXX-XXXX-XXXX-XXXX-MYAPPSUBDOMAIN2 DisplayName: az egyéni megjelenítendő név 2 aldomain: SubscriptionId sablon: XXXXXXXXXXXX: XXXXXXXX-XXXX- iotc-default@1.0.0 ResourceGroupName MyResourceGroupName:</span><span class="sxs-lookup"><span data-stu-id="e7e5a-124">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="e7e5a-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e7e5a-125">PARAMETERS</span></span>

### <span data-ttu-id="e7e5a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7e5a-126">-DefaultProfile</span></span>
<span data-ttu-id="e7e5a-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e7e5a-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7e5a-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e7e5a-128">-Name</span></span>
<span data-ttu-id="e7e5a-129">Az IOT központi alkalmazás-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="e7e5a-129">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7e5a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7e5a-130">-ResourceGroupName</span></span>
<span data-ttu-id="e7e5a-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e7e5a-131">Name of the Resource Group.</span></span>

```yaml
Type: String
Parameter Sets: ListIotCentralAppsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7e5a-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7e5a-132">-ResourceId</span></span>
<span data-ttu-id="e7e5a-133">IOT központi alkalmazás-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="e7e5a-133">Iot Central Application Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7e5a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7e5a-134">CommonParameters</span></span>
<span data-ttu-id="e7e5a-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e7e5a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7e5a-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7e5a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7e5a-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7e5a-137">INPUTS</span></span>

### <span data-ttu-id="e7e5a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e7e5a-138">System.String</span></span>
## <span data-ttu-id="e7e5a-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7e5a-139">OUTPUTS</span></span>

### <span data-ttu-id="e7e5a-140">Microsoft. Azure. Command. IotCentral. models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="e7e5a-140">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>
## <span data-ttu-id="e7e5a-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e7e5a-141">NOTES</span></span>

## <span data-ttu-id="e7e5a-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e7e5a-142">RELATED LINKS</span></span>
