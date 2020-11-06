---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Start-AzureRmJitNetworkAccessPolicy.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Start-AzureRmJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Start-AzureRmJitNetworkAccessPolicy.md
ms.openlocfilehash: 62dccdc3b55caa5d63036ed3298caa5a01514342
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501068"
---
# <span data-ttu-id="f4f74-101">Start-AzureRmJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f4f74-101">Start-AzureRmJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="f4f74-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f4f74-102">SYNOPSIS</span></span>
<span data-ttu-id="f4f74-103">Ideiglenes hálózati hozzáférési kérést hív meg.</span><span class="sxs-lookup"><span data-stu-id="f4f74-103">Invokes a temporary network access request.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4f74-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f4f74-104">SYNTAX</span></span>

### <span data-ttu-id="f4f74-105">ResourceGroupLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f4f74-105">ResourceGroupLevelResource (Default)</span></span>
```
Start-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4f74-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4f74-106">ResourceId</span></span>
```
Start-AzureRmJitNetworkAccessPolicy -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4f74-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="f4f74-107">InputObject</span></span>
```
Start-AzureRmJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicyInitiateInputObject>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4f74-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f4f74-108">DESCRIPTION</span></span>
<span data-ttu-id="f4f74-109">Ideiglenes hálózati hozzáférési kérést hív meg.</span><span class="sxs-lookup"><span data-stu-id="f4f74-109">Invokes a temporary network access request.</span></span>
<span data-ttu-id="f4f74-110">A kérés érvényesítése a beállított JIT-hálózat hozzáférési házirendjével történik, és ha a permittet, a felhasználó kérése szerint megnyílik egy hálózati kapcsolat.</span><span class="sxs-lookup"><span data-stu-id="f4f74-110">The request is validated against the configured JIT network access policy and if permittet, opens up a network connection according to the user's request.</span></span>
<span data-ttu-id="f4f74-111">A kérés a későbbi véleményezéshez loged válik, és a megadott időtartam túllépése után megszűnik.</span><span class="sxs-lookup"><span data-stu-id="f4f74-111">The request will be loged in the policy for later review and will be terminated when the specified duration will be exceeded.</span></span>

## <span data-ttu-id="f4f74-112">Példák</span><span class="sxs-lookup"><span data-stu-id="f4f74-112">EXAMPLES</span></span>

### <span data-ttu-id="f4f74-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f4f74-113">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -Kind "Basic" -VirtualMachine $vms

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.S
                    ecurity/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.
                    Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="f4f74-114">Megnyit egy hálózati kapcsolatot a megadott kapcsolatkérelem-adatforrásnak megfelelően.</span><span class="sxs-lookup"><span data-stu-id="f4f74-114">Opens up a network connection according to the specified connection request data.</span></span>

## <span data-ttu-id="f4f74-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f4f74-115">PARAMETERS</span></span>

### <span data-ttu-id="f4f74-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4f74-116">-DefaultProfile</span></span>
<span data-ttu-id="f4f74-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f4f74-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4f74-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4f74-118">-InputObject</span></span>
<span data-ttu-id="f4f74-119">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="f4f74-119">Input Object.</span></span>

```yaml
Type: PSSecurityJitNetworkAccessPolicyInitiateInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4f74-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="f4f74-120">-Location</span></span>
<span data-ttu-id="f4f74-121">Helyre.</span><span class="sxs-lookup"><span data-stu-id="f4f74-121">Location.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4f74-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f4f74-122">-Name</span></span>
<span data-ttu-id="f4f74-123">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="f4f74-123">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4f74-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4f74-124">-ResourceGroupName</span></span>
<span data-ttu-id="f4f74-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="f4f74-125">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4f74-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4f74-126">-ResourceId</span></span>
<span data-ttu-id="f4f74-127">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="f4f74-127">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4f74-128">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f4f74-128">-VirtualMachine</span></span>
<span data-ttu-id="f4f74-129">Automatikus kiépítési.</span><span class="sxs-lookup"><span data-stu-id="f4f74-129">Automatic Provisioning.</span></span>

```yaml
Type: PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4f74-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f4f74-130">-Confirm</span></span>
<span data-ttu-id="f4f74-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f4f74-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4f74-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4f74-132">-WhatIf</span></span>
<span data-ttu-id="f4f74-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f4f74-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4f74-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f4f74-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4f74-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4f74-135">CommonParameters</span></span>
<span data-ttu-id="f4f74-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f4f74-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4f74-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4f74-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4f74-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4f74-138">INPUTS</span></span>

### <span data-ttu-id="f4f74-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f4f74-139">System.String</span></span>
<span data-ttu-id="f4f74-140">Microsoft. Azure. commands. Security. models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine []</span><span class="sxs-lookup"><span data-stu-id="f4f74-140">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]</span></span>

## <span data-ttu-id="f4f74-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4f74-141">OUTPUTS</span></span>

### <span data-ttu-id="f4f74-142">Microsoft. Azure. commands. Security. models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f4f74-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="f4f74-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f4f74-143">NOTES</span></span>

## <span data-ttu-id="f4f74-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4f74-144">RELATED LINKS</span></span>
