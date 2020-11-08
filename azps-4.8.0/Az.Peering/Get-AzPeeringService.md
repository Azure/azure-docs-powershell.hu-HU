---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
ms.openlocfilehash: 016701a762a87ec03912cda62dd5f436f1a45950
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182937"
---
# <span data-ttu-id="99eba-101">Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="99eba-101">Get-AzPeeringService</span></span>

## <span data-ttu-id="99eba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="99eba-102">SYNOPSIS</span></span>
<span data-ttu-id="99eba-103">Megtudhatja, hogy egyetlen objektumhoz tartozó társközi szolgáltatási objektumok listája</span><span class="sxs-lookup"><span data-stu-id="99eba-103">Get a list of peering service objects of a single object.</span></span>

## <span data-ttu-id="99eba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="99eba-104">SYNTAX</span></span>

### <span data-ttu-id="99eba-105">ByResourceGroupName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="99eba-105">ByResourceGroupName (Default)</span></span>
```
Get-AzPeeringService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="99eba-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="99eba-106">ByResourceGroupAndName</span></span>
```
Get-AzPeeringService [-ResourceGroupName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="99eba-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="99eba-107">ByResourceId</span></span>
```
Get-AzPeeringService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99eba-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="99eba-108">DESCRIPTION</span></span>
<span data-ttu-id="99eba-109">Az előfizetéshez kapcsolódó szolgáltatások megkeresése</span><span class="sxs-lookup"><span data-stu-id="99eba-109">Gets peering services for a subscription</span></span>

## <span data-ttu-id="99eba-110">Példák</span><span class="sxs-lookup"><span data-stu-id="99eba-110">EXAMPLES</span></span>

### <span data-ttu-id="99eba-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="99eba-111">Example 1</span></span>
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

<span data-ttu-id="99eba-112">Egy erőforráscsoport számára Kinyer egy egyenrangú szolgáltatást</span><span class="sxs-lookup"><span data-stu-id="99eba-112">Gets a peering service for a resource group</span></span>

### <span data-ttu-id="99eba-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="99eba-113">Example 2</span></span>
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

<span data-ttu-id="99eba-114">Egy erőforráscsoport és egy név társítására szolgáló szolgáltatás lekérdezése</span><span class="sxs-lookup"><span data-stu-id="99eba-114">Gets a peering service for a resource group and name</span></span>

### <span data-ttu-id="99eba-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="99eba-115">Example 3</span></span>
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

<span data-ttu-id="99eba-116">Erőforrás-azonosítóval rendelkező társközi szolgáltatás lekérdezése</span><span class="sxs-lookup"><span data-stu-id="99eba-116">Gets a peering service by resource id</span></span>

## <span data-ttu-id="99eba-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="99eba-117">PARAMETERS</span></span>

### <span data-ttu-id="99eba-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99eba-118">-DefaultProfile</span></span>
<span data-ttu-id="99eba-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="99eba-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99eba-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="99eba-120">-Name</span></span>
<span data-ttu-id="99eba-121">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="99eba-121">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="99eba-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99eba-122">-ResourceGroupName</span></span>
<span data-ttu-id="99eba-123">A meglévő erőforráscsoport nevének létrehozása vagy használata.</span><span class="sxs-lookup"><span data-stu-id="99eba-123">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="99eba-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99eba-124">-ResourceId</span></span>
<span data-ttu-id="99eba-125">Az erőforrás-azonosító karakterlánc neve.</span><span class="sxs-lookup"><span data-stu-id="99eba-125">The resource id string name.</span></span>

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

### <span data-ttu-id="99eba-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99eba-126">CommonParameters</span></span>
<span data-ttu-id="99eba-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="99eba-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99eba-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="99eba-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99eba-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="99eba-129">INPUTS</span></span>

### <span data-ttu-id="99eba-130">System. String</span><span class="sxs-lookup"><span data-stu-id="99eba-130">System.String</span></span>

## <span data-ttu-id="99eba-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="99eba-131">OUTPUTS</span></span>

### <span data-ttu-id="99eba-132">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="99eba-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="99eba-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="99eba-133">NOTES</span></span>

## <span data-ttu-id="99eba-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="99eba-134">RELATED LINKS</span></span>
