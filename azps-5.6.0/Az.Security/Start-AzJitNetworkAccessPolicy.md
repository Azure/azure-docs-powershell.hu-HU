---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Start-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 674f88a30ea036fc496cd6931b3d856a20a25c0a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936009"
---
# <span data-ttu-id="e7f03-101">Start-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e7f03-101">Start-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="e7f03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7f03-102">SYNOPSIS</span></span>
<span data-ttu-id="e7f03-103">Ideiglenes hálózati hozzáférési kérést hív meg.</span><span class="sxs-lookup"><span data-stu-id="e7f03-103">Invokes a temporary network access request.</span></span>

## <span data-ttu-id="e7f03-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e7f03-104">SYNTAX</span></span>

### <span data-ttu-id="e7f03-105">ResourceGroupLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e7f03-105">ResourceGroupLevelResource (Default)</span></span>
```
Start-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7f03-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7f03-106">ResourceId</span></span>
```
Start-AzJitNetworkAccessPolicy -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7f03-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="e7f03-107">InputObject</span></span>
```
Start-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicyInitiateInputObject>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7f03-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e7f03-108">DESCRIPTION</span></span>
<span data-ttu-id="e7f03-109">Ideiglenes hálózati hozzáférési kérést hív meg.</span><span class="sxs-lookup"><span data-stu-id="e7f03-109">Invokes a temporary network access request.</span></span>
<span data-ttu-id="e7f03-110">A kérés érvényesítése a konfigurált JIT hálózati hozzáférési házirend alapján történik, és ha engedélyezett, a felhasználó kérésének megfelelően hálózati kapcsolatot nyit meg.</span><span class="sxs-lookup"><span data-stu-id="e7f03-110">The request is validated against the configured JIT network access policy and if permitted, opens up a network connection according to the user's request.</span></span>
<span data-ttu-id="e7f03-111">A kérést a rendszer későbbi ellenőrzésre naplózza a házirendben, és a megadott időtartam túllépése esetén megszűnik.</span><span class="sxs-lookup"><span data-stu-id="e7f03-111">The request will be logged in the policy for later review and will be terminated when the specified duration will be exceeded.</span></span>

## <span data-ttu-id="e7f03-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e7f03-112">EXAMPLES</span></span>

### <span data-ttu-id="e7f03-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="e7f03-113">Example 1</span></span>
```powershell
$MyResource = Get-AzResource -Id /subscriptions/xxxxxxx-xxxxx-xxxxx-xxxxxxx/resourceGroups/PolicyDemo/providers/Microsoft.Compute/virtualMachines/PolicyDemoVM1
$JitPolicy = (@{
        id    = $MyResource.ResourceId; 
        ports = (@{
                number                     = 22
                endTimeUtc                 = Get-Date (Get-Date -AsUTC).AddHours(1) -Format O
                allowedSourceAddressPrefix = @($MyPublicIP) 
            })
    })
$ActivationVM = @($JitPolicy)
Start-AzJitNetworkAccessPolicy -ResourceGroupName $($MyResource.ResourceGroupName) -Location $MyResource.Location -Name "default" -VirtualMachine $ActivationVM

```

<span data-ttu-id="e7f03-114">Hálózati kapcsolatot nyit meg 1 órával a 22-es porton keresztül a nyilvános IP-címemről (ez nem jelenik meg).</span><span class="sxs-lookup"><span data-stu-id="e7f03-114">Opens up a network connection for 1 hour over port 22 from my public IP (not shown).</span></span>

## <span data-ttu-id="e7f03-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7f03-115">PARAMETERS</span></span>

### <span data-ttu-id="e7f03-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7f03-116">-DefaultProfile</span></span>
<span data-ttu-id="e7f03-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e7f03-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7f03-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7f03-118">-InputObject</span></span>
<span data-ttu-id="e7f03-119">Bemeneti objektum.</span><span class="sxs-lookup"><span data-stu-id="e7f03-119">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7f03-120">-Location</span><span class="sxs-lookup"><span data-stu-id="e7f03-120">-Location</span></span>
<span data-ttu-id="e7f03-121">Hely.</span><span class="sxs-lookup"><span data-stu-id="e7f03-121">Location.</span></span>

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

### <span data-ttu-id="e7f03-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e7f03-122">-Name</span></span>
<span data-ttu-id="e7f03-123">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="e7f03-123">Resource name.</span></span>

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

### <span data-ttu-id="e7f03-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7f03-124">-ResourceGroupName</span></span>
<span data-ttu-id="e7f03-125">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e7f03-125">Resource group name.</span></span>

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

### <span data-ttu-id="e7f03-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7f03-126">-ResourceId</span></span>
<span data-ttu-id="e7f03-127">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="e7f03-127">Resource ID.</span></span>

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

### <span data-ttu-id="e7f03-128">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e7f03-128">-VirtualMachine</span></span>
<span data-ttu-id="e7f03-129">Automatikus kiépítés.</span><span class="sxs-lookup"><span data-stu-id="e7f03-129">Automatic Provisioning.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7f03-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e7f03-130">-Confirm</span></span>
<span data-ttu-id="e7f03-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e7f03-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7f03-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7f03-132">-WhatIf</span></span>
<span data-ttu-id="e7f03-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e7f03-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e7f03-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e7f03-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7f03-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7f03-135">CommonParameters</span></span>
<span data-ttu-id="e7f03-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7f03-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7f03-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7f03-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7f03-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e7f03-138">INPUTS</span></span>

### <span data-ttu-id="e7f03-139">System.String</span><span class="sxs-lookup"><span data-stu-id="e7f03-139">System.String</span></span>

### <span data-ttu-id="e7f03-140">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject</span><span class="sxs-lookup"><span data-stu-id="e7f03-140">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject</span></span>

## <span data-ttu-id="e7f03-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7f03-141">OUTPUTS</span></span>

### <span data-ttu-id="e7f03-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e7f03-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="e7f03-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e7f03-143">NOTES</span></span>

## <span data-ttu-id="e7f03-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e7f03-144">RELATED LINKS</span></span>
