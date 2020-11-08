---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/get-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
ms.openlocfilehash: cbc7e255f74943ea2aff3518d278035f72394235
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187798"
---
# <span data-ttu-id="d1e29-101">Get-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="d1e29-101">Get-AzIotCentralApp</span></span>

## <span data-ttu-id="d1e29-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d1e29-102">SYNOPSIS</span></span>
<span data-ttu-id="d1e29-103">Egy vagy több IoT-alapú központi alkalmazás tulajdonságait kapja.</span><span class="sxs-lookup"><span data-stu-id="d1e29-103">Gets properties for either one or several IoT Central Applications.</span></span>

## <span data-ttu-id="d1e29-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d1e29-104">SYNTAX</span></span>

### <span data-ttu-id="d1e29-105">ListIotCentralAppsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d1e29-105">ListIotCentralAppsParameterSet (Default)</span></span>
```
Get-AzIotCentralApp [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d1e29-106">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1e29-106">InteractiveIotCentralParameterSet</span></span>
```
Get-AzIotCentralApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d1e29-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1e29-107">ResourceIdParameterSet</span></span>
```
Get-AzIotCentralApp -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1e29-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d1e29-108">DESCRIPTION</span></span>
<span data-ttu-id="d1e29-109">Egy adott IoT központi alkalmazás metaadatait vagy egy erőforráscsoport vagy-előfizetés összes alkalmazását kapja meg, a beállított paramétertől függően.</span><span class="sxs-lookup"><span data-stu-id="d1e29-109">Gets the metadata for either a specific IoT Central Application, or all the applications in a Resource Group or Subscription, depending on Parameter Set.</span></span> 

## <span data-ttu-id="d1e29-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d1e29-110">EXAMPLES</span></span>

### <span data-ttu-id="d1e29-111">1. példa: adott IoT központi alkalmazás beolvasása</span><span class="sxs-lookup"><span data-stu-id="d1e29-111">Example 1 Get Specific IoT Central Application.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="d1e29-112">A megadott IoT központi alkalmazás metaadatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d1e29-112">Gets the metadata for the specified IoT Central Application.</span></span>

<span data-ttu-id="d1e29-113">Példa kimenet:</span><span class="sxs-lookup"><span data-stu-id="d1e29-113">Example Output:</span></span>

<span data-ttu-id="d1e29-114">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName név: MyAppResourceName típus: Microsoft. IoTCentral/IoTApps hely: westus címke: {[kulcs, val]} SKU: Microsoft. Azure. Command. IotCentral. models. PSIotCentralAppSkuInfo. ApplicationId. XXXXXXXXXXXX: XXXXXXXX-XXXX-XXXX-XXXX-MYAPPSUBDOMAIN DisplayName: az egyéni megjelenítendő név altartománya: SubscriptionId sablon: XXXXXXXXXXXX iotc-default@1.0.0 : XXXXXXXX-XXXX-ResourceGroupName MyResourceGroupName:</span><span class="sxs-lookup"><span data-stu-id="d1e29-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="d1e29-115">2. példa: a IoT központi alkalmazásainak beszerzése az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="d1e29-115">Example 2 Get IoT Central Applications in Subscription.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp
```

<span data-ttu-id="d1e29-116">A jelenlegi előfizetésben az összes IoT központi alkalmazás metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="d1e29-116">Gets the metadata for all the IoT Central Applications in the current Subscription.</span></span>

<span data-ttu-id="d1e29-117">Példa kimenet:</span><span class="sxs-lookup"><span data-stu-id="d1e29-117">Example Output:</span></span>

