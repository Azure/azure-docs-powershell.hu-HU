---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: ce52463e9e983f3ad2483262775f5d4114370aa8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355793"
---
# <span data-ttu-id="7e781-101">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="7e781-101">Get-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="7e781-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e781-102">SYNOPSIS</span></span>
<span data-ttu-id="7e781-103">A Beágyazott PowerBI-kapacitás részleteinek lekérte.</span><span class="sxs-lookup"><span data-stu-id="7e781-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="7e781-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7e781-104">SYNTAX</span></span>

### <span data-ttu-id="7e781-105">ByCapacityOrResourceGroupOrSubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7e781-105">ByCapacityOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzPowerBIEmbeddedCapacity [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e781-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7e781-106">ByResourceId</span></span>
```
Get-AzPowerBIEmbeddedCapacity -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7e781-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7e781-107">DESCRIPTION</span></span>
<span data-ttu-id="7e781-108">A Get-AzPowerBIEmbeddedCapacity parancsmag megkapja a Beágyazott PowerBI-kapacitás részleteit.</span><span class="sxs-lookup"><span data-stu-id="7e781-108">The Get-AzPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="7e781-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7e781-109">EXAMPLES</span></span>

### <span data-ttu-id="7e781-110">1. példa: Erőforráscsoport-kapacitások lekérte</span><span class="sxs-lookup"><span data-stu-id="7e781-110">Example 1: Get resource group capacities</span></span>
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

<span data-ttu-id="7e781-111">Ez a parancs az Összes Azure PowerBI beágyazott kapacitást megkapja a testRG nevű erőforráscsoportban</span><span class="sxs-lookup"><span data-stu-id="7e781-111">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="7e781-112">2. példa: Kapacitás lekérte</span><span class="sxs-lookup"><span data-stu-id="7e781-112">Example 2: Get a capacity</span></span>
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

<span data-ttu-id="7e781-113">Ez a parancs az Azure PowerBI Beágyazott kapacitás nevű tesztkapacitást kapja meg a testRG nevű erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="7e781-113">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="7e781-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e781-114">PARAMETERS</span></span>

### <span data-ttu-id="7e781-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e781-115">-DefaultProfile</span></span>
<span data-ttu-id="7e781-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7e781-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e781-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7e781-117">-Name</span></span>
<span data-ttu-id="7e781-118">A Beágyazott PowerBI-kapacitás neve</span><span class="sxs-lookup"><span data-stu-id="7e781-118">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="7e781-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e781-119">-ResourceGroupName</span></span>
<span data-ttu-id="7e781-120">Annak az Azure-erőforráscsoportnak a neve, amelyhez a kapacitás tartozik</span><span class="sxs-lookup"><span data-stu-id="7e781-120">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="7e781-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e781-121">-ResourceId</span></span>
<span data-ttu-id="7e781-122">Azure-erőforrásazonosító</span><span class="sxs-lookup"><span data-stu-id="7e781-122">Azure resource ID</span></span>

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

### <span data-ttu-id="7e781-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e781-123">CommonParameters</span></span>
<span data-ttu-id="7e781-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e781-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e781-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e781-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e781-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7e781-126">INPUTS</span></span>

### <span data-ttu-id="7e781-127">System.String</span><span class="sxs-lookup"><span data-stu-id="7e781-127">System.String</span></span>

## <span data-ttu-id="7e781-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e781-128">OUTPUTS</span></span>

### <span data-ttu-id="7e781-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="7e781-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="7e781-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7e781-130">NOTES</span></span>

## <span data-ttu-id="7e781-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7e781-131">RELATED LINKS</span></span>

[<span data-ttu-id="7e781-132">New-AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="7e781-132">New-AzPowerBIEmbeddedCapacity </span></span>](./New-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="7e781-133">Remove-AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="7e781-133">Remove-AzPowerBIEmbeddedCapacity </span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
