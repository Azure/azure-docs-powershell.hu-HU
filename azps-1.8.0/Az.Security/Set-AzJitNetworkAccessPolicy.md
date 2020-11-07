---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: ddb9bc19e852ae482dbbf687966c5f73f0a0a1d3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669233"
---
# <span data-ttu-id="20d74-101">Set-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="20d74-101">Set-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="20d74-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="20d74-102">SYNOPSIS</span></span>
<span data-ttu-id="20d74-103">A JIT-hálózat elérési házirendjének frissítése</span><span class="sxs-lookup"><span data-stu-id="20d74-103">Updates JIT network access policy.</span></span>

## <span data-ttu-id="20d74-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="20d74-104">SYNTAX</span></span>

```
Set-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyVirtualMachine[]> -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20d74-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="20d74-105">DESCRIPTION</span></span>
<span data-ttu-id="20d74-106">A JIT-hálózat elérési házirendjének frissítése</span><span class="sxs-lookup"><span data-stu-id="20d74-106">Updates JIT network access policy.</span></span>

## <span data-ttu-id="20d74-107">Példák</span><span class="sxs-lookup"><span data-stu-id="20d74-107">EXAMPLES</span></span>

### <span data-ttu-id="20d74-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="20d74-108">Example 1</span></span>
```powershell
PS C:\> Set-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -VirtualMachine $vmRules -Kind "Basic"

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="20d74-109">A JIT-hálózat hozzáférési házirendjének frissítése új VM-szabályokkal.</span><span class="sxs-lookup"><span data-stu-id="20d74-109">Updates a JIT network access policy with new VM rules.</span></span>

## <span data-ttu-id="20d74-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="20d74-110">PARAMETERS</span></span>

### <span data-ttu-id="20d74-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20d74-111">-DefaultProfile</span></span>
<span data-ttu-id="20d74-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="20d74-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20d74-113">-Kind</span><span class="sxs-lookup"><span data-stu-id="20d74-113">-Kind</span></span>
<span data-ttu-id="20d74-114">Típusú.</span><span class="sxs-lookup"><span data-stu-id="20d74-114">Kind.</span></span>

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

### <span data-ttu-id="20d74-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="20d74-115">-Location</span></span>
<span data-ttu-id="20d74-116">Helyre.</span><span class="sxs-lookup"><span data-stu-id="20d74-116">Location.</span></span>

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

### <span data-ttu-id="20d74-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="20d74-117">-Name</span></span>
<span data-ttu-id="20d74-118">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="20d74-118">Resource name.</span></span>

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

### <span data-ttu-id="20d74-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20d74-119">-ResourceGroupName</span></span>
<span data-ttu-id="20d74-120">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="20d74-120">Resource group name.</span></span>

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

### <span data-ttu-id="20d74-121">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="20d74-121">-VirtualMachine</span></span>
<span data-ttu-id="20d74-122">Virutal machines.</span><span class="sxs-lookup"><span data-stu-id="20d74-122">Virutal Machines.</span></span>

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

### <span data-ttu-id="20d74-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="20d74-123">-Confirm</span></span>
<span data-ttu-id="20d74-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="20d74-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20d74-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20d74-125">-WhatIf</span></span>
<span data-ttu-id="20d74-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="20d74-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="20d74-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="20d74-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20d74-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20d74-128">CommonParameters</span></span>
<span data-ttu-id="20d74-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="20d74-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20d74-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20d74-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20d74-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="20d74-131">INPUTS</span></span>

### <span data-ttu-id="20d74-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="20d74-132">None</span></span>

## <span data-ttu-id="20d74-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="20d74-133">OUTPUTS</span></span>

### <span data-ttu-id="20d74-134">Microsoft. Azure. commands. Security. models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="20d74-134">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="20d74-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="20d74-135">NOTES</span></span>

## <span data-ttu-id="20d74-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="20d74-136">RELATED LINKS</span></span>
