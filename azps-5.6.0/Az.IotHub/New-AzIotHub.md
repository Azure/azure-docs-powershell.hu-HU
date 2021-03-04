---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/new-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
ms.openlocfilehash: 71f5e9805467bc285b991a9aa4ee289b3d807729
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936785"
---
# <span data-ttu-id="5fff1-101">New-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="5fff1-101">New-AzIotHub</span></span>

## <span data-ttu-id="5fff1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fff1-102">SYNOPSIS</span></span>
<span data-ttu-id="5fff1-103">Létrehoz egy új IotHubot.</span><span class="sxs-lookup"><span data-stu-id="5fff1-103">Creates a new IotHub.</span></span>

## <span data-ttu-id="5fff1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5fff1-104">SYNTAX</span></span>

```
New-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> -Units <Int64>
 -Location <String> [-Properties <PSIotHubInputProperties>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fff1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5fff1-105">DESCRIPTION</span></span>
<span data-ttu-id="5fff1-106">Létrehoz egy új IotHubot.</span><span class="sxs-lookup"><span data-stu-id="5fff1-106">Creates a new IotHub.</span></span>
<span data-ttu-id="5fff1-107">Az IotHubot létrehozhatja az alapértelmezett tulajdonságokkal, vagy megadhatja a bemeneti tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="5fff1-107">You can create the IotHub with either the default properties or specify the input properties.</span></span>

## <span data-ttu-id="5fff1-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5fff1-108">EXAMPLES</span></span>

### <span data-ttu-id="5fff1-109">1. példa: Új IotHub létrehozása alapértelmezett tulajdonságokkal</span><span class="sxs-lookup"><span data-stu-id="5fff1-109">Example 1 Create a new IotHub with default properties</span></span>
```
PS C:\> $tags = @{}
PS C:\> $tags.Add('key1','value1')
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Tag $tags
```

<span data-ttu-id="5fff1-110">Létrehozza az "S1" termékváltozat "myiothub" nevű új IotHubját, az 1-es kapacitást és a "northeurope" helyet a Címkék között.</span><span class="sxs-lookup"><span data-stu-id="5fff1-110">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" included with Tags.</span></span>

### <span data-ttu-id="5fff1-111">2. példa: Új IotHub létrehozása a CloudToDevice-várólista MaxDeliveryCount értékében 20-ra van állítva</span><span class="sxs-lookup"><span data-stu-id="5fff1-111">Example 2 Create a new IotHub with the MaxDeliveryCount of the CloudToDevice Queue set to 20</span></span>
```
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties
```

<span data-ttu-id="5fff1-112">Létrehozza az "S1" termékváltozat "myiothub" nevű új IotHubját, az 1-es kapacitást és a "northeurope" helyet, és speciális beviteli tulajdonságokat ad $properties.</span><span class="sxs-lookup"><span data-stu-id="5fff1-112">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" with advanced input properties represented by $properties.</span></span>
<span data-ttu-id="5fff1-113">$psCloudToDeviceProperties = New-Object Microsoft.Azure.Commands.Management.iotHub.Models.PSCloudToDeviceProperties -Property @{MaxDeliveryCount=20} $properties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties -Property @{CloudToDevice=$psCloudToDeviceProperties} New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties</span><span class="sxs-lookup"><span data-stu-id="5fff1-113">$psCloudToDeviceProperties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties -Property @{MaxDeliveryCount=20} $properties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties -Property @{CloudToDevice=$psCloudToDeviceProperties} New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties</span></span>

## <span data-ttu-id="5fff1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5fff1-114">PARAMETERS</span></span>

### <span data-ttu-id="5fff1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fff1-115">-DefaultProfile</span></span>
<span data-ttu-id="5fff1-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5fff1-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5fff1-117">-Location</span><span class="sxs-lookup"><span data-stu-id="5fff1-117">-Location</span></span>
<span data-ttu-id="5fff1-118">Az a hely, ahol létre kell hozatni az IoT-központot.</span><span class="sxs-lookup"><span data-stu-id="5fff1-118">Location where the IoT hub needs to be created.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fff1-119">-Name</span><span class="sxs-lookup"><span data-stu-id="5fff1-119">-Name</span></span>
<span data-ttu-id="5fff1-120">Az IotHub neve</span><span class="sxs-lookup"><span data-stu-id="5fff1-120">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fff1-121">-Properties</span><span class="sxs-lookup"><span data-stu-id="5fff1-121">-Properties</span></span>
<span data-ttu-id="5fff1-122">Az IoT-központ tulajdonságai.</span><span class="sxs-lookup"><span data-stu-id="5fff1-122">Properties of the IoT hub.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fff1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fff1-123">-ResourceGroupName</span></span>
<span data-ttu-id="5fff1-124">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="5fff1-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fff1-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="5fff1-125">-SkuName</span></span>
<span data-ttu-id="5fff1-126">A termékváltozat neve</span><span class="sxs-lookup"><span data-stu-id="5fff1-126">Name of the sku</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSku
Parameter Sets: (All)
Aliases:
Accepted values: F1, S1, S2, S3, B1, B2, B3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fff1-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="5fff1-127">-Tag</span></span>
<span data-ttu-id="5fff1-128">Az IoT-központ példánycímkéi.</span><span class="sxs-lookup"><span data-stu-id="5fff1-128">IoT hub instance tags.</span></span> <span data-ttu-id="5fff1-129">Property bag in key-value pairs in a form of a hash table.</span><span class="sxs-lookup"><span data-stu-id="5fff1-129">Property bag in key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="5fff1-130">-Egység</span><span class="sxs-lookup"><span data-stu-id="5fff1-130">-Units</span></span>
<span data-ttu-id="5fff1-131">Egységek száma</span><span class="sxs-lookup"><span data-stu-id="5fff1-131">Number of units</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fff1-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5fff1-132">-Confirm</span></span>
<span data-ttu-id="5fff1-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5fff1-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fff1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fff1-134">-WhatIf</span></span>
<span data-ttu-id="5fff1-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5fff1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fff1-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5fff1-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fff1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fff1-137">CommonParameters</span></span>
<span data-ttu-id="5fff1-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fff1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fff1-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fff1-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fff1-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5fff1-140">INPUTS</span></span>

### <span data-ttu-id="5fff1-141">System.String</span><span class="sxs-lookup"><span data-stu-id="5fff1-141">System.String</span></span>

## <span data-ttu-id="5fff1-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5fff1-142">OUTPUTS</span></span>

### <span data-ttu-id="5fff1-143">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="5fff1-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="5fff1-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5fff1-144">NOTES</span></span>

## <span data-ttu-id="5fff1-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5fff1-145">RELATED LINKS</span></span>
