---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/get-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveResource.md
ms.openlocfilehash: e0ce7e46e8105048d58ee8a4334eaf098b40399c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377885"
---
# <span data-ttu-id="407dc-101">Get-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="407dc-101">Get-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="407dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="407dc-102">SYNOPSIS</span></span>
<span data-ttu-id="407dc-103">Az Áthelyezési erőforrást kapja meg.</span><span class="sxs-lookup"><span data-stu-id="407dc-103">Gets the Move Resource.</span></span>

## <span data-ttu-id="407dc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="407dc-104">SYNTAX</span></span>

### <span data-ttu-id="407dc-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="407dc-105">List (Default)</span></span>
```
Get-AzResourceMoverMoveResource -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="407dc-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="407dc-106">Get</span></span>
```
Get-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="407dc-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="407dc-107">DESCRIPTION</span></span>
<span data-ttu-id="407dc-108">Az Áthelyezési erőforrást kapja meg.</span><span class="sxs-lookup"><span data-stu-id="407dc-108">Gets the Move Resource.</span></span>

## <span data-ttu-id="407dc-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="407dc-109">EXAMPLES</span></span>

### <span data-ttu-id="407dc-110">1. példa: Az Áthelyezés gyűjtemény összes erőforrásának részletei.</span><span class="sxs-lookup"><span data-stu-id="407dc-110">Example 1: Get details of all the resources in the Move collection.</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveResource -MoveCollectionName PS-centralus-westcentralus-demoRM -ResourceGroupName RG-MoveCollection-demoRM          

Code                                    :
DependsOn                               : {/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Networ
                                          k/networkInterfaces/psdemovm62,
                                          /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/PSDemoRM}
DependsOnOverride                       : {}
Detail                                  :
ExistingTargetId                        :
Id                                      : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/M
                                          icrosoft.Migrate/MoveCollections/PS-centralus-westcentralus-demoRM/MoveResources/PSDemoVM
Message                                 :
MoveStatusCode                          :
MoveStatusDetail                        :
MoveStatusJobName                       :
MoveStatusJobProgress                   :
MoveStatusMessage                       :
MoveStatusMoveState                     : PreparePending
MoveStatusTarget                        :
MoveStatusTargetId                      :
Name                                    : PSDemoVM
ProvisioningState                       : Succeeded
ResourceSettingResourceType             : Microsoft.Compute/virtualMachines
ResourceSettingTargetResourceName       : PSDemoVM
SourceId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Compute
                                          /virtualMachines/PSDemoVM
SourceResourceSettingResourceType       : Microsoft.Compute/virtualMachines
SourceResourceSettingTargetResourceName : PSDemoVM
Target                                  :
TargetId                                :
Type                                    :

Code                                    :
DependsOn                               : {/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.networ
                                          k/publicipaddresses/psdemovm-ip, /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/psd
                                          emorm/providers/Microsoft.Network/virtualNetworks/psdemorm-vnet, /subscriptions/e80eb9fa-c996-4435-aa32
                                          -5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg,
                                          /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/PSDemoRM}
DependsOnOverride                       : {}
Detail                                  :
ExistingTargetId                        :
Id                                      : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/M
                                          icrosoft.Migrate/MoveCollections/PS-centralus-westcentralus-demoRM/MoveResources/psdemovm62
Message                                 :
MoveStatusCode                          :
MoveStatusDetail                        :
MoveStatusJobName                       :
MoveStatusJobProgress                   :
MoveStatusMessage                       :
MoveStatusMoveState                     : MovePending
MoveStatusTarget                        :
MoveStatusTargetId                      :
Name                                    : psdemovm62
ProvisioningState                       : Succeeded
ResourceSettingResourceType             : Microsoft.Network/networkInterfaces
ResourceSettingTargetResourceName       : psdemovm62
SourceId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Network
                                          /networkInterfaces/psdemovm62
SourceResourceSettingResourceType       : Microsoft.Network/networkInterfaces
SourceResourceSettingTargetResourceName : psdemovm62
Target                                  :
TargetId                                :
Type                                    :

