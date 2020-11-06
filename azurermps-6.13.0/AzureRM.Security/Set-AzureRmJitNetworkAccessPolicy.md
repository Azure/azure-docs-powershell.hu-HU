---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmJitNetworkAccessPolicy.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmJitNetworkAccessPolicy.md
ms.openlocfilehash: 72e3cf48f112c5e9bb07a8f7eb57dfe3d4c9ee07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494917"
---
# <span data-ttu-id="3b3fe-101">Set-AzureRmJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3b3fe-101">Set-AzureRmJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="3b3fe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3b3fe-102">SYNOPSIS</span></span>
<span data-ttu-id="3b3fe-103">A JIT-hálózat elérési házirendjének frissítése</span><span class="sxs-lookup"><span data-stu-id="3b3fe-103">Updates JIT network access policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b3fe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3b3fe-104">SYNTAX</span></span>

```
Set-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyVirtualMachine[]> -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b3fe-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3b3fe-105">DESCRIPTION</span></span>
<span data-ttu-id="3b3fe-106">A JIT-hálózat elérési házirendjének frissítése</span><span class="sxs-lookup"><span data-stu-id="3b3fe-106">Updates JIT network access policy.</span></span>

## <span data-ttu-id="3b3fe-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3b3fe-107">EXAMPLES</span></span>

### <span data-ttu-id="3b3fe-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3b3fe-108">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -VirtualMachine $vmRules -Kind "Basic"

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="3b3fe-109">A JIT-hálózat hozzáférési házirendjének frissítése új VM-szabályokkal.</span><span class="sxs-lookup"><span data-stu-id="3b3fe-109">Updates a JIT network access policy with new VM rules.</span></span>

## <span data-ttu-id="3b3fe-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3b3fe-110">PARAMETERS</span></span>

### <span data-ttu-id="3b3fe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b3fe-111">-DefaultProfile</span></span>
<span data-ttu-id="3b3fe-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3b3fe-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3fe-113">-Kind</span><span class="sxs-lookup"><span data-stu-id="3b3fe-113">-Kind</span></span>
<span data-ttu-id="3b3fe-114">Típusú.</span><span class="sxs-lookup"><span data-stu-id="3b3fe-114">Kind.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3fe-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="3b3fe-115">-Location</span></span>
<span data-ttu-id="3b3fe-116">Helyre.</span><span class="sxs-lookup"><span data-stu-id="3b3fe-116">Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3fe-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3b3fe-117">-Name</span></span>
<span data-ttu-id="3b3fe-118">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="3b3fe-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3fe-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b3fe-119">-ResourceGroupName</span></span>
<span data-ttu-id="3b3fe-120">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="3b3fe-120">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3fe-121">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="3b3fe-121">-VirtualMachine</span></span>
<span data-ttu-id="3b3fe-122">Virutal machines.</span><span class="sxs-lookup"><span data-stu-id="3b3fe-122">Virutal Machines.</span></span>

```yaml
Type: PSSecurityJitNetworkAccessPolicyVirtualMachine[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3fe-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3b3fe-123">-Confirm</span></span>
<span data-ttu-id="3b3fe-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3b3fe-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3fe-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b3fe-125">-WhatIf</span></span>
<span data-ttu-id="3b3fe-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3b3fe-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3b3fe-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3b3fe-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3fe-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b3fe-128">CommonParameters</span></span>
<span data-ttu-id="3b3fe-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3b3fe-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b3fe-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b3fe-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b3fe-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b3fe-131">INPUTS</span></span>

### <span data-ttu-id="3b3fe-132">System. String</span><span class="sxs-lookup"><span data-stu-id="3b3fe-132">System.String</span></span>
<span data-ttu-id="3b3fe-133">Microsoft. Azure. commands. Security. models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicyVirtualMachine []</span><span class="sxs-lookup"><span data-stu-id="3b3fe-133">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyVirtualMachine[]</span></span>

## <span data-ttu-id="3b3fe-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b3fe-134">OUTPUTS</span></span>

### <span data-ttu-id="3b3fe-135">Microsoft. Azure. commands. Security. models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3b3fe-135">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="3b3fe-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3b3fe-136">NOTES</span></span>

## <span data-ttu-id="3b3fe-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3b3fe-137">RELATED LINKS</span></span>
