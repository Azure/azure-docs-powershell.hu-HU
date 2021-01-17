---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
ms.openlocfilehash: 364b54f9e0b7a9112c2ce46f33363a4510c7bb68
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386537"
---
# <span data-ttu-id="a8563-101">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="a8563-101">Set-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="a8563-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8563-102">SYNOPSIS</span></span>
<span data-ttu-id="a8563-103">Frissítse egy eszköz elosztott nyomkövetési beállításait.</span><span class="sxs-lookup"><span data-stu-id="a8563-103">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="a8563-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a8563-104">SYNTAX</span></span>

### <span data-ttu-id="a8563-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a8563-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8563-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a8563-106">InputObjectSet</span></span>
```
Set-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8563-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a8563-107">ResourceIdSet</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8563-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a8563-108">DESCRIPTION</span></span>
<span data-ttu-id="a8563-109">Frissítse egy eszköz elosztott nyomkövetési beállításait.</span><span class="sxs-lookup"><span data-stu-id="a8563-109">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="a8563-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a8563-110">EXAMPLES</span></span>

### <span data-ttu-id="a8563-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="a8563-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -SamplingMode Enabled -SamplingRate 22

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="a8563-112">Frissítse egy eszköz elosztott nyomkövetési beállításait.</span><span class="sxs-lookup"><span data-stu-id="a8563-112">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="a8563-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8563-113">PARAMETERS</span></span>

### <span data-ttu-id="a8563-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8563-114">-DefaultProfile</span></span>
<span data-ttu-id="a8563-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a8563-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8563-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="a8563-116">-DeviceId</span></span>
<span data-ttu-id="a8563-117">Céleszköz azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a8563-117">Target Device Id.</span></span>

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

### <span data-ttu-id="a8563-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8563-118">-InputObject</span></span>
<span data-ttu-id="a8563-119">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="a8563-119">IotHub object</span></span>

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

### <span data-ttu-id="a8563-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="a8563-120">-IotHubName</span></span>
<span data-ttu-id="a8563-121">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="a8563-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a8563-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8563-122">-ResourceGroupName</span></span>
<span data-ttu-id="a8563-123">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="a8563-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a8563-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8563-124">-ResourceId</span></span>
<span data-ttu-id="a8563-125">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="a8563-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a8563-126">-SamplingMode</span><span class="sxs-lookup"><span data-stu-id="a8563-126">-SamplingMode</span></span>
<span data-ttu-id="a8563-127">A elosztott nyomkövetés engedélyezése és letiltása esetén a mintavételezést bekapcsolja.</span><span class="sxs-lookup"><span data-stu-id="a8563-127">Turns sampling for distributed tracing enable and disable.</span></span>

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

### <span data-ttu-id="a8563-128">-SamplingRate</span><span class="sxs-lookup"><span data-stu-id="a8563-128">-SamplingRate</span></span>
<span data-ttu-id="a8563-129">A nyomkövetési környezet hozzáadásához mintaként kiválasztott üzenetek mennyiségét szabályozza.</span><span class="sxs-lookup"><span data-stu-id="a8563-129">Controls the amount of messages sampled for adding trace context.</span></span>
<span data-ttu-id="a8563-130">Ez az érték százalékérték.</span><span class="sxs-lookup"><span data-stu-id="a8563-130">This value is a percentage.</span></span>
<span data-ttu-id="a8563-131">Csak a 0 és 100 között (a határértékeket is beleértve) értékek megengedettek.</span><span class="sxs-lookup"><span data-stu-id="a8563-131">Only values from 0 to 100 (inclusive) are permitted.</span></span>

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

### <span data-ttu-id="a8563-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a8563-132">-Confirm</span></span>
<span data-ttu-id="a8563-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a8563-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8563-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8563-134">-WhatIf</span></span>
<span data-ttu-id="a8563-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a8563-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8563-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a8563-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8563-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8563-137">CommonParameters</span></span>
<span data-ttu-id="a8563-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8563-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8563-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8563-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8563-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a8563-140">INPUTS</span></span>

### <span data-ttu-id="a8563-141">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a8563-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a8563-142">System.String</span><span class="sxs-lookup"><span data-stu-id="a8563-142">System.String</span></span>

## <span data-ttu-id="a8563-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8563-143">OUTPUTS</span></span>

### <span data-ttu-id="a8563-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span><span class="sxs-lookup"><span data-stu-id="a8563-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="a8563-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a8563-145">NOTES</span></span>

## <span data-ttu-id="a8563-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a8563-146">RELATED LINKS</span></span>
