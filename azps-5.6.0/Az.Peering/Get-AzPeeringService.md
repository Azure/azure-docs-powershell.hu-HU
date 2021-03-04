---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
ms.openlocfilehash: 4ce8e54b2ee5f43b9196263af5285af826aa9d01
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937729"
---
# <span data-ttu-id="a0645-101">Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="a0645-101">Get-AzPeeringService</span></span>

## <span data-ttu-id="a0645-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0645-102">SYNOPSIS</span></span>
<span data-ttu-id="a0645-103">Egyetlen objektum társviszony-szolgáltatási objektumának listájának lekérte.</span><span class="sxs-lookup"><span data-stu-id="a0645-103">Get a list of peering service objects of a single object.</span></span>

## <span data-ttu-id="a0645-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a0645-104">SYNTAX</span></span>

### <span data-ttu-id="a0645-105">ByResourceGroupName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a0645-105">ByResourceGroupName (Default)</span></span>
```
Get-AzPeeringService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a0645-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="a0645-106">ByResourceGroupAndName</span></span>
```
Get-AzPeeringService [-ResourceGroupName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a0645-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a0645-107">ByResourceId</span></span>
```
Get-AzPeeringService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0645-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a0645-108">DESCRIPTION</span></span>
<span data-ttu-id="a0645-109">Társviszony-létesítő szolgáltatásokat kap egy előfizetéshez</span><span class="sxs-lookup"><span data-stu-id="a0645-109">Gets peering services for a subscription</span></span>

## <span data-ttu-id="a0645-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a0645-110">EXAMPLES</span></span>

### <span data-ttu-id="a0645-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="a0645-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService3990
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService3990
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="a0645-112">Társviszony-létesítő szolgáltatást kap egy erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="a0645-112">Gets a peering service for a resource group</span></span>

### <span data-ttu-id="a0645-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="a0645-113">Example 2</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $name

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="a0645-114">Társviszony-létesítő szolgáltatást kap egy erőforráscsoporthoz és egy névhez</span><span class="sxs-lookup"><span data-stu-id="a0645-114">Gets a peering service for a resource group and name</span></span>

### <span data-ttu-id="a0645-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="a0645-115">Example 3</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceId $rid

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="a0645-116">Társviszony-létesítő szolgáltatást kap erőforrás-azonosító alapján</span><span class="sxs-lookup"><span data-stu-id="a0645-116">Gets a peering service by resource id</span></span>

## <span data-ttu-id="a0645-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0645-117">PARAMETERS</span></span>

### <span data-ttu-id="a0645-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0645-118">-DefaultProfile</span></span>
<span data-ttu-id="a0645-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a0645-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0645-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a0645-120">-Name</span></span>
<span data-ttu-id="a0645-121">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="a0645-121">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0645-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0645-122">-ResourceGroupName</span></span>
<span data-ttu-id="a0645-123">Meglévő erőforráscsoport nevének létrehozása vagy használata.</span><span class="sxs-lookup"><span data-stu-id="a0645-123">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0645-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0645-124">-ResourceId</span></span>
<span data-ttu-id="a0645-125">Az erőforrás-azonosító karakterláncának neve.</span><span class="sxs-lookup"><span data-stu-id="a0645-125">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0645-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0645-126">CommonParameters</span></span>
<span data-ttu-id="a0645-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0645-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0645-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a0645-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0645-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a0645-129">INPUTS</span></span>

### <span data-ttu-id="a0645-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a0645-130">System.String</span></span>

## <span data-ttu-id="a0645-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0645-131">OUTPUTS</span></span>

### <span data-ttu-id="a0645-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="a0645-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="a0645-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a0645-133">NOTES</span></span>

## <span data-ttu-id="a0645-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a0645-134">RELATED LINKS</span></span>
