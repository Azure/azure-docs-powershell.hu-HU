---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
ms.openlocfilehash: 364b54f9e0b7a9112c2ce46f33363a4510c7bb68
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011412"
---
# <span data-ttu-id="0d420-101">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="0d420-101">Set-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="0d420-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0d420-102">SYNOPSIS</span></span>
<span data-ttu-id="0d420-103">Az eszköz terjesztett nyomkövetési beállításainak frissítése</span><span class="sxs-lookup"><span data-stu-id="0d420-103">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="0d420-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0d420-104">SYNTAX</span></span>

### <span data-ttu-id="0d420-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0d420-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d420-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0d420-106">InputObjectSet</span></span>
```
Set-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d420-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0d420-107">ResourceIdSet</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d420-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0d420-108">DESCRIPTION</span></span>
<span data-ttu-id="0d420-109">Az eszköz terjesztett nyomkövetési beállításainak frissítése</span><span class="sxs-lookup"><span data-stu-id="0d420-109">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="0d420-110">Példák</span><span class="sxs-lookup"><span data-stu-id="0d420-110">EXAMPLES</span></span>

### <span data-ttu-id="0d420-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0d420-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -SamplingMode Enabled -SamplingRate 22

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="0d420-112">Az eszköz terjesztett nyomkövetési beállításainak frissítése</span><span class="sxs-lookup"><span data-stu-id="0d420-112">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="0d420-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0d420-113">PARAMETERS</span></span>

### <span data-ttu-id="0d420-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d420-114">-DefaultProfile</span></span>
<span data-ttu-id="0d420-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0d420-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d420-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="0d420-116">-DeviceId</span></span>
<span data-ttu-id="0d420-117">Céleszköz-azonosító.</span><span class="sxs-lookup"><span data-stu-id="0d420-117">Target Device Id.</span></span>

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

### <span data-ttu-id="0d420-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d420-118">-InputObject</span></span>
<span data-ttu-id="0d420-119">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="0d420-119">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d420-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="0d420-120">-IotHubName</span></span>
<span data-ttu-id="0d420-121">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="0d420-121">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d420-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d420-122">-ResourceGroupName</span></span>
<span data-ttu-id="0d420-123">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="0d420-123">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d420-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d420-124">-ResourceId</span></span>
<span data-ttu-id="0d420-125">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="0d420-125">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d420-126">-SamplingMode</span><span class="sxs-lookup"><span data-stu-id="0d420-126">-SamplingMode</span></span>
<span data-ttu-id="0d420-127">Bekapcsolja a mintavételt az elosztott nyomkövetés engedélyezéséhez és letiltásához.</span><span class="sxs-lookup"><span data-stu-id="0d420-127">Turns sampling for distributed tracing enable and disable.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDistributedTracingSamplingMode
Parameter Sets: (All)
Aliases: Mode
Accepted values: Disabled, Enabled

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d420-128">-SamplingRate</span><span class="sxs-lookup"><span data-stu-id="0d420-128">-SamplingRate</span></span>
<span data-ttu-id="0d420-129">Szabályozza a mintázott üzenetek számát a nyomkövetési környezet hozzáadásához.</span><span class="sxs-lookup"><span data-stu-id="0d420-129">Controls the amount of messages sampled for adding trace context.</span></span>
<span data-ttu-id="0d420-130">Ez az érték egy százalék.</span><span class="sxs-lookup"><span data-stu-id="0d420-130">This value is a percentage.</span></span>
<span data-ttu-id="0d420-131">Csak a 0 – 100 (beleértve) értékek engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="0d420-131">Only values from 0 to 100 (inclusive) are permitted.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Rate

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d420-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0d420-132">-Confirm</span></span>
<span data-ttu-id="0d420-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0d420-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d420-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d420-134">-WhatIf</span></span>
<span data-ttu-id="0d420-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0d420-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d420-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0d420-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d420-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d420-137">CommonParameters</span></span>
<span data-ttu-id="0d420-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0d420-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d420-139">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d420-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d420-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d420-140">INPUTS</span></span>

### <span data-ttu-id="0d420-141">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="0d420-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="0d420-142">System. String</span><span class="sxs-lookup"><span data-stu-id="0d420-142">System.String</span></span>

## <span data-ttu-id="0d420-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d420-143">OUTPUTS</span></span>

### <span data-ttu-id="0d420-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span><span class="sxs-lookup"><span data-stu-id="0d420-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="0d420-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0d420-145">NOTES</span></span>

## <span data-ttu-id="0d420-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0d420-146">RELATED LINKS</span></span>