<span data-ttu-id="d1e29-118">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName név: MyAppResourceName típus: Microsoft. IoTCentral/IoTApps hely: westus címke: {[kulcs, val]} SKU: Microsoft. Azure. Command. IotCentral. models. PSIotCentralAppSkuInfo. ApplicationId. XXXXXXXXXXXX: XXXXXXXX-XXXX-XXXX-XXXX-MYAPPSUBDOMAIN DisplayName: az egyéni megjelenítendő név altartománya: SubscriptionId sablon: XXXXXXXXXXXX iotc-default@1.0.0 : XXXXXXXX-XXXX-ResourceGroupName MyResourceGroupName:</span><span class="sxs-lookup"><span data-stu-id="d1e29-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="d1e29-119">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2 név: MyAppResourceName2 típus: Microsoft. IoTCentral/IoTApps hely: westus címke: {[kulcs, val]} SKU: Microsoft. Azure. Command. IotCentral. models. PSIotCentralAppSkuInfo. ApplicationId. XXXXXXXXXXXX: XXXXXXXX-XXXX-XXXX-XXXX-MYAPPSUBDOMAIN2 DisplayName: az egyéni megjelenítendő név 2 aldomain: SubscriptionId sablon: XXXXXXXXXXXX: XXXXXXXX-XXXX- iotc-default@1.0.0 ResourceGroupName MyResourceGroupName2:</span><span class="sxs-lookup"><span data-stu-id="d1e29-119">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName2</span></span>

### <span data-ttu-id="d1e29-120">3 Példa: a IoT központi alkalmazásai beolvasása az erőforráscsoport-ban</span><span class="sxs-lookup"><span data-stu-id="d1e29-120">Example 3 Get IoT Central Applications in Resource Group.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName"
```

<span data-ttu-id="d1e29-121">A megadott erőforráscsoport összes IoT-alkalmazásának metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="d1e29-121">Gets the metadata for all IoT Central Applications in the provided Resource Group.</span></span>

<span data-ttu-id="d1e29-122">Példa kimenet:</span><span class="sxs-lookup"><span data-stu-id="d1e29-122">Example Output:</span></span>

<span data-ttu-id="d1e29-123">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName név: MyAppResourceName típus: Microsoft. IoTCentral/IoTApps hely: westus címke: {[kulcs, val]} SKU: Microsoft. Azure. Command. IotCentral. models. PSIotCentralAppSkuInfo. ApplicationId. XXXXXXXXXXXX: XXXXXXXX-XXXX-XXXX-XXXX-MYAPPSUBDOMAIN DisplayName: az egyéni megjelenítendő név altartománya: SubscriptionId sablon: XXXXXXXXXXXX iotc-default@1.0.0 : XXXXXXXX-XXXX-ResourceGroupName MyResourceGroupName:</span><span class="sxs-lookup"><span data-stu-id="d1e29-123">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="d1e29-124">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2 név: MyAppResourceName2 típus: Microsoft. IoTCentral/IoTApps hely: westus címke: {[kulcs, val]} SKU: Microsoft. Azure. Command. IotCentral. models. PSIotCentralAppSkuInfo. ApplicationId. XXXXXXXXXXXX: XXXXXXXX-XXXX-XXXX-XXXX-MYAPPSUBDOMAIN2 DisplayName: az egyéni megjelenítendő név 2 aldomain: SubscriptionId sablon: XXXXXXXXXXXX: XXXXXXXX-XXXX- iotc-default@1.0.0 ResourceGroupName MyResourceGroupName:</span><span class="sxs-lookup"><span data-stu-id="d1e29-124">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="d1e29-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d1e29-125">PARAMETERS</span></span>

### <span data-ttu-id="d1e29-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1e29-126">-DefaultProfile</span></span>
<span data-ttu-id="d1e29-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d1e29-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1e29-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d1e29-128">-Name</span></span>
<span data-ttu-id="d1e29-129">Az IOT központi alkalmazás-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="d1e29-129">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="d1e29-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1e29-130">-ResourceGroupName</span></span>
<span data-ttu-id="d1e29-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d1e29-131">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="d1e29-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1e29-132">-ResourceId</span></span>
<span data-ttu-id="d1e29-133">IOT központi alkalmazás-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="d1e29-133">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="d1e29-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1e29-134">CommonParameters</span></span>
<span data-ttu-id="d1e29-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d1e29-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1e29-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d1e29-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1e29-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1e29-137">INPUTS</span></span>

### <span data-ttu-id="d1e29-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d1e29-138">System.String</span></span>

## <span data-ttu-id="d1e29-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1e29-139">OUTPUTS</span></span>

### <span data-ttu-id="d1e29-140">Microsoft. Azure. Command. IotCentral. models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="d1e29-140">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="d1e29-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d1e29-141">NOTES</span></span>

## <span data-ttu-id="d1e29-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d1e29-142">RELATED LINKS</span></span>