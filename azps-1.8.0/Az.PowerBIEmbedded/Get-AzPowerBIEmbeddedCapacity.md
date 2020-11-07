---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 68d9e388238f9054ce56592186f686728e378000
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669819"
---
# <span data-ttu-id="b76a8-101">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="b76a8-101">Get-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="b76a8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b76a8-102">SYNOPSIS</span></span>
<span data-ttu-id="b76a8-103">A PowerBI beágyazott kapacitásainak részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b76a8-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="b76a8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b76a8-104">SYNTAX</span></span>

### <span data-ttu-id="b76a8-105">ByCapacityOrResourceGroupOrSubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b76a8-105">ByCapacityOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzPowerBIEmbeddedCapacity [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b76a8-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b76a8-106">ByResourceId</span></span>
```
Get-AzPowerBIEmbeddedCapacity -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b76a8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b76a8-107">DESCRIPTION</span></span>
<span data-ttu-id="b76a8-108">A Get-AzPowerBIEmbeddedCapacity parancsmag a PowerBI beágyazott kapacitásának részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b76a8-108">The Get-AzPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="b76a8-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b76a8-109">EXAMPLES</span></span>

### <span data-ttu-id="b76a8-110">Példa 1: erőforráscsoport-kapacitások beolvasása</span><span class="sxs-lookup"><span data-stu-id="b76a8-110">Example 1: Get resource group capacities</span></span>
```
PS C:\>Get-AzPowerBIEmbeddedCapacity -ResourceGroupName "testRG"
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

<span data-ttu-id="b76a8-111">Ez a parancs beilleszti az összes Azure PowerBI beágyazott kapacitást a testRG nevű erőforráscsoport erőforrás csoportjába.</span><span class="sxs-lookup"><span data-stu-id="b76a8-111">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="b76a8-112">2. példa: kapacitás beszerzése</span><span class="sxs-lookup"><span data-stu-id="b76a8-112">Example 2: Get a capacity</span></span>
```
PS C:\>Get-AzPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity"
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

<span data-ttu-id="b76a8-113">Ez a parancs beilleszti az Azure PowerBI testcapacity nevű beágyazott kapacitást a testRG nevű erőforrás csoportba.</span><span class="sxs-lookup"><span data-stu-id="b76a8-113">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="b76a8-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b76a8-114">PARAMETERS</span></span>

### <span data-ttu-id="b76a8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b76a8-115">-DefaultProfile</span></span>
<span data-ttu-id="b76a8-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b76a8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b76a8-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b76a8-117">-Name</span></span>
<span data-ttu-id="b76a8-118">A PowerBI beágyazott kapacitásának neve</span><span class="sxs-lookup"><span data-stu-id="b76a8-118">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="b76a8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b76a8-119">-ResourceGroupName</span></span>
<span data-ttu-id="b76a8-120">Annak az Azure-erőforrás-csoportnak a neve, amelyhez a kapacitás tartozik</span><span class="sxs-lookup"><span data-stu-id="b76a8-120">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="b76a8-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b76a8-121">-ResourceId</span></span>
<span data-ttu-id="b76a8-122">Azure Resource ID</span><span class="sxs-lookup"><span data-stu-id="b76a8-122">Azure resource ID</span></span>

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

### <span data-ttu-id="b76a8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b76a8-123">CommonParameters</span></span>
<span data-ttu-id="b76a8-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b76a8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b76a8-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b76a8-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b76a8-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b76a8-126">INPUTS</span></span>

### <span data-ttu-id="b76a8-127">System. String</span><span class="sxs-lookup"><span data-stu-id="b76a8-127">System.String</span></span>

## <span data-ttu-id="b76a8-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b76a8-128">OUTPUTS</span></span>

### <span data-ttu-id="b76a8-129">Microsoft. Azure. Command. PowerBI. models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="b76a8-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="b76a8-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b76a8-130">NOTES</span></span>

## <span data-ttu-id="b76a8-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b76a8-131">RELATED LINKS</span></span>

[<span data-ttu-id="b76a8-132">Új – AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="b76a8-132">New-AzPowerBIEmbeddedCapacity </span></span>](./New-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="b76a8-133">Remove-AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="b76a8-133">Remove-AzPowerBIEmbeddedCapacity </span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
