---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/set-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
ms.openlocfilehash: 78fdf68ecb8c50d0eebf4611b51a2fad14c66e5d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666307"
---
# <span data-ttu-id="02c94-101">Set-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="02c94-101">Set-AzIotCentralApp</span></span>

## <span data-ttu-id="02c94-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="02c94-102">SYNOPSIS</span></span>
<span data-ttu-id="02c94-103">Frissíti a IoT-alapú központi alkalmazások metaadatait.</span><span class="sxs-lookup"><span data-stu-id="02c94-103">Updates the metadata for an IoT Central Application.</span></span>

## <span data-ttu-id="02c94-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="02c94-104">SYNTAX</span></span>

### <span data-ttu-id="02c94-105">ResourceIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="02c94-105">ResourceIdParameterSet (Default)</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02c94-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02c94-106">InputObjectParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>]
 -InputObject <PSIotCentralApp> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02c94-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="02c94-107">InteractiveIotCentralParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="02c94-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="02c94-108">DESCRIPTION</span></span>
<span data-ttu-id="02c94-109">Frissítse a IoT-alapú központi alkalmazások metaadatait.</span><span class="sxs-lookup"><span data-stu-id="02c94-109">Update the metadata for an IoT Central Application.</span></span> 

## <span data-ttu-id="02c94-110">Példák</span><span class="sxs-lookup"><span data-stu-id="02c94-110">EXAMPLES</span></span>

### <span data-ttu-id="02c94-111">Példa 1 a megjelenítendő név frissítése</span><span class="sxs-lookup"><span data-stu-id="02c94-111">Example 1 Update Display Name</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

<span data-ttu-id="02c94-112">A megjelenítendő név frissítése egy meglévő IoT-os központi alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="02c94-112">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="02c94-113">Példa kimenet:</span><span class="sxs-lookup"><span data-stu-id="02c94-113">Example Output:</span></span>

<span data-ttu-id="02c94-114">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName név: MyAppResourceName típus: Microsoft. IoTCentral/IoTApps hely: westus címke: SKU: Microsoft. Azure. Command. IotCentral. models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX: az új egyéni megjelenítendő név altartománya: MyAppSubdomain: SubscriptionId-XXXX-XXXX- iotc-default@1.0.0 XXXXXXXXXXXX</span><span class="sxs-lookup"><span data-stu-id="02c94-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My New Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="02c94-115">Példa 2 aldomain frissítése</span><span class="sxs-lookup"><span data-stu-id="02c94-115">Example 2 Update Subdomain</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "new-subdomain"
```

<span data-ttu-id="02c94-116">A megjelenítendő név frissítése egy meglévő IoT-os központi alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="02c94-116">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="02c94-117">Példa kimenet:</span><span class="sxs-lookup"><span data-stu-id="02c94-117">Example Output:</span></span>

<span data-ttu-id="02c94-118">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName név: MyAppResourceName típus: Microsoft. IoTCentral/IoTApps hely: westus címke: SKU: Microsoft. Azure. Command. IotCentral. models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX: megjelenítendő név altartomány: új-aldomain sablon: SubscriptionId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX-ResourceGroupName: MyResourceGroupName iotc-default@1.0.0</span><span class="sxs-lookup"><span data-stu-id="02c94-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : new-subdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="02c94-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="02c94-119">PARAMETERS</span></span>

### <span data-ttu-id="02c94-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02c94-120">-AsJob</span></span>
<span data-ttu-id="02c94-121">A parancsmagot feladatként futtathatja a háttérben.</span><span class="sxs-lookup"><span data-stu-id="02c94-121">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="02c94-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02c94-122">-DefaultProfile</span></span>
<span data-ttu-id="02c94-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="02c94-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02c94-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="02c94-124">-DisplayName</span></span>
<span data-ttu-id="02c94-125">Az IOT központi alkalmazás egyéni megjelenítendő neve</span><span class="sxs-lookup"><span data-stu-id="02c94-125">Custom Display Name of the Iot Central Application.</span></span>

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

### <span data-ttu-id="02c94-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02c94-126">-InputObject</span></span>
<span data-ttu-id="02c94-127">IOT központi alkalmazás bemeneti objektuma</span><span class="sxs-lookup"><span data-stu-id="02c94-127">Iot Central Application Input Object.</span></span>

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

### <span data-ttu-id="02c94-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="02c94-128">-Name</span></span>
<span data-ttu-id="02c94-129">Az IOT központi alkalmazás-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="02c94-129">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="02c94-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02c94-130">-ResourceGroupName</span></span>
<span data-ttu-id="02c94-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="02c94-131">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="02c94-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02c94-132">-ResourceId</span></span>
<span data-ttu-id="02c94-133">IOT központi alkalmazás-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="02c94-133">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="02c94-134">-Aldomain</span><span class="sxs-lookup"><span data-stu-id="02c94-134">-Subdomain</span></span>
<span data-ttu-id="02c94-135">Az IoT központi alkalmazás altartománya.</span><span class="sxs-lookup"><span data-stu-id="02c94-135">Subdomain of the IoT Central Application.</span></span>

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

### <span data-ttu-id="02c94-136">-Címke</span><span class="sxs-lookup"><span data-stu-id="02c94-136">-Tag</span></span>
<span data-ttu-id="02c94-137">IOT központi alkalmazás-erőforrás címkéi</span><span class="sxs-lookup"><span data-stu-id="02c94-137">Iot Central Application Resource Tags.</span></span>

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

### <span data-ttu-id="02c94-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="02c94-138">-Confirm</span></span>
<span data-ttu-id="02c94-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="02c94-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02c94-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02c94-140">-WhatIf</span></span>
<span data-ttu-id="02c94-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="02c94-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02c94-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="02c94-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02c94-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02c94-143">CommonParameters</span></span>
<span data-ttu-id="02c94-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="02c94-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02c94-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02c94-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02c94-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="02c94-146">INPUTS</span></span>

### <span data-ttu-id="02c94-147">System. String</span><span class="sxs-lookup"><span data-stu-id="02c94-147">System.String</span></span>

### <span data-ttu-id="02c94-148">Microsoft. Azure. Command. IotCentral. models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="02c94-148">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="02c94-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="02c94-149">OUTPUTS</span></span>

### <span data-ttu-id="02c94-150">Microsoft. Azure. Command. IotCentral. models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="02c94-150">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="02c94-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="02c94-151">NOTES</span></span>

## <span data-ttu-id="02c94-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="02c94-152">RELATED LINKS</span></span>
