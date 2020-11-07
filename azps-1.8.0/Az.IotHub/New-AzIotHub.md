---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
ms.openlocfilehash: 54ba89e380bf5f35d4a95b0bf026b872aa78b14c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835862"
---
# <span data-ttu-id="46c6b-101">New-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="46c6b-101">New-AzIotHub</span></span>

## <span data-ttu-id="46c6b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="46c6b-102">SYNOPSIS</span></span>
<span data-ttu-id="46c6b-103">Új IotHub hoz létre.</span><span class="sxs-lookup"><span data-stu-id="46c6b-103">Creates a new IotHub.</span></span>

## <span data-ttu-id="46c6b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="46c6b-104">SYNTAX</span></span>

```
New-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> -Units <Int64>
 -Location <String> [-Properties <PSIotHubInputProperties>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46c6b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="46c6b-105">DESCRIPTION</span></span>
<span data-ttu-id="46c6b-106">Új IotHub hoz létre.</span><span class="sxs-lookup"><span data-stu-id="46c6b-106">Creates a new IotHub.</span></span>
<span data-ttu-id="46c6b-107">A IotHub az alapértelmezett tulajdonságokkal hozhatja létre, vagy megadhatja a beviteli Proerties.</span><span class="sxs-lookup"><span data-stu-id="46c6b-107">You can create the IotHub with either the default properties or specify the input proerties.</span></span>

## <span data-ttu-id="46c6b-108">Példák</span><span class="sxs-lookup"><span data-stu-id="46c6b-108">EXAMPLES</span></span>

### <span data-ttu-id="46c6b-109">Példa 1 új IotHub létrehozása alapértelmezett tulajdonságokkal</span><span class="sxs-lookup"><span data-stu-id="46c6b-109">Example 1 Create a new IotHub with default properties</span></span>
```
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope"
```

<span data-ttu-id="46c6b-110">A "myiothub" nevű új IotHub hoz létre a SKU "S1", a kapacitás 1 és a "northeurope" helyről.</span><span class="sxs-lookup"><span data-stu-id="46c6b-110">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope".</span></span>

### <span data-ttu-id="46c6b-111">2 példa: új IotHub létrehozása a CloudtoDevice-várólista MaxDeliveryCount 20 értékre</span><span class="sxs-lookup"><span data-stu-id="46c6b-111">Example 2 Create a new IotHub with the MaxDeliveryCount of the CloudtoDevice Queue set to 20</span></span>
```
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties
```

<span data-ttu-id="46c6b-112">A "myiothub" nevű új IotHub hoz létre az "S1", a kapacitás 1 és a "northeurope" hely mellett, az $properties által képviselt speciális beviteli tulajdonságokkal.</span><span class="sxs-lookup"><span data-stu-id="46c6b-112">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" with advanced input properties represented by $properties.</span></span>
<span data-ttu-id="46c6b-113">$psCloudToDeviceProperties = New-Object Microsoft. Azure. Command. Management. IotHub. models. PSCloudToDeviceProperties-Property @ {MaxDeliveryCount = 20} $properties = New-Object Microsoft. Azure. commands. Management. IotHub. models. PSIotHubInputProperties-tulajdonság @ {CloudToDevice = $psCloudToDeviceProperties} New-AzIotHub-ResourceGroupName "myresourcegroup"-Name "myiothub"-SkuName</span><span class="sxs-lookup"><span data-stu-id="46c6b-113">$psCloudToDeviceProperties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties -Property @{MaxDeliveryCount=20} $properties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties -Property @{CloudToDevice=$psCloudToDeviceProperties} New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties</span></span>

## <span data-ttu-id="46c6b-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="46c6b-114">PARAMETERS</span></span>

### <span data-ttu-id="46c6b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46c6b-115">-DefaultProfile</span></span>
<span data-ttu-id="46c6b-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="46c6b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46c6b-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="46c6b-117">-Location</span></span>
<span data-ttu-id="46c6b-118">Az a hely, ahol a IoT-hubot létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="46c6b-118">Location where the IoT hub needs to be created.</span></span> 

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

### <span data-ttu-id="46c6b-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="46c6b-119">-Name</span></span>
<span data-ttu-id="46c6b-120">A IotHub neve</span><span class="sxs-lookup"><span data-stu-id="46c6b-120">Name of the IotHub</span></span>

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

### <span data-ttu-id="46c6b-121">-Tulajdonságok</span><span class="sxs-lookup"><span data-stu-id="46c6b-121">-Properties</span></span>
<span data-ttu-id="46c6b-122">A IoT-központ tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="46c6b-122">Properties of the IoT hub.</span></span> 

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

### <span data-ttu-id="46c6b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46c6b-123">-ResourceGroupName</span></span>
<span data-ttu-id="46c6b-124">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="46c6b-124">Resource Group Name</span></span>

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

### <span data-ttu-id="46c6b-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="46c6b-125">-SkuName</span></span>
<span data-ttu-id="46c6b-126">A SKU neve</span><span class="sxs-lookup"><span data-stu-id="46c6b-126">Name of the sku</span></span>

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

### <span data-ttu-id="46c6b-127">-Egységek</span><span class="sxs-lookup"><span data-stu-id="46c6b-127">-Units</span></span>
<span data-ttu-id="46c6b-128">Egységek száma</span><span class="sxs-lookup"><span data-stu-id="46c6b-128">Number of units</span></span>

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

### <span data-ttu-id="46c6b-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="46c6b-129">-Confirm</span></span>
<span data-ttu-id="46c6b-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="46c6b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46c6b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46c6b-131">-WhatIf</span></span>
<span data-ttu-id="46c6b-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="46c6b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46c6b-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="46c6b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46c6b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46c6b-134">CommonParameters</span></span>
<span data-ttu-id="46c6b-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="46c6b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46c6b-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46c6b-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46c6b-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="46c6b-137">INPUTS</span></span>

### <span data-ttu-id="46c6b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="46c6b-138">System.String</span></span>

## <span data-ttu-id="46c6b-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="46c6b-139">OUTPUTS</span></span>

### <span data-ttu-id="46c6b-140">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="46c6b-140">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="46c6b-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="46c6b-141">NOTES</span></span>

## <span data-ttu-id="46c6b-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="46c6b-142">RELATED LINKS</span></span>
