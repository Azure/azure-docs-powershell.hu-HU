---
external help file: Microsoft.Azure.Commands.IotCentral.dll-Help.xml
Module Name: AzureRM.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iotcentral/set-azurermiotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Set-AzureRmIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Set-AzureRmIotCentralApp.md
ms.openlocfilehash: a9b7dbc962809288979f5293c14fd875081f48bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680664"
---
# <span data-ttu-id="a2d2a-101">Set-AzureRmIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="a2d2a-101">Set-AzureRmIotCentralApp</span></span>

## <span data-ttu-id="a2d2a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a2d2a-102">SYNOPSIS</span></span>
<span data-ttu-id="a2d2a-103">Frissíti a IoT-alapú központi alkalmazások metaadatait.</span><span class="sxs-lookup"><span data-stu-id="a2d2a-103">Updates the metadata for an IoT Central Application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2d2a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a2d2a-104">SYNTAX</span></span>

### <span data-ttu-id="a2d2a-105">ResourceIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a2d2a-105">ResourceIdParameterSet (Default)</span></span>
```
Set-AzureRmIotCentralApp [-DisplayName <String>] [-Tag <Hashtable>] -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2d2a-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2d2a-106">InputObjectParameterSet</span></span>
```
Set-AzureRmIotCentralApp [-DisplayName <String>] [-Tag <Hashtable>] -InputObject <PSIotCentralApp> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2d2a-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2d2a-107">InteractiveIotCentralParameterSet</span></span>
```
Set-AzureRmIotCentralApp [-DisplayName <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2d2a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a2d2a-108">DESCRIPTION</span></span>
<span data-ttu-id="a2d2a-109">Frissítse a IoT-alapú központi alkalmazások metaadatait.</span><span class="sxs-lookup"><span data-stu-id="a2d2a-109">Update the metadata for an IoT Central Application.</span></span> 

## <span data-ttu-id="a2d2a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a2d2a-110">EXAMPLES</span></span>

### <span data-ttu-id="a2d2a-111">Példa 1 a megjelenítendő név frissítése</span><span class="sxs-lookup"><span data-stu-id="a2d2a-111">Example 1 Update Display Name</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

<span data-ttu-id="a2d2a-112">A megjelenítendő név frissítése egy meglévő IoT-os központi alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="a2d2a-112">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="a2d2a-113">Példa kimenet:</span><span class="sxs-lookup"><span data-stu-id="a2d2a-113">Example Output:</span></span>

<span data-ttu-id="a2d2a-114">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName név: MyAppResourceName típus: Microsoft. IoTCentral/IoTApps hely: westus címke: SKU: Microsoft. Azure. Command. IotCentral. models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX: az új egyéni megjelenítendő név altartománya: MyAppSubdomain: SubscriptionId-XXXX-XXXX- iotc-default@1.0.0 XXXXXXXXXXXX</span><span class="sxs-lookup"><span data-stu-id="a2d2a-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My New Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="a2d2a-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a2d2a-115">PARAMETERS</span></span>

### <span data-ttu-id="a2d2a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2d2a-116">-AsJob</span></span>
<span data-ttu-id="a2d2a-117">A parancsmagot feladatként futtathatja a háttérben.</span><span class="sxs-lookup"><span data-stu-id="a2d2a-117">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="a2d2a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2d2a-118">-DefaultProfile</span></span>
<span data-ttu-id="a2d2a-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a2d2a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2d2a-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a2d2a-120">-DisplayName</span></span>
<span data-ttu-id="a2d2a-121">Az IOT központi alkalmazás egyéni megjelenítendő neve</span><span class="sxs-lookup"><span data-stu-id="a2d2a-121">Custom Display Name of the Iot Central Application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2d2a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2d2a-122">-InputObject</span></span>
<span data-ttu-id="a2d2a-123">IOT központi alkalmazás bemeneti objektuma</span><span class="sxs-lookup"><span data-stu-id="a2d2a-123">Iot Central Application Input Object.</span></span>

```yaml
Type: PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2d2a-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a2d2a-124">-Name</span></span>
<span data-ttu-id="a2d2a-125">Az IOT központi alkalmazás-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="a2d2a-125">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="a2d2a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2d2a-126">-ResourceGroupName</span></span>
<span data-ttu-id="a2d2a-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a2d2a-127">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="a2d2a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2d2a-128">-ResourceId</span></span>
<span data-ttu-id="a2d2a-129">IOT központi alkalmazás-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="a2d2a-129">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="a2d2a-130">-Címke</span><span class="sxs-lookup"><span data-stu-id="a2d2a-130">-Tag</span></span>
<span data-ttu-id="a2d2a-131">IOT központi alkalmazás-erőforrás címkéi</span><span class="sxs-lookup"><span data-stu-id="a2d2a-131">Iot Central Application Resource Tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2d2a-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a2d2a-132">-Confirm</span></span>
<span data-ttu-id="a2d2a-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a2d2a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2d2a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2d2a-134">-WhatIf</span></span>
<span data-ttu-id="a2d2a-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a2d2a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2d2a-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a2d2a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2d2a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2d2a-137">CommonParameters</span></span>
<span data-ttu-id="a2d2a-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a2d2a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2d2a-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2d2a-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2d2a-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2d2a-140">INPUTS</span></span>

### <span data-ttu-id="a2d2a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a2d2a-141">System.String</span></span>
### <span data-ttu-id="a2d2a-142">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a2d2a-142">System.Collections.Hashtable</span></span>
### <span data-ttu-id="a2d2a-143">Microsoft. Azure. Command. IotCentral. models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="a2d2a-143">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>
## <span data-ttu-id="a2d2a-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2d2a-144">OUTPUTS</span></span>

### <span data-ttu-id="a2d2a-145">Microsoft. Azure. Command. IotCentral. models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="a2d2a-145">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>
## <span data-ttu-id="a2d2a-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a2d2a-146">NOTES</span></span>

## <span data-ttu-id="a2d2a-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2d2a-147">RELATED LINKS</span></span>
