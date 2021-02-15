---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: e82c540b946408671c424a1f86d3266a7e6d6906
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143570"
---
# <span data-ttu-id="f7174-101">Get-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f7174-101">Get-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="f7174-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7174-102">SYNOPSIS</span></span>
<span data-ttu-id="f7174-103">A JIT hálózati hozzáférési házirendek lekérte</span><span class="sxs-lookup"><span data-stu-id="f7174-103">Gets the JIT network access policies</span></span>

## <span data-ttu-id="f7174-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f7174-104">SYNTAX</span></span>

### <span data-ttu-id="f7174-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f7174-105">SubscriptionScope (Default)</span></span>
```
Get-AzJitNetworkAccessPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7174-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="f7174-106">ResourceGroupScope</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f7174-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="f7174-107">ResourceGroupLevelResource</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7174-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7174-108">ResourceId</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7174-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f7174-109">DESCRIPTION</span></span>
<span data-ttu-id="f7174-110">A Csak az ideje (JIT) hálózati hozzáférési házirendek segítségével meghatározhat egy házirendet, amely lehetővé teszi az egyszerű felhasználóknak, hogy ideiglenes hálózati kapcsolatot hozzanak létre a VIRTUÁLIS géphez.</span><span class="sxs-lookup"><span data-stu-id="f7174-110">Just In Time (JIT) network access policies let you define a policy the will allow simple users to create a temporary network connection to a VM.</span></span>
<span data-ttu-id="f7174-111">A házirend meghatározza, hogy milyen portok, protokollok és forrás IP-címek kérnek kapcsolatot a virtuális géphez, és hogy a kapcsolat automatikus lezárása előtt mennyi ideig tart a kapcsolat.</span><span class="sxs-lookup"><span data-stu-id="f7174-111">The policy defines what ports, protocol and source IP addresses can request a connection to a VM and the max duration before the connection will be closed automatically.</span></span>
<span data-ttu-id="f7174-112">A házirendben az ezzel a házirendvel kapcsolatos kapcsolatkérést is láthatja.</span><span class="sxs-lookup"><span data-stu-id="f7174-112">In the policy you can also see the connection request that were made with this policy.</span></span> 

## <span data-ttu-id="f7174-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f7174-113">EXAMPLES</span></span>

### <span data-ttu-id="f7174-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="f7174-114">Example 1</span></span>
```powershell
PS C:\> Get-AzJitNetworkAccessPolicy
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/northeurope/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="f7174-115">A JIT-hálózat hozzáférési rendreinek lekérte egy előfizetésre</span><span class="sxs-lookup"><span data-stu-id="f7174-115">Get all the JIT network access polices on a subscription</span></span>

### <span data-ttu-id="f7174-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="f7174-116">Example 2</span></span>
```powershell
PS C:\> Get-AzJitNetworkAccessPolicy -ResourceGroupName "myService1"
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/northeurope/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="f7174-117">A JIT-hálózat hozzáférésének összes rendrei a "myService1" erőforráscsoportban</span><span class="sxs-lookup"><span data-stu-id="f7174-117">Get all the JIT network access polices on the "myService1" resource group</span></span>

### <span data-ttu-id="f7174-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="f7174-118">Example 3</span></span>
```powershell
PS C:\> Get-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="f7174-119">Egy adott JIT-hálózati hozzáférési házirendet kap</span><span class="sxs-lookup"><span data-stu-id="f7174-119">Gets a specific JIT network access policy</span></span>

## <span data-ttu-id="f7174-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7174-120">PARAMETERS</span></span>

### <span data-ttu-id="f7174-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7174-121">-DefaultProfile</span></span>
<span data-ttu-id="f7174-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f7174-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7174-123">-Location</span><span class="sxs-lookup"><span data-stu-id="f7174-123">-Location</span></span>
<span data-ttu-id="f7174-124">Hely.</span><span class="sxs-lookup"><span data-stu-id="f7174-124">Location.</span></span>

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

### <span data-ttu-id="f7174-125">-Name</span><span class="sxs-lookup"><span data-stu-id="f7174-125">-Name</span></span>
<span data-ttu-id="f7174-126">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f7174-126">Resource name.</span></span>

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

### <span data-ttu-id="f7174-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7174-127">-ResourceGroupName</span></span>
<span data-ttu-id="f7174-128">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f7174-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7174-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7174-129">-ResourceId</span></span>
<span data-ttu-id="f7174-130">A jit Network Access Policy erőforrás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f7174-130">The resource id of the jit Network Access Policy resource.</span></span>

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

### <span data-ttu-id="f7174-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7174-131">CommonParameters</span></span>
<span data-ttu-id="f7174-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7174-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7174-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7174-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7174-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f7174-134">INPUTS</span></span>

### <span data-ttu-id="f7174-135">System.String</span><span class="sxs-lookup"><span data-stu-id="f7174-135">System.String</span></span>

## <span data-ttu-id="f7174-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7174-136">OUTPUTS</span></span>

### <span data-ttu-id="f7174-137">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f7174-137">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="f7174-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f7174-138">NOTES</span></span>

## <span data-ttu-id="f7174-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f7174-139">RELATED LINKS</span></span>
