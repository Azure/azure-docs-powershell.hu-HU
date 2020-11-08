---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: c54f3df57739b4a68620aa1f7f3d700746369a60
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012481"
---
# <span data-ttu-id="d897d-101">Get-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d897d-101">Get-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="d897d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d897d-102">SYNOPSIS</span></span>
<span data-ttu-id="d897d-103">A JIT hálózati hozzáférési házirendek beolvasása</span><span class="sxs-lookup"><span data-stu-id="d897d-103">Gets the JIT network access policies</span></span>

## <span data-ttu-id="d897d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d897d-104">SYNTAX</span></span>

### <span data-ttu-id="d897d-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d897d-105">SubscriptionScope (Default)</span></span>
```
Get-AzJitNetworkAccessPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d897d-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="d897d-106">ResourceGroupScope</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d897d-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="d897d-107">ResourceGroupLevelResource</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d897d-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d897d-108">ResourceId</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d897d-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="d897d-109">DESCRIPTION</span></span>
<span data-ttu-id="d897d-110">Éppen időben (JIT) a hálózat-hozzáférési házirendek lehetővé teszik a szabályok definiálását, amely lehetővé teszi, hogy az egyszerű felhasználók ideiglenes hálózati kapcsolatot hozzanak létre egy VM-kapcsolattal.</span><span class="sxs-lookup"><span data-stu-id="d897d-110">Just In Time (JIT) network access policies let you define a policy the will allow simple users to create a temporary network connection to a VM.</span></span>
<span data-ttu-id="d897d-111">A házirend azt határozza meg, hogy a portok, a protokollok és a forrás IP-címei hogyan igényelhetnek kapcsolatot a VM-vel és a maximális időtartammal, mielőtt a kapcsolat automatikusan bezárul.</span><span class="sxs-lookup"><span data-stu-id="d897d-111">The policy defines what ports, protocol and source IP addresses can request a connection to a VM and the max duration before the connection will be closed automatically.</span></span>
<span data-ttu-id="d897d-112">A házirendben megtekintheti az ezzel a házirenddel létrehozott kapcsolatkérelem-kérést is.</span><span class="sxs-lookup"><span data-stu-id="d897d-112">In the policy you can also see the connection request that were made with this policy.</span></span> 

## <span data-ttu-id="d897d-113">Példák</span><span class="sxs-lookup"><span data-stu-id="d897d-113">EXAMPLES</span></span>

### <span data-ttu-id="d897d-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d897d-114">Example 1</span></span>
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

<span data-ttu-id="d897d-115">Az összes JIT-hálózat hozzáférési rendőrének beszerzése előfizetéshez</span><span class="sxs-lookup"><span data-stu-id="d897d-115">Get all the JIT network access polices on a subscription</span></span>

### <span data-ttu-id="d897d-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="d897d-116">Example 2</span></span>
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

<span data-ttu-id="d897d-117">Az összes JIT-hálózati hozzáférési rendőr beszerzése a "myService1" erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="d897d-117">Get all the JIT network access polices on the "myService1" resource group</span></span>

### <span data-ttu-id="d897d-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="d897d-118">Example 3</span></span>
```powershell
PS C:\> Get-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="d897d-119">Meghatározott JIT-hálózati hozzáférési házirend beolvasása</span><span class="sxs-lookup"><span data-stu-id="d897d-119">Gets a specific JIT network access policy</span></span>

## <span data-ttu-id="d897d-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d897d-120">PARAMETERS</span></span>

### <span data-ttu-id="d897d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d897d-121">-DefaultProfile</span></span>
<span data-ttu-id="d897d-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d897d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d897d-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="d897d-123">-Location</span></span>
<span data-ttu-id="d897d-124">Helyre.</span><span class="sxs-lookup"><span data-stu-id="d897d-124">Location.</span></span>

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

### <span data-ttu-id="d897d-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d897d-125">-Name</span></span>
<span data-ttu-id="d897d-126">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="d897d-126">Resource name.</span></span>

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

### <span data-ttu-id="d897d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d897d-127">-ResourceGroupName</span></span>
<span data-ttu-id="d897d-128">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="d897d-128">Resource group name.</span></span>

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

### <span data-ttu-id="d897d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d897d-129">-ResourceId</span></span>
<span data-ttu-id="d897d-130">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="d897d-130">Resource ID.</span></span>

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

### <span data-ttu-id="d897d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d897d-131">CommonParameters</span></span>
<span data-ttu-id="d897d-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d897d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d897d-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d897d-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d897d-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d897d-134">INPUTS</span></span>

### <span data-ttu-id="d897d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d897d-135">System.String</span></span>

## <span data-ttu-id="d897d-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d897d-136">OUTPUTS</span></span>

### <span data-ttu-id="d897d-137">Microsoft. Azure. commands. Security. models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d897d-137">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="d897d-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d897d-138">NOTES</span></span>

## <span data-ttu-id="d897d-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d897d-139">RELATED LINKS</span></span>
