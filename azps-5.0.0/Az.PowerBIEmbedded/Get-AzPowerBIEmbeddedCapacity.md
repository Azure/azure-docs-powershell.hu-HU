---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: ce52463e9e983f3ad2483262775f5d4114370aa8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194205"
---
# <span data-ttu-id="01f25-101">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="01f25-101">Get-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="01f25-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="01f25-102">SYNOPSIS</span></span>
<span data-ttu-id="01f25-103">A PowerBI beágyazott kapacitásainak részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="01f25-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="01f25-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="01f25-104">SYNTAX</span></span>

### <span data-ttu-id="01f25-105">ByCapacityOrResourceGroupOrSubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="01f25-105">ByCapacityOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzPowerBIEmbeddedCapacity [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01f25-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="01f25-106">ByResourceId</span></span>
```
Get-AzPowerBIEmbeddedCapacity -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="01f25-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="01f25-107">DESCRIPTION</span></span>
<span data-ttu-id="01f25-108">A Get-AzPowerBIEmbeddedCapacity parancsmag a PowerBI beágyazott kapacitásának részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="01f25-108">The Get-AzPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="01f25-109">Példák</span><span class="sxs-lookup"><span data-stu-id="01f25-109">EXAMPLES</span></span>

### <span data-ttu-id="01f25-110">Példa 1: erőforráscsoport-kapacitások beolvasása</span><span class="sxs-lookup"><span data-stu-id="01f25-110">Example 1: Get resource group capacities</span></span>
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

<span data-ttu-id="01f25-111">Ez a parancs beilleszti az összes Azure PowerBI beágyazott kapacitást a testRG nevű erőforráscsoport erőforrás csoportjába.</span><span class="sxs-lookup"><span data-stu-id="01f25-111">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="01f25-112">2. példa: kapacitás beszerzése</span><span class="sxs-lookup"><span data-stu-id="01f25-112">Example 2: Get a capacity</span></span>
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

<span data-ttu-id="01f25-113">Ez a parancs beilleszti az Azure PowerBI testcapacity nevű beágyazott kapacitást a testRG nevű erőforrás csoportba.</span><span class="sxs-lookup"><span data-stu-id="01f25-113">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="01f25-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="01f25-114">PARAMETERS</span></span>

### <span data-ttu-id="01f25-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01f25-115">-DefaultProfile</span></span>
<span data-ttu-id="01f25-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="01f25-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01f25-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="01f25-117">-Name</span></span>
<span data-ttu-id="01f25-118">A PowerBI beágyazott kapacitásának neve</span><span class="sxs-lookup"><span data-stu-id="01f25-118">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="01f25-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01f25-119">-ResourceGroupName</span></span>
<span data-ttu-id="01f25-120">Annak az Azure-erőforrás-csoportnak a neve, amelyhez a kapacitás tartozik</span><span class="sxs-lookup"><span data-stu-id="01f25-120">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="01f25-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01f25-121">-ResourceId</span></span>
<span data-ttu-id="01f25-122">Azure Resource ID</span><span class="sxs-lookup"><span data-stu-id="01f25-122">Azure resource ID</span></span>

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

### <span data-ttu-id="01f25-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01f25-123">CommonParameters</span></span>
<span data-ttu-id="01f25-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="01f25-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01f25-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01f25-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01f25-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="01f25-126">INPUTS</span></span>

### <span data-ttu-id="01f25-127">System. String</span><span class="sxs-lookup"><span data-stu-id="01f25-127">System.String</span></span>

## <span data-ttu-id="01f25-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="01f25-128">OUTPUTS</span></span>

### <span data-ttu-id="01f25-129">Microsoft. Azure. Command. PowerBI. models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="01f25-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="01f25-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="01f25-130">NOTES</span></span>

## <span data-ttu-id="01f25-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="01f25-131">RELATED LINKS</span></span>

[<span data-ttu-id="01f25-132">Új – AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="01f25-132">New-AzPowerBIEmbeddedCapacity </span></span>](./New-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="01f25-133">Remove-AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="01f25-133">Remove-AzPowerBIEmbeddedCapacity </span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)