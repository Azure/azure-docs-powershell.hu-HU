---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Start-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: b992f3a41278ba66c54eeefc0b548eef76b50980
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186183"
---
# <span data-ttu-id="dd092-101">Start-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dd092-101">Start-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="dd092-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dd092-102">SYNOPSIS</span></span>
<span data-ttu-id="dd092-103">Ideiglenes hálózati hozzáférési kérést hív meg.</span><span class="sxs-lookup"><span data-stu-id="dd092-103">Invokes a temporary network access request.</span></span>

## <span data-ttu-id="dd092-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dd092-104">SYNTAX</span></span>

### <span data-ttu-id="dd092-105">ResourceGroupLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dd092-105">ResourceGroupLevelResource (Default)</span></span>
```
Start-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd092-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd092-106">ResourceId</span></span>
```
Start-AzJitNetworkAccessPolicy -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd092-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="dd092-107">InputObject</span></span>
```
Start-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicyInitiateInputObject>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd092-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="dd092-108">DESCRIPTION</span></span>
<span data-ttu-id="dd092-109">Ideiglenes hálózati hozzáférési kérést hív meg.</span><span class="sxs-lookup"><span data-stu-id="dd092-109">Invokes a temporary network access request.</span></span>
<span data-ttu-id="dd092-110">A kérés a beállított JIT-hálózat hozzáférési házirendjével van érvényesítve, és ha engedélyezve van, a felhasználó kérése szerint megnyílik egy hálózati kapcsolat.</span><span class="sxs-lookup"><span data-stu-id="dd092-110">The request is validated against the configured JIT network access policy and if permitted, opens up a network connection according to the user's request.</span></span>
<span data-ttu-id="dd092-111">A kérés a házirendbe kerül a későbbi véleményezésre, és a megadott időtartam túllépése után megszűnik.</span><span class="sxs-lookup"><span data-stu-id="dd092-111">The request will be logged in the policy for later review and will be terminated when the specified duration will be exceeded.</span></span>

## <span data-ttu-id="dd092-112">Példák</span><span class="sxs-lookup"><span data-stu-id="dd092-112">EXAMPLES</span></span>

### <span data-ttu-id="dd092-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="dd092-113">Example 1</span></span>
```powershell
PS C:\> Set-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -Kind "Basic" -VirtualMachine $vms

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.S
                    ecurity/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.
                    Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="dd092-114">Megnyit egy hálózati kapcsolatot a megadott kapcsolatkérelem-adatforrásnak megfelelően.</span><span class="sxs-lookup"><span data-stu-id="dd092-114">Opens up a network connection according to the specified connection request data.</span></span>

## <span data-ttu-id="dd092-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dd092-115">PARAMETERS</span></span>

### <span data-ttu-id="dd092-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd092-116">-DefaultProfile</span></span>
<span data-ttu-id="dd092-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dd092-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd092-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd092-118">-InputObject</span></span>
<span data-ttu-id="dd092-119">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="dd092-119">Input Object.</span></span>

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

### <span data-ttu-id="dd092-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="dd092-120">-Location</span></span>
<span data-ttu-id="dd092-121">Helyre.</span><span class="sxs-lookup"><span data-stu-id="dd092-121">Location.</span></span>

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

### <span data-ttu-id="dd092-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dd092-122">-Name</span></span>
<span data-ttu-id="dd092-123">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="dd092-123">Resource name.</span></span>

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

### <span data-ttu-id="dd092-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd092-124">-ResourceGroupName</span></span>
<span data-ttu-id="dd092-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="dd092-125">Resource group name.</span></span>

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

### <span data-ttu-id="dd092-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd092-126">-ResourceId</span></span>
<span data-ttu-id="dd092-127">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="dd092-127">Resource ID.</span></span>

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

### <span data-ttu-id="dd092-128">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="dd092-128">-VirtualMachine</span></span>
<span data-ttu-id="dd092-129">Automatikus kiépítési.</span><span class="sxs-lookup"><span data-stu-id="dd092-129">Automatic Provisioning.</span></span>

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

### <span data-ttu-id="dd092-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dd092-130">-Confirm</span></span>
<span data-ttu-id="dd092-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dd092-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd092-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd092-132">-WhatIf</span></span>
<span data-ttu-id="dd092-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dd092-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dd092-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dd092-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd092-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd092-135">CommonParameters</span></span>
<span data-ttu-id="dd092-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dd092-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd092-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="dd092-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd092-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd092-138">INPUTS</span></span>

### <span data-ttu-id="dd092-139">System. String</span><span class="sxs-lookup"><span data-stu-id="dd092-139">System.String</span></span>

### <span data-ttu-id="dd092-140">Microsoft. Azure. Command. Security. parancsmagok. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicyInitiateInputObject</span><span class="sxs-lookup"><span data-stu-id="dd092-140">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject</span></span>

## <span data-ttu-id="dd092-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd092-141">OUTPUTS</span></span>

### <span data-ttu-id="dd092-142">Microsoft. Azure. commands. Security. models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dd092-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="dd092-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dd092-143">NOTES</span></span>

## <span data-ttu-id="dd092-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dd092-144">RELATED LINKS</span></span>
