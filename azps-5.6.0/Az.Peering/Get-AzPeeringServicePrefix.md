---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServicePrefix.md
ms.openlocfilehash: 8b62189848583d11738a39555bc80ed0a52776fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937714"
---
# <span data-ttu-id="7a782-101">Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="7a782-101">Get-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="7a782-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a782-102">SYNOPSIS</span></span>
<span data-ttu-id="7a782-103">A társviszony-létesítő szolgáltatás előtagok listáját tartalmazza az előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="7a782-103">Gets a list of peering service prefixes for a subscription.</span></span>

## <span data-ttu-id="7a782-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7a782-104">SYNTAX</span></span>

### <span data-ttu-id="7a782-105">ByResourceGroupAndName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7a782-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringServicePrefix [-ResourceGroupName] <String> [-PeeringServiceName] <String> [-Name <String>]
 [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a782-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="7a782-106">InputObject</span></span>
```
Get-AzPeeringServicePrefix [-PeeringServiceObject] <PSPeeringService> [-Name <String>] [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a782-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7a782-107">ByResourceId</span></span>
```
Get-AzPeeringServicePrefix [-ResourceId] <String> [-Expand] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7a782-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7a782-108">DESCRIPTION</span></span>
<span data-ttu-id="7a782-109">Társviszony-létesítő szolgáltatáselőtagok listába sorolása a társviszony-létesítő szolgáltatásobjektumok esetén</span><span class="sxs-lookup"><span data-stu-id="7a782-109">List peering service prefixes for peering service objects</span></span>

## <span data-ttu-id="7a782-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7a782-110">EXAMPLES</span></span>

### <span data-ttu-id="7a782-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="7a782-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $name | Get-AzPeeringServicePrefix

Prefix                : 200.25.69.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes

Prefix                : 200.25.71.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix3463
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService4084/pre
                        fixes/myPrefix3463
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="7a782-112">A társviszony-létesítő szolgáltatás előtagját a pipázási parancsok alapján kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7a782-112">Gets the prefixes for a peering service based on piping commands.</span></span>

### <span data-ttu-id="7a782-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="7a782-113">Example 2</span></span>
```powershell
PS C:\> Get-AzPeeringServicePrefix -ResourceId $peeringServicePrefixResourceId 

Prefix                : 200.25.69.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="7a782-114">Egy társviszony-szolgáltatáshoz erőforrás-azonosító alapján adott előtagot kap.</span><span class="sxs-lookup"><span data-stu-id="7a782-114">Gets a specific prefix for a peering service by resource id.</span></span>

### <span data-ttu-id="7a782-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="7a782-115">Example 3</span></span>
```powershell
PS C:\> Get-AzPeeringServicePrefix -ResourceGroupName $rgName -PeeringServiceName $peeringServiceName -Name $prefixName

Prefix                : 200.25.69.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="7a782-116">Egy társviszony-szolgáltatáshoz erőforrás-azonosító alapján adott előtagot kap.</span><span class="sxs-lookup"><span data-stu-id="7a782-116">Gets a specific prefix for a peering service by resource id.</span></span>

### <span data-ttu-id="7a782-117">4. példa</span><span class="sxs-lookup"><span data-stu-id="7a782-117">Example 4</span></span>
```powershell
PS C:\> Get-AzPeeringServicePrefix -ResourceGroupName $rgName -PeeringServiceName $peeringServiceName -Name $prefixName -Expand

Prefix                : 10.2.6.0/24
PrefixValidationState : Failed
LearnedType           : None
ErrorMessage          :
Events                : {}
ProvisioningState     : Succeeded
Name                  : ps0
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService6616/pre
                        fixes/ps0
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="7a782-118">Egy kibontott attribútumokkal bővített társviszony-szolgáltatás adott előtagot kap</span><span class="sxs-lookup"><span data-stu-id="7a782-118">Gets a specific prefix for a peering service with expanded attributes</span></span>

## <span data-ttu-id="7a782-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a782-119">PARAMETERS</span></span>

### <span data-ttu-id="7a782-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a782-120">-DefaultProfile</span></span>
<span data-ttu-id="7a782-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7a782-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a782-122">-Kibontás</span><span class="sxs-lookup"><span data-stu-id="7a782-122">-Expand</span></span>
<span data-ttu-id="7a782-123">Társviszony-szolgáltatási előtag eseményeinek megtekintése</span><span class="sxs-lookup"><span data-stu-id="7a782-123">View the events for a peering service prefix</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a782-124">-Name</span><span class="sxs-lookup"><span data-stu-id="7a782-124">-Name</span></span>
<span data-ttu-id="7a782-125">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="7a782-125">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a782-126">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="7a782-126">-PeeringServiceName</span></span>
<span data-ttu-id="7a782-127">A társviszony-létesítő szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="7a782-127">The peering service name.</span></span> <span data-ttu-id="7a782-128">Egy New-AzPeeringService új társviszony-szolgáltatáshoz Get-AzPeeringService parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7a782-128">Use New-AzPeeringService cmdlet for a new peering service or Get-AzPeeringService for a list.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a782-129">-PeeringServiceObject</span><span class="sxs-lookup"><span data-stu-id="7a782-129">-PeeringServiceObject</span></span>
<span data-ttu-id="7a782-130">A Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="7a782-130">Use a Get-AzPeeringService</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a782-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a782-131">-ResourceGroupName</span></span>
<span data-ttu-id="7a782-132">Meglévő erőforráscsoport nevének létrehozása vagy használata.</span><span class="sxs-lookup"><span data-stu-id="7a782-132">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="7a782-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a782-133">-ResourceId</span></span>
<span data-ttu-id="7a782-134">Az erőforrás-azonosító karakterláncának neve.</span><span class="sxs-lookup"><span data-stu-id="7a782-134">The resource id string name.</span></span>

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

### <span data-ttu-id="7a782-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a782-135">CommonParameters</span></span>
<span data-ttu-id="7a782-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a782-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a782-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a782-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a782-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7a782-138">INPUTS</span></span>

### <span data-ttu-id="7a782-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="7a782-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

### <span data-ttu-id="7a782-140">System.String</span><span class="sxs-lookup"><span data-stu-id="7a782-140">System.String</span></span>

## <span data-ttu-id="7a782-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a782-141">OUTPUTS</span></span>

### <span data-ttu-id="7a782-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="7a782-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

## <span data-ttu-id="7a782-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7a782-143">NOTES</span></span>

## <span data-ttu-id="7a782-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7a782-144">RELATED LINKS</span></span>
