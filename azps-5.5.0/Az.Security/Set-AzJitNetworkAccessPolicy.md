---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 83aca2353102b85fd138422f249464b59a8666ca
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208239"
---
# <span data-ttu-id="8d5e2-101">Set-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8d5e2-101">Set-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="8d5e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d5e2-102">SYNOPSIS</span></span>
<span data-ttu-id="8d5e2-103">Frissíti a JIT-hálózati hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="8d5e2-103">Updates JIT network access policy.</span></span>

## <span data-ttu-id="8d5e2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8d5e2-104">SYNTAX</span></span>

```
Set-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyVirtualMachine[]> -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d5e2-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8d5e2-105">DESCRIPTION</span></span>
<span data-ttu-id="8d5e2-106">Frissíti a JIT-hálózati hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="8d5e2-106">Updates JIT network access policy.</span></span>

## <span data-ttu-id="8d5e2-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8d5e2-107">EXAMPLES</span></span>

### <span data-ttu-id="8d5e2-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="8d5e2-108">Example 1</span></span>
```powershell
PS C:\> Set-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -VirtualMachine $vmRules -Kind "Basic"

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="8d5e2-109">Új VM-szabályokkal frissíti a JIT hálózati hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="8d5e2-109">Updates a JIT network access policy with new VM rules.</span></span>

## <span data-ttu-id="8d5e2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d5e2-110">PARAMETERS</span></span>

### <span data-ttu-id="8d5e2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d5e2-111">-DefaultProfile</span></span>
<span data-ttu-id="8d5e2-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8d5e2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d5e2-113">-Kind</span><span class="sxs-lookup"><span data-stu-id="8d5e2-113">-Kind</span></span>
<span data-ttu-id="8d5e2-114">Jit Network Access Policy Kind.</span><span class="sxs-lookup"><span data-stu-id="8d5e2-114">Jit Network Access Policy Kind.</span></span>

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

### <span data-ttu-id="8d5e2-115">-Location</span><span class="sxs-lookup"><span data-stu-id="8d5e2-115">-Location</span></span>
<span data-ttu-id="8d5e2-116">Hely.</span><span class="sxs-lookup"><span data-stu-id="8d5e2-116">Location.</span></span>

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

### <span data-ttu-id="8d5e2-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8d5e2-117">-Name</span></span>
<span data-ttu-id="8d5e2-118">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="8d5e2-118">Resource name.</span></span>

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

### <span data-ttu-id="8d5e2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d5e2-119">-ResourceGroupName</span></span>
<span data-ttu-id="8d5e2-120">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8d5e2-120">Resource group name.</span></span>

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

### <span data-ttu-id="8d5e2-121">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="8d5e2-121">-VirtualMachine</span></span>
<span data-ttu-id="8d5e2-122">Virtuális gépek.</span><span class="sxs-lookup"><span data-stu-id="8d5e2-122">Virtual Machines.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyVirtualMachine[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d5e2-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d5e2-123">-Confirm</span></span>
<span data-ttu-id="8d5e2-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8d5e2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d5e2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d5e2-125">-WhatIf</span></span>
<span data-ttu-id="8d5e2-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8d5e2-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8d5e2-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8d5e2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d5e2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d5e2-128">CommonParameters</span></span>
<span data-ttu-id="8d5e2-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d5e2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d5e2-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8d5e2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d5e2-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8d5e2-131">INPUTS</span></span>

### <span data-ttu-id="8d5e2-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="8d5e2-132">None</span></span>

## <span data-ttu-id="8d5e2-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d5e2-133">OUTPUTS</span></span>

### <span data-ttu-id="8d5e2-134">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8d5e2-134">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="8d5e2-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8d5e2-135">NOTES</span></span>

## <span data-ttu-id="8d5e2-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8d5e2-136">RELATED LINKS</span></span>
