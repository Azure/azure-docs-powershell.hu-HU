---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/set-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
ms.openlocfilehash: 94a6e4d2b140487b279d85db1a8b663e03523ce4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183561"
---
# <span data-ttu-id="07295-101">Set-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="07295-101">Set-AzIotCentralApp</span></span>

## <span data-ttu-id="07295-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="07295-102">SYNOPSIS</span></span>
<span data-ttu-id="07295-103">Frissíti a IoT-alapú központi alkalmazások metaadatait.</span><span class="sxs-lookup"><span data-stu-id="07295-103">Updates the metadata for an IoT Central Application.</span></span>

## <span data-ttu-id="07295-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="07295-104">SYNTAX</span></span>

### <span data-ttu-id="07295-105">ResourceIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="07295-105">ResourceIdParameterSet (Default)</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>]
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="07295-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="07295-106">InputObjectParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>]
 -InputObject <PSIotCentralApp> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="07295-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="07295-107">InteractiveIotCentralParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="07295-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="07295-108">DESCRIPTION</span></span>
<span data-ttu-id="07295-109">Frissítse a IoT-alapú központi alkalmazások metaadatait.</span><span class="sxs-lookup"><span data-stu-id="07295-109">Update the metadata for an IoT Central Application.</span></span> 

## <span data-ttu-id="07295-110">Példák</span><span class="sxs-lookup"><span data-stu-id="07295-110">EXAMPLES</span></span>

### <span data-ttu-id="07295-111">Példa 1 a megjelenítendő név frissítése</span><span class="sxs-lookup"><span data-stu-id="07295-111">Example 1 Update Display Name</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

<span data-ttu-id="07295-112">A megjelenítendő név frissítése egy meglévő IoT-os központi alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="07295-112">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="07295-113">Példa kimenet:</span><span class="sxs-lookup"><span data-stu-id="07295-113">Example Output:</span></span>

<span data-ttu-id="07295-114">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName név: MyAppResourceName típus: Microsoft. IoTCentral/IoTApps hely: westus címke: SKU: Microsoft. Azure. Command. IotCentral. models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX: az új egyéni megjelenítendő név altartománya: MyAppSubdomain: SubscriptionId-XXXX-XXXX- iotc-default@1.0.0 XXXXXXXXXXXX</span><span class="sxs-lookup"><span data-stu-id="07295-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My New Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="07295-115">Példa 2 aldomain frissítése</span><span class="sxs-lookup"><span data-stu-id="07295-115">Example 2 Update Subdomain</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "new-subdomain"
```

<span data-ttu-id="07295-116">A megjelenítendő név frissítése egy meglévő IoT-os központi alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="07295-116">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="07295-117">Példa kimenet:</span><span class="sxs-lookup"><span data-stu-id="07295-117">Example Output:</span></span>

<span data-ttu-id="07295-118">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName név: MyAppResourceName típus: Microsoft. IoTCentral/IoTApps hely: westus címke: SKU: Microsoft. Azure. Command. IotCentral. models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX: megjelenítendő név altartomány: új-aldomain sablon: SubscriptionId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX-ResourceGroupName: MyResourceGroupName iotc-default@1.0.0</span><span class="sxs-lookup"><span data-stu-id="07295-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : new-subdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="07295-119">Példa 3 Update app SKU info</span><span class="sxs-lookup"><span data-stu-id="07295-119">Example 3 Update App Sku Info</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Sku "ST2"
```

<span data-ttu-id="07295-120">Frissítse a SKU-ot egy meglévő IoT központi alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="07295-120">Update the sku on an existing IoT Central Application.</span></span>

<span data-ttu-id="07295-121">Példa kimenet:</span><span class="sxs-lookup"><span data-stu-id="07295-121">Example Output:</span></span>

<span data-ttu-id="07295-122">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName név: MyAppResourceName típus: Microsoft. IoTCentral/IoTApps hely: westus címke: SKU: Microsoft. Azure. Command. IotCentral. models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX: megjelenítendő név altartomány: MyAppSubdomain sablon: SubscriptionId-XXXX-XXXX- iotc-default@1.0.0 XXXXXXXXXXXX ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07295-122">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="07295-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="07295-123">PARAMETERS</span></span>

### <span data-ttu-id="07295-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07295-124">-AsJob</span></span>
<span data-ttu-id="07295-125">A parancsmagot feladatként futtathatja a háttérben.</span><span class="sxs-lookup"><span data-stu-id="07295-125">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="07295-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07295-126">-DefaultProfile</span></span>
<span data-ttu-id="07295-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="07295-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07295-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="07295-128">-DisplayName</span></span>
<span data-ttu-id="07295-129">Az IOT központi alkalmazás egyéni megjelenítendő neve</span><span class="sxs-lookup"><span data-stu-id="07295-129">Custom Display Name of the Iot Central Application.</span></span>

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

### <span data-ttu-id="07295-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07295-130">-InputObject</span></span>
<span data-ttu-id="07295-131">IOT központi alkalmazás bemeneti objektuma</span><span class="sxs-lookup"><span data-stu-id="07295-131">Iot Central Application Input Object.</span></span>

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

### <span data-ttu-id="07295-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="07295-132">-Name</span></span>
<span data-ttu-id="07295-133">Az IOT központi alkalmazás-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="07295-133">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="07295-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07295-134">-ResourceGroupName</span></span>
<span data-ttu-id="07295-135">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="07295-135">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="07295-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07295-136">-ResourceId</span></span>
<span data-ttu-id="07295-137">IOT központi alkalmazás-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="07295-137">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="07295-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="07295-138">-Sku</span></span>
<span data-ttu-id="07295-139">Az IoT központi alkalmazásainak árazási szintje.</span><span class="sxs-lookup"><span data-stu-id="07295-139">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="07295-140">Az alapértelmezett érték a ST2.</span><span class="sxs-lookup"><span data-stu-id="07295-140">Default value is ST2.</span></span>

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

### <span data-ttu-id="07295-141">-Aldomain</span><span class="sxs-lookup"><span data-stu-id="07295-141">-Subdomain</span></span>
<span data-ttu-id="07295-142">Az IoT központi alkalmazás altartománya.</span><span class="sxs-lookup"><span data-stu-id="07295-142">Subdomain of the IoT Central Application.</span></span>

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

### <span data-ttu-id="07295-143">-Címke</span><span class="sxs-lookup"><span data-stu-id="07295-143">-Tag</span></span>
<span data-ttu-id="07295-144">IOT központi alkalmazás-erőforrás címkéi</span><span class="sxs-lookup"><span data-stu-id="07295-144">Iot Central Application Resource Tags.</span></span>

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

### <span data-ttu-id="07295-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="07295-145">-Confirm</span></span>
<span data-ttu-id="07295-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="07295-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07295-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07295-147">-WhatIf</span></span>
<span data-ttu-id="07295-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="07295-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07295-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="07295-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07295-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07295-150">CommonParameters</span></span>
<span data-ttu-id="07295-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="07295-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07295-152">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="07295-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07295-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="07295-153">INPUTS</span></span>

### <span data-ttu-id="07295-154">System. String</span><span class="sxs-lookup"><span data-stu-id="07295-154">System.String</span></span>

### <span data-ttu-id="07295-155">Microsoft. Azure. Command. IotCentral. models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="07295-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="07295-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="07295-156">OUTPUTS</span></span>

### <span data-ttu-id="07295-157">Microsoft. Azure. Command. IotCentral. models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="07295-157">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="07295-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="07295-158">NOTES</span></span>

## <span data-ttu-id="07295-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="07295-159">RELATED LINKS</span></span>
