---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/set-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
ms.openlocfilehash: cea582481515f519e14df9f430dc1326e72a0877
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94002941"
---
# <span data-ttu-id="af274-101">Set-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="af274-101">Set-AzIotCentralApp</span></span>

## <span data-ttu-id="af274-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="af274-102">SYNOPSIS</span></span>
<span data-ttu-id="af274-103">Frissíti a IoT-alapú központi alkalmazások metaadatait.</span><span class="sxs-lookup"><span data-stu-id="af274-103">Updates the metadata for an IoT Central Application.</span></span>

## <span data-ttu-id="af274-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="af274-104">SYNTAX</span></span>

### <span data-ttu-id="af274-105">ResourceIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="af274-105">ResourceIdParameterSet (Default)</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af274-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="af274-106">InputObjectParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>]
 -InputObject <PSIotCentralApp> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="af274-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="af274-107">InteractiveIotCentralParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="af274-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="af274-108">DESCRIPTION</span></span>
<span data-ttu-id="af274-109">Frissítse a IoT-alapú központi alkalmazások metaadatait.</span><span class="sxs-lookup"><span data-stu-id="af274-109">Update the metadata for an IoT Central Application.</span></span> 

## <span data-ttu-id="af274-110">Példák</span><span class="sxs-lookup"><span data-stu-id="af274-110">EXAMPLES</span></span>

### <span data-ttu-id="af274-111">Példa 1 a megjelenítendő név frissítése</span><span class="sxs-lookup"><span data-stu-id="af274-111">Example 1 Update Display Name</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

<span data-ttu-id="af274-112">A megjelenítendő név frissítése egy meglévő IoT-os központi alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="af274-112">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="af274-113">Példa kimenet:</span><span class="sxs-lookup"><span data-stu-id="af274-113">Example Output:</span></span>

<span data-ttu-id="af274-114">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName név: MyAppResourceName típus: Microsoft. IoTCentral/IoTApps hely: westus címke: SKU: Microsoft. Azure. Command. IotCentral. models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX: az új egyéni megjelenítendő név altartománya: MyAppSubdomain: SubscriptionId-XXXX-XXXX- iotc-default@1.0.0 XXXXXXXXXXXX</span><span class="sxs-lookup"><span data-stu-id="af274-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My New Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="af274-115">Példa 2 aldomain frissítése</span><span class="sxs-lookup"><span data-stu-id="af274-115">Example 2 Update Subdomain</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "new-subdomain"
```

<span data-ttu-id="af274-116">A megjelenítendő név frissítése egy meglévő IoT-os központi alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="af274-116">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="af274-117">Példa kimenet:</span><span class="sxs-lookup"><span data-stu-id="af274-117">Example Output:</span></span>

<span data-ttu-id="af274-118">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName név: MyAppResourceName típus: Microsoft. IoTCentral/IoTApps hely: westus címke: SKU: Microsoft. Azure. Command. IotCentral. models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX: megjelenítendő név altartomány: új-aldomain sablon: SubscriptionId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX-ResourceGroupName: MyResourceGroupName iotc-default@1.0.0</span><span class="sxs-lookup"><span data-stu-id="af274-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : new-subdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="af274-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="af274-119">PARAMETERS</span></span>

### <span data-ttu-id="af274-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="af274-120">-AsJob</span></span>
<span data-ttu-id="af274-121">A parancsmagot feladatként futtathatja a háttérben.</span><span class="sxs-lookup"><span data-stu-id="af274-121">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="af274-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af274-122">-DefaultProfile</span></span>
<span data-ttu-id="af274-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="af274-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af274-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="af274-124">-DisplayName</span></span>
<span data-ttu-id="af274-125">Az IOT központi alkalmazás egyéni megjelenítendő neve</span><span class="sxs-lookup"><span data-stu-id="af274-125">Custom Display Name of the Iot Central Application.</span></span>

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

### <span data-ttu-id="af274-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af274-126">-InputObject</span></span>
<span data-ttu-id="af274-127">IOT központi alkalmazás bemeneti objektuma</span><span class="sxs-lookup"><span data-stu-id="af274-127">Iot Central Application Input Object.</span></span>

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

### <span data-ttu-id="af274-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="af274-128">-Name</span></span>
<span data-ttu-id="af274-129">Az IOT központi alkalmazás-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="af274-129">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="af274-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af274-130">-ResourceGroupName</span></span>
<span data-ttu-id="af274-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="af274-131">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="af274-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af274-132">-ResourceId</span></span>
<span data-ttu-id="af274-133">IOT központi alkalmazás-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="af274-133">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="af274-134">-Aldomain</span><span class="sxs-lookup"><span data-stu-id="af274-134">-Subdomain</span></span>
<span data-ttu-id="af274-135">Az IoT központi alkalmazás altartománya.</span><span class="sxs-lookup"><span data-stu-id="af274-135">Subdomain of the IoT Central Application.</span></span>

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

### <span data-ttu-id="af274-136">-Címke</span><span class="sxs-lookup"><span data-stu-id="af274-136">-Tag</span></span>
<span data-ttu-id="af274-137">IOT központi alkalmazás-erőforrás címkéi</span><span class="sxs-lookup"><span data-stu-id="af274-137">Iot Central Application Resource Tags.</span></span>

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

### <span data-ttu-id="af274-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="af274-138">-Confirm</span></span>
<span data-ttu-id="af274-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="af274-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af274-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af274-140">-WhatIf</span></span>
<span data-ttu-id="af274-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="af274-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af274-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="af274-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af274-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af274-143">CommonParameters</span></span>
<span data-ttu-id="af274-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="af274-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af274-145">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af274-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af274-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="af274-146">INPUTS</span></span>

### <span data-ttu-id="af274-147">System. String</span><span class="sxs-lookup"><span data-stu-id="af274-147">System.String</span></span>

### <span data-ttu-id="af274-148">Microsoft. Azure. Command. IotCentral. models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="af274-148">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="af274-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="af274-149">OUTPUTS</span></span>

### <span data-ttu-id="af274-150">Microsoft. Azure. Command. IotCentral. models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="af274-150">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="af274-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="af274-151">NOTES</span></span>

## <span data-ttu-id="af274-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="af274-152">RELATED LINKS</span></span>
