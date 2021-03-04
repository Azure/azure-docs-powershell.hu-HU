---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityTopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTopology.md
ms.openlocfilehash: 0f6cbe88eaabb49a07bb0704f0d6ea547449a229
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938449"
---
# <span data-ttu-id="6f01d-101">Get-AzSecurityTopology</span><span class="sxs-lookup"><span data-stu-id="6f01d-101">Get-AzSecurityTopology</span></span>

## <span data-ttu-id="6f01d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f01d-102">SYNOPSIS</span></span>
<span data-ttu-id="6f01d-103">Biztonsági topológiák listáját kapja egy előfizetéshez</span><span class="sxs-lookup"><span data-stu-id="6f01d-103">Gets a list of Security Topologies on a subscription</span></span>

## <span data-ttu-id="6f01d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6f01d-104">SYNTAX</span></span>

### <span data-ttu-id="6f01d-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6f01d-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityTopology [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f01d-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="6f01d-106">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f01d-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f01d-107">ResourceId</span></span>
```
Get-AzSecurityTopology -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6f01d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6f01d-108">DESCRIPTION</span></span>
<span data-ttu-id="6f01d-109">A biztonsági topológiákat az Azure Biztonsági központ automatikusan felismeri, és ezzel a parancsmaggal megtekintheti a biztonsági topológiákat.</span><span class="sxs-lookup"><span data-stu-id="6f01d-109">Security Topologies are automatically discovered by Azure Security Center, use this cmdlet to view security topologies.</span></span>

## <span data-ttu-id="6f01d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6f01d-110">EXAMPLES</span></span>

### <span data-ttu-id="6f01d-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="6f01d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityTopology
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/topologies/virtualMachines
Name:   virtualMachines
Type:   Microsoft.Security/locations/topologies
CalculatedDateTime: 03-Jun-20 3:03:48 PM
TopologyResources:  /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="6f01d-112">Előfizetés biztonsági topológiáinak megtekintése</span><span class="sxs-lookup"><span data-stu-id="6f01d-112">View all security topologies in a subscription</span></span>

### <span data-ttu-id="6f01d-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="6f01d-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityTopology -ResourceGroupName "myService1" -Location "centralus" -Name "virtualMachines"
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/topologies/virtualMachines
Name:   virtualMachines
Type:   Microsoft.Security/locations/topologies
CalculatedDateTime: 03-Jun-20 3:03:48 PM
TopologyResources:  /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="6f01d-114">Adott biztonsági topológiák lekérte</span><span class="sxs-lookup"><span data-stu-id="6f01d-114">Get a specific security topologies</span></span>

## <span data-ttu-id="6f01d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f01d-115">PARAMETERS</span></span>

### <span data-ttu-id="6f01d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f01d-116">-DefaultProfile</span></span>
<span data-ttu-id="6f01d-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6f01d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f01d-118">-Location</span><span class="sxs-lookup"><span data-stu-id="6f01d-118">-Location</span></span>
<span data-ttu-id="6f01d-119">Hely.</span><span class="sxs-lookup"><span data-stu-id="6f01d-119">Location.</span></span>

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

### <span data-ttu-id="6f01d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6f01d-120">-Name</span></span>
<span data-ttu-id="6f01d-121">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="6f01d-121">Resource name.</span></span>

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

### <span data-ttu-id="6f01d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f01d-122">-ResourceGroupName</span></span>
<span data-ttu-id="6f01d-123">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6f01d-123">Resource group name.</span></span>

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

### <span data-ttu-id="6f01d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f01d-124">-ResourceId</span></span>
<span data-ttu-id="6f01d-125">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="6f01d-125">Resource ID.</span></span>

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

### <span data-ttu-id="6f01d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f01d-126">CommonParameters</span></span>
<span data-ttu-id="6f01d-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f01d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f01d-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f01d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f01d-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6f01d-129">INPUTS</span></span>

### <span data-ttu-id="6f01d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="6f01d-130">System.String</span></span>

## <span data-ttu-id="6f01d-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f01d-131">OUTPUTS</span></span>

### <span data-ttu-id="6f01d-132">Microsoft.Azure.Commands.Security.Models.Topology.PSSecurityTopologyes</span><span class="sxs-lookup"><span data-stu-id="6f01d-132">Microsoft.Azure.Commands.Security.Models.Topology.PSSecurityTopologies</span></span>

## <span data-ttu-id="6f01d-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6f01d-133">NOTES</span></span>

## <span data-ttu-id="6f01d-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6f01d-134">RELATED LINKS</span></span>
