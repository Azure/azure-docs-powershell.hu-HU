---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Start-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: cc25282105b8a45e75984ffbdc272743dd88220e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669219"
---
# <span data-ttu-id="592f7-101">Start-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="592f7-101">Start-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="592f7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="592f7-102">SYNOPSIS</span></span>
<span data-ttu-id="592f7-103">Ideiglenes hálózati hozzáférési kérést hív meg.</span><span class="sxs-lookup"><span data-stu-id="592f7-103">Invokes a temporary network access request.</span></span>

## <span data-ttu-id="592f7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="592f7-104">SYNTAX</span></span>

### <span data-ttu-id="592f7-105">ResourceGroupLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="592f7-105">ResourceGroupLevelResource (Default)</span></span>
```
Start-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="592f7-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="592f7-106">ResourceId</span></span>
```
Start-AzJitNetworkAccessPolicy -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="592f7-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="592f7-107">InputObject</span></span>
```
Start-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicyInitiateInputObject>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="592f7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="592f7-108">DESCRIPTION</span></span>
<span data-ttu-id="592f7-109">Ideiglenes hálózati hozzáférési kérést hív meg.</span><span class="sxs-lookup"><span data-stu-id="592f7-109">Invokes a temporary network access request.</span></span>
<span data-ttu-id="592f7-110">A kérés érvényesítése a beállított JIT-hálózat hozzáférési házirendjével történik, és ha a permittet, a felhasználó kérése szerint megnyílik egy hálózati kapcsolat.</span><span class="sxs-lookup"><span data-stu-id="592f7-110">The request is validated against the configured JIT network access policy and if permittet, opens up a network connection according to the user's request.</span></span>
<span data-ttu-id="592f7-111">A kérés a későbbi véleményezéshez loged válik, és a megadott időtartam túllépése után megszűnik.</span><span class="sxs-lookup"><span data-stu-id="592f7-111">The request will be loged in the policy for later review and will be terminated when the specified duration will be exceeded.</span></span>

## <span data-ttu-id="592f7-112">Példák</span><span class="sxs-lookup"><span data-stu-id="592f7-112">EXAMPLES</span></span>

### <span data-ttu-id="592f7-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="592f7-113">Example 1</span></span>
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

<span data-ttu-id="592f7-114">Megnyit egy hálózati kapcsolatot a megadott kapcsolatkérelem-adatforrásnak megfelelően.</span><span class="sxs-lookup"><span data-stu-id="592f7-114">Opens up a network connection according to the specified connection request data.</span></span>

## <span data-ttu-id="592f7-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="592f7-115">PARAMETERS</span></span>

### <span data-ttu-id="592f7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="592f7-116">-DefaultProfile</span></span>
<span data-ttu-id="592f7-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="592f7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="592f7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="592f7-118">-InputObject</span></span>
<span data-ttu-id="592f7-119">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="592f7-119">Input Object.</span></span>

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

### <span data-ttu-id="592f7-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="592f7-120">-Location</span></span>
<span data-ttu-id="592f7-121">Helyre.</span><span class="sxs-lookup"><span data-stu-id="592f7-121">Location.</span></span>

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

### <span data-ttu-id="592f7-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="592f7-122">-Name</span></span>
<span data-ttu-id="592f7-123">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="592f7-123">Resource name.</span></span>

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

### <span data-ttu-id="592f7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="592f7-124">-ResourceGroupName</span></span>
<span data-ttu-id="592f7-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="592f7-125">Resource group name.</span></span>

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

### <span data-ttu-id="592f7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="592f7-126">-ResourceId</span></span>
<span data-ttu-id="592f7-127">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="592f7-127">Resource ID.</span></span>

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

### <span data-ttu-id="592f7-128">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="592f7-128">-VirtualMachine</span></span>
<span data-ttu-id="592f7-129">Automatikus kiépítési.</span><span class="sxs-lookup"><span data-stu-id="592f7-129">Automatic Provisioning.</span></span>

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

### <span data-ttu-id="592f7-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="592f7-130">-Confirm</span></span>
<span data-ttu-id="592f7-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="592f7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="592f7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="592f7-132">-WhatIf</span></span>
<span data-ttu-id="592f7-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="592f7-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="592f7-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="592f7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="592f7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="592f7-135">CommonParameters</span></span>
<span data-ttu-id="592f7-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="592f7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="592f7-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="592f7-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="592f7-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="592f7-138">INPUTS</span></span>

### <span data-ttu-id="592f7-139">System. String</span><span class="sxs-lookup"><span data-stu-id="592f7-139">System.String</span></span>

### <span data-ttu-id="592f7-140">Microsoft. Azure. Command. Security. parancsmagok. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicyInitiateInputObject</span><span class="sxs-lookup"><span data-stu-id="592f7-140">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject</span></span>

## <span data-ttu-id="592f7-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="592f7-141">OUTPUTS</span></span>

### <span data-ttu-id="592f7-142">Microsoft. Azure. commands. Security. models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="592f7-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="592f7-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="592f7-143">NOTES</span></span>

## <span data-ttu-id="592f7-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="592f7-144">RELATED LINKS</span></span>
