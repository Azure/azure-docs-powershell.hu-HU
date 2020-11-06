---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/new-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHub.md
ms.openlocfilehash: a24f06c07552f60aa5e18ab6af0c7d25b78b567d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497444"
---
# <span data-ttu-id="bc9ea-101">New-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="bc9ea-101">New-AzureRmIotHub</span></span>

## <span data-ttu-id="bc9ea-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bc9ea-102">SYNOPSIS</span></span>
<span data-ttu-id="bc9ea-103">Új IotHub hoz létre.</span><span class="sxs-lookup"><span data-stu-id="bc9ea-103">Creates a new IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc9ea-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bc9ea-104">SYNTAX</span></span>

```
New-AzureRmIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> -Units <Int64>
 -Location <String> [-Properties <PSIotHubInputProperties>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc9ea-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bc9ea-105">DESCRIPTION</span></span>
<span data-ttu-id="bc9ea-106">Új IotHub hoz létre.</span><span class="sxs-lookup"><span data-stu-id="bc9ea-106">Creates a new IotHub.</span></span>
<span data-ttu-id="bc9ea-107">A IotHub az alapértelmezett tulajdonságokkal hozhatja létre, vagy megadhatja a beviteli Proerties.</span><span class="sxs-lookup"><span data-stu-id="bc9ea-107">You can create the IotHub with either the default properties or specify the input proerties.</span></span>

## <span data-ttu-id="bc9ea-108">Példák</span><span class="sxs-lookup"><span data-stu-id="bc9ea-108">EXAMPLES</span></span>

### <span data-ttu-id="bc9ea-109">Példa 1 új IotHub létrehozása alapértelmezett tulajdonságokkal</span><span class="sxs-lookup"><span data-stu-id="bc9ea-109">Example 1 Create a new IotHub with default properties</span></span>
```
PS C:\> New-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope"
```

<span data-ttu-id="bc9ea-110">A "myiothub" nevű új IotHub hoz létre a SKU "S1", a kapacitás 1 és a "northeurope" helyről.</span><span class="sxs-lookup"><span data-stu-id="bc9ea-110">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope".</span></span>

### <span data-ttu-id="bc9ea-111">2 példa: új IotHub létrehozása a CloudtoDevice-várólista MaxDeliveryCount 20 értékre</span><span class="sxs-lookup"><span data-stu-id="bc9ea-111">Example 2 Create a new IotHub with the MaxDeliveryCount of the CloudtoDevice Queue set to 20</span></span>
```
PS C:\> New-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties
```

<span data-ttu-id="bc9ea-112">A "myiothub" nevű új IotHub hoz létre az "S1", a kapacitás 1 és a "northeurope" hely mellett, az $properties által képviselt speciális beviteli tulajdonságokkal.</span><span class="sxs-lookup"><span data-stu-id="bc9ea-112">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" with advanced input properties represented by $properties.</span></span>
<span data-ttu-id="bc9ea-113">$psCloudToDeviceProperties = New-Object Microsoft. Azure. Command. Management. IotHub. models. PSCloudToDeviceProperties-Property @ {MaxDeliveryCount = 20} $properties = New-Object Microsoft. Azure. commands. Management. IotHub. models. PSIotHubInputProperties-tulajdonság @ {CloudToDevice = $psCloudToDeviceProperties} New-AzureRmIotHub-ResourceGroupName "myresourcegroup"-Name "myiothub"-SkuName</span><span class="sxs-lookup"><span data-stu-id="bc9ea-113">$psCloudToDeviceProperties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties -Property @{MaxDeliveryCount=20} $properties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties -Property @{CloudToDevice=$psCloudToDeviceProperties} New-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties</span></span>

## <span data-ttu-id="bc9ea-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bc9ea-114">PARAMETERS</span></span>

### <span data-ttu-id="bc9ea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc9ea-115">-DefaultProfile</span></span>
<span data-ttu-id="bc9ea-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="bc9ea-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc9ea-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="bc9ea-117">-Location</span></span>
<span data-ttu-id="bc9ea-118">Az a hely, ahol a IoT-hubot létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="bc9ea-118">Location where the IoT hub needs to be created.</span></span> 

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

### <span data-ttu-id="bc9ea-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bc9ea-119">-Name</span></span>
<span data-ttu-id="bc9ea-120">A IotHub neve</span><span class="sxs-lookup"><span data-stu-id="bc9ea-120">Name of the IotHub</span></span>

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

### <span data-ttu-id="bc9ea-121">-Tulajdonságok</span><span class="sxs-lookup"><span data-stu-id="bc9ea-121">-Properties</span></span>
<span data-ttu-id="bc9ea-122">A IoT-központ tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="bc9ea-122">Properties of the IoT hub.</span></span> 

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

### <span data-ttu-id="bc9ea-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc9ea-123">-ResourceGroupName</span></span>
<span data-ttu-id="bc9ea-124">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="bc9ea-124">Resource Group Name</span></span>

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

### <span data-ttu-id="bc9ea-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="bc9ea-125">-SkuName</span></span>
<span data-ttu-id="bc9ea-126">A SKU neve</span><span class="sxs-lookup"><span data-stu-id="bc9ea-126">Name of the sku</span></span>

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

### <span data-ttu-id="bc9ea-127">-Egységek</span><span class="sxs-lookup"><span data-stu-id="bc9ea-127">-Units</span></span>
<span data-ttu-id="bc9ea-128">Egységek száma</span><span class="sxs-lookup"><span data-stu-id="bc9ea-128">Number of units</span></span>

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

### <span data-ttu-id="bc9ea-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bc9ea-129">-Confirm</span></span>
<span data-ttu-id="bc9ea-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bc9ea-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc9ea-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc9ea-131">-WhatIf</span></span>
<span data-ttu-id="bc9ea-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bc9ea-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc9ea-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bc9ea-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc9ea-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc9ea-134">CommonParameters</span></span>
<span data-ttu-id="bc9ea-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bc9ea-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc9ea-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc9ea-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc9ea-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc9ea-137">INPUTS</span></span>

### <span data-ttu-id="bc9ea-138">System. String</span><span class="sxs-lookup"><span data-stu-id="bc9ea-138">System.String</span></span>

## <span data-ttu-id="bc9ea-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc9ea-139">OUTPUTS</span></span>

### <span data-ttu-id="bc9ea-140">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="bc9ea-140">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="bc9ea-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bc9ea-141">NOTES</span></span>

## <span data-ttu-id="bc9ea-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bc9ea-142">RELATED LINKS</span></span>
