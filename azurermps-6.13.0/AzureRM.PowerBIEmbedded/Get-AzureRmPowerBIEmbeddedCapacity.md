---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Get-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Get-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 4e15a9490fcaa41c77bb4ba822429646c6e45952
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493993"
---
# <span data-ttu-id="840d2-101">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="840d2-101">Get-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="840d2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="840d2-102">SYNOPSIS</span></span>
<span data-ttu-id="840d2-103">A PowerBI beágyazott kapacitásainak részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="840d2-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="840d2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="840d2-104">SYNTAX</span></span>

### <span data-ttu-id="840d2-105">ByCapacityOrResourceGroupOrSubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="840d2-105">ByCapacityOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzureRmPowerBIEmbeddedCapacity [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="840d2-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="840d2-106">ByResourceId</span></span>
```
Get-AzureRmPowerBIEmbeddedCapacity -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="840d2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="840d2-107">DESCRIPTION</span></span>
<span data-ttu-id="840d2-108">A Get-AzureRmPowerBIEmbeddedCapacity parancsmag a PowerBI beágyazott kapacitásának részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="840d2-108">The Get-AzureRmPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="840d2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="840d2-109">EXAMPLES</span></span>

### <span data-ttu-id="840d2-110">Példa 1: erőforráscsoport-kapacitások beolvasása</span><span class="sxs-lookup"><span data-stu-id="840d2-110">Example 1: Get resource group capacities</span></span>
```
PS C:\>Get-AzureRmPowerBIEmbeddedCapacity -ResourceGroupName "testRG"
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}

Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/mycapacity
ResourceGroup          : testRG
Name                   : mycapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A4
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="840d2-111">Ez a parancs beilleszti az összes Azure PowerBI beágyazott kapacitást a testRG nevű erőforráscsoport erőforrás csoportjába.</span><span class="sxs-lookup"><span data-stu-id="840d2-111">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="840d2-112">2. példa: kapacitás beszerzése</span><span class="sxs-lookup"><span data-stu-id="840d2-112">Example 2: Get a capacity</span></span>
```
PS C:\>Get-AzureRmPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity"
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="840d2-113">Ez a parancs beilleszti az Azure PowerBI testcapacity nevű beágyazott kapacitást a testRG nevű erőforrás csoportba.</span><span class="sxs-lookup"><span data-stu-id="840d2-113">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="840d2-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="840d2-114">PARAMETERS</span></span>

### <span data-ttu-id="840d2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="840d2-115">-DefaultProfile</span></span>
<span data-ttu-id="840d2-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="840d2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="840d2-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="840d2-117">-Name</span></span>
<span data-ttu-id="840d2-118">A PowerBI beágyazott kapacitásának neve</span><span class="sxs-lookup"><span data-stu-id="840d2-118">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: ByCapacityOrResourceGroupOrSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="840d2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="840d2-119">-ResourceGroupName</span></span>
<span data-ttu-id="840d2-120">Annak az Azure-erőforrás-csoportnak a neve, amelyhez a kapacitás tartozik</span><span class="sxs-lookup"><span data-stu-id="840d2-120">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: ByCapacityOrResourceGroupOrSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="840d2-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="840d2-121">-ResourceId</span></span>
<span data-ttu-id="840d2-122">Azure Resource ID</span><span class="sxs-lookup"><span data-stu-id="840d2-122">Azure resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="840d2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="840d2-123">CommonParameters</span></span>
<span data-ttu-id="840d2-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="840d2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="840d2-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="840d2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="840d2-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="840d2-126">INPUTS</span></span>

### <span data-ttu-id="840d2-127">System. String</span><span class="sxs-lookup"><span data-stu-id="840d2-127">System.String</span></span>

## <span data-ttu-id="840d2-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="840d2-128">OUTPUTS</span></span>

### <span data-ttu-id="840d2-129">Microsoft. Azure. Command. PowerBI. models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="840d2-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="840d2-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="840d2-130">NOTES</span></span>

## <span data-ttu-id="840d2-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="840d2-131">RELATED LINKS</span></span>

[<span data-ttu-id="840d2-132">Új – AzureRmPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="840d2-132">New-AzureRmPowerBIEmbeddedCapacity </span></span>](./New-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="840d2-133">Remove-AzureRmPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="840d2-133">Remove-AzureRmPowerBIEmbeddedCapacity </span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
