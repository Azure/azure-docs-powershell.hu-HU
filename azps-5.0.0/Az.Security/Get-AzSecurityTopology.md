---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityTopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTopology.md
ms.openlocfilehash: ef984a1cbb1cf922ddc931a7924a5d39ba6c6a0b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187534"
---
# <span data-ttu-id="e8097-101">Get-AzSecurityTopology</span><span class="sxs-lookup"><span data-stu-id="e8097-101">Get-AzSecurityTopology</span></span>

## <span data-ttu-id="e8097-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e8097-102">SYNOPSIS</span></span>
<span data-ttu-id="e8097-103">Biztonsági topológiák listáját kapja egy előfizetésben</span><span class="sxs-lookup"><span data-stu-id="e8097-103">Gets a list of Security Topologies on a subscription</span></span>

## <span data-ttu-id="e8097-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e8097-104">SYNTAX</span></span>

### <span data-ttu-id="e8097-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e8097-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityTopology [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8097-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="e8097-106">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8097-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8097-107">ResourceId</span></span>
```
Get-AzSecurityTopology -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e8097-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e8097-108">DESCRIPTION</span></span>
<span data-ttu-id="e8097-109">Az Azure Security Center automatikusan felismeri a biztonsági topológiákat, ezzel a parancsmaggal megtekintheti a biztonsági topológiákat.</span><span class="sxs-lookup"><span data-stu-id="e8097-109">Security Topologies are automatically discovered by Azure Security Center, use this cmdlet to view security topologies.</span></span>

## <span data-ttu-id="e8097-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e8097-110">EXAMPLES</span></span>

### <span data-ttu-id="e8097-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e8097-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityTopology
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/topologies/virtualMachines
Name:   virtualMachines
Type:   Microsoft.Security/locations/topologies
CalculatedDateTime: 03-Jun-20 3:03:48 PM
TopologyResources:  /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="e8097-112">Az előfizetések minden biztonsági topológiájának megtekintése</span><span class="sxs-lookup"><span data-stu-id="e8097-112">View all security topologies in a subscription</span></span>

### <span data-ttu-id="e8097-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="e8097-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityTopology -ResourceGroupName "myService1" -Location "centralus" -Name "virtualMachines"
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/topologies/virtualMachines
Name:   virtualMachines
Type:   Microsoft.Security/locations/topologies
CalculatedDateTime: 03-Jun-20 3:03:48 PM
TopologyResources:  /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="e8097-114">Bizonyos biztonsági topológiák beszerzése</span><span class="sxs-lookup"><span data-stu-id="e8097-114">Get a specific security topologies</span></span>

## <span data-ttu-id="e8097-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e8097-115">PARAMETERS</span></span>

### <span data-ttu-id="e8097-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8097-116">-DefaultProfile</span></span>
<span data-ttu-id="e8097-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e8097-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8097-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="e8097-118">-Location</span></span>
<span data-ttu-id="e8097-119">Helyre.</span><span class="sxs-lookup"><span data-stu-id="e8097-119">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8097-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e8097-120">-Name</span></span>
<span data-ttu-id="e8097-121">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="e8097-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8097-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8097-122">-ResourceGroupName</span></span>
<span data-ttu-id="e8097-123">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="e8097-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8097-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8097-124">-ResourceId</span></span>
<span data-ttu-id="e8097-125">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="e8097-125">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8097-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8097-126">CommonParameters</span></span>
<span data-ttu-id="e8097-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e8097-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8097-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8097-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8097-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8097-129">INPUTS</span></span>

### <span data-ttu-id="e8097-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e8097-130">System.String</span></span>

## <span data-ttu-id="e8097-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8097-131">OUTPUTS</span></span>

### <span data-ttu-id="e8097-132">Microsoft. Azure. commands. Security. models. topológia. PSSecurityTopologies</span><span class="sxs-lookup"><span data-stu-id="e8097-132">Microsoft.Azure.Commands.Security.Models.Topology.PSSecurityTopologies</span></span>

## <span data-ttu-id="e8097-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e8097-133">NOTES</span></span>

## <span data-ttu-id="e8097-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e8097-134">RELATED LINKS</span></span>