Code                                    :
DependsOn                               : {}
DependsOnOverride                       : {}
Detail                                  :
ExistingTargetId                        :
Id                                      : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/M
                                          icrosoft.Migrate/MoveCollections/PS-centralus-westcentralus-demoRM/MoveResources/psdemorm
Message                                 :
MoveStatusCode                          :
MoveStatusDetail                        :
MoveStatusJobName                       :
MoveStatusJobProgress                   :
MoveStatusMessage                       :
MoveStatusMoveState                     : CommitPending
MoveStatusTarget                        :
MoveStatusTargetId                      :
Name                                    : psdemorm
ProvisioningState                       : Succeeded
ResourceSettingResourceType             : resourceGroups
ResourceSettingTargetResourceName       : psdemorm2
SourceId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm
SourceResourceSettingResourceType       : resourceGroups
SourceResourceSettingTargetResourceName : psdemorm
Target                                  :
TargetId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/psdemorm2
Type                                    :

```

<span data-ttu-id="407dc-111">Részleteket olvashat az áthelyezési gyűjteményben rendelkezésre álló erőforrásokról.</span><span class="sxs-lookup"><span data-stu-id="407dc-111">Get details of all the resources in the move collection.</span></span>

### <span data-ttu-id="407dc-112">2. példa: Az áthelyezési gyűjtemény adott erőforrásainak részletei az erőforrás nevének áthelyezését használva.</span><span class="sxs-lookup"><span data-stu-id="407dc-112">Example 2: Get details of a specific resources in a Move collection using move resource name .</span></span>
```powershell
PS C:\> Get-AzResourceMoverMoveResource -MoveCollectionName PS-centralus-westcentralus-demoRM -ResourceGroupName RG-MoveCollection-demoRM -Name PSDemoVM   
                                                     
Code                                    :
DependsOn                               : {/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Networ
                                          k/networkInterfaces/psdemovm62,
                                          /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/PSDemoRM}
DependsOnOverride                       : {}
Detail                                  :
ExistingTargetId                        :
Id                                      : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/M
                                          icrosoft.Migrate/MoveCollections/PS-centralus-westcentralus-demoRM/MoveResources/PSDemoVM
Message                                 :
MoveStatusCode                          :
MoveStatusDetail                        :
MoveStatusJobName                       :
MoveStatusJobProgress                   :
MoveStatusMessage                       :
MoveStatusMoveState                     : PreparePending
MoveStatusTarget                        :
MoveStatusTargetId                      :
Name                                    : PSDemoVM
ProvisioningState                       : Succeeded
ResourceSettingResourceType             : Microsoft.Compute/virtualMachines
ResourceSettingTargetResourceName       : PSDemoVM
SourceId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Compute
                                          /virtualMachines/PSDemoVM
SourceResourceSettingResourceType       : Microsoft.Compute/virtualMachines
SourceResourceSettingTargetResourceName : PSDemoVM
Target                                  :
TargetId                                :
Type                                    :

