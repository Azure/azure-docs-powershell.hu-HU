---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: a316a59492034f0effd2d233ce386cbd6a256c75
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335441"
---
# <span data-ttu-id="f4728-101">Set-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f4728-101">Set-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="f4728-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4728-102">SYNOPSIS</span></span>
<span data-ttu-id="f4728-103">Frissíti a JIT-hálózati hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="f4728-103">Updates JIT network access policy.</span></span>

## <span data-ttu-id="f4728-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f4728-104">SYNTAX</span></span>

```
Set-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyVirtualMachine[]> -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4728-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f4728-105">DESCRIPTION</span></span>
<span data-ttu-id="f4728-106">Frissíti a JIT-hálózati hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="f4728-106">Updates JIT network access policy.</span></span>

## <span data-ttu-id="f4728-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f4728-107">EXAMPLES</span></span>

### <span data-ttu-id="f4728-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="f4728-108">Example 1</span></span>
```powershell
PS C:\> Set-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -VirtualMachine $vmRules -Kind "Basic"

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="f4728-109">Új VM-szabályokkal frissíti a JIT hálózati hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="f4728-109">Updates a JIT network access policy with new VM rules.</span></span>

## <span data-ttu-id="f4728-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4728-110">PARAMETERS</span></span>

### <span data-ttu-id="f4728-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4728-111">-DefaultProfile</span></span>
<span data-ttu-id="f4728-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f4728-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4728-113">-Kind</span><span class="sxs-lookup"><span data-stu-id="f4728-113">-Kind</span></span>
<span data-ttu-id="f4728-114">Kind.</span><span class="sxs-lookup"><span data-stu-id="f4728-114">Kind.</span></span>

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

### <span data-ttu-id="f4728-115">-Location</span><span class="sxs-lookup"><span data-stu-id="f4728-115">-Location</span></span>
<span data-ttu-id="f4728-116">Hely.</span><span class="sxs-lookup"><span data-stu-id="f4728-116">Location.</span></span>

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

### <span data-ttu-id="f4728-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f4728-117">-Name</span></span>
<span data-ttu-id="f4728-118">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f4728-118">Resource name.</span></span>

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

### <span data-ttu-id="f4728-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4728-119">-ResourceGroupName</span></span>
<span data-ttu-id="f4728-120">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f4728-120">Resource group name.</span></span>

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

### <span data-ttu-id="f4728-121">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f4728-121">-VirtualMachine</span></span>
<span data-ttu-id="f4728-122">Virtuális gépek.</span><span class="sxs-lookup"><span data-stu-id="f4728-122">Virtual Machines.</span></span>

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

### <span data-ttu-id="f4728-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4728-123">-Confirm</span></span>
<span data-ttu-id="f4728-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f4728-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4728-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4728-125">-WhatIf</span></span>
<span data-ttu-id="f4728-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f4728-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4728-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f4728-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4728-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4728-128">CommonParameters</span></span>
<span data-ttu-id="f4728-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4728-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4728-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4728-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4728-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f4728-131">INPUTS</span></span>

### <span data-ttu-id="f4728-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="f4728-132">None</span></span>

## <span data-ttu-id="f4728-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4728-133">OUTPUTS</span></span>

### <span data-ttu-id="f4728-134">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f4728-134">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="f4728-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f4728-135">NOTES</span></span>

## <span data-ttu-id="f4728-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4728-136">RELATED LINKS</span></span>