```

<span data-ttu-id="407dc-113">Az Áthelyezés gyűjtemény adott erőforrásainak részletei az erőforrás nevének áthelyezését használva.</span><span class="sxs-lookup"><span data-stu-id="407dc-113">Get details of a specific resources in a Move collection using move resource name .</span></span>

### <span data-ttu-id="407dc-114">3. példa: Egy Áthelyezési gyűjtemény adott erőforrásainak részletei a következő szűrők használatával: SourceResourceName, SourceId, MoveState, IsResolveRequired, ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="407dc-114">Example 3:Get details of a specific resources in a Move collection using filters such as : SourceResourceName, SourceId, MoveState, IsResolveRequired, ProvisioningState</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveResource -MoveCollectionName PS-centralus-westcentralus-demoRM -ResourceGroupName RG-MoveCollection-demoRM -Filter "Properties/SourceResourceName eq 'PSDemoVM'"

Code                                    :
DependsOn                               : {/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Networ
                                          k/networkInterfaces/psdemovm62,
                                          /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/PSDemoRM}
DependsOnOverride                       : {}
Detail                                  :
ExistingTargetId                        :
Id                                      : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/M
                                          icrosoft.Migrate/MoveCollections/PS-centralus-westcentralus-demoRM/MoveResources/PSDemoVM
Message                                 :
MoveStatusCode                          :
MoveStatusDetail                        :
MoveStatusJobName                       :
MoveStatusJobProgress                   :
MoveStatusMessage                       :
MoveStatusMoveState                     : PreparePending
MoveStatusTarget                        :
MoveStatusTargetId                      :
Name                                    : PSDemoVM
ProvisioningState                       : Succeeded
ResourceSettingResourceType             : Microsoft.Compute/virtualMachines
ResourceSettingTargetResourceName       : PSDemoVM
SourceId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Compute
                                          /virtualMachines/PSDemoVM
SourceResourceSettingResourceType       : Microsoft.Compute/virtualMachines
SourceResourceSettingTargetResourceName : PSDemoVM
Target                                  :
TargetId                                :
Type                                    :

```

<span data-ttu-id="407dc-115">Részleteket olvashat egy áthelyezési gyűjtemény adott erőforrásairól egy szűrő (például armid, moveStatusMoveState(ellenőrzés) használatával stb.</span><span class="sxs-lookup"><span data-stu-id="407dc-115">Get details of a specific resources in a Move collection using filter such as armid ,moveStatusMoveState(verify) etc.</span></span>

## <span data-ttu-id="407dc-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="407dc-116">PARAMETERS</span></span>

### <span data-ttu-id="407dc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="407dc-117">-DefaultProfile</span></span>
<span data-ttu-id="407dc-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="407dc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="407dc-119">-Filter</span><span class="sxs-lookup"><span data-stu-id="407dc-119">-Filter</span></span>
<span data-ttu-id="407dc-120">A műveletre alkalmazandó szűrő.</span><span class="sxs-lookup"><span data-stu-id="407dc-120">The filter to apply on the operation.</span></span>
<span data-ttu-id="407dc-121">Használhatja például a $filter=Properties/ProvisioningState eq "Sikeres" parancsot.</span><span class="sxs-lookup"><span data-stu-id="407dc-121">For example, you can use $filter=Properties/ProvisioningState eq 'Succeeded'.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="407dc-122">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="407dc-122">-MoveCollectionName</span></span>
<span data-ttu-id="407dc-123">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="407dc-123">The Move Collection Name.</span></span>

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

### <span data-ttu-id="407dc-124">-Name</span><span class="sxs-lookup"><span data-stu-id="407dc-124">-Name</span></span>
<span data-ttu-id="407dc-125">Az Erőforrás neve áthelyezése 2010.</span><span class="sxs-lookup"><span data-stu-id="407dc-125">The Move Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: MoveResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="407dc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="407dc-126">-ResourceGroupName</span></span>
<span data-ttu-id="407dc-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="407dc-127">The Resource Group Name.</span></span>

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

### <span data-ttu-id="407dc-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="407dc-128">-SubscriptionId</span></span>
<span data-ttu-id="407dc-129">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="407dc-129">The Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="407dc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="407dc-130">CommonParameters</span></span>
<span data-ttu-id="407dc-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="407dc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="407dc-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="407dc-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="407dc-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="407dc-133">INPUTS</span></span>

## <span data-ttu-id="407dc-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="407dc-134">OUTPUTS</span></span>

### <span data-ttu-id="407dc-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveResource</span><span class="sxs-lookup"><span data-stu-id="407dc-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveResource</span></span>

## <span data-ttu-id="407dc-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="407dc-136">NOTES</span></span>

<span data-ttu-id="407dc-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="407dc-137">ALIASES</span></span>

## <span data-ttu-id="407dc-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="407dc-138">RELATED LINKS</span></span>

