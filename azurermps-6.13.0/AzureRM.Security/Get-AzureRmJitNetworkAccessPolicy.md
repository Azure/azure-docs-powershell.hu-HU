---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmJitNetworkAccessPolicy.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmJitNetworkAccessPolicy.md
ms.openlocfilehash: bd366b636a29a08bea9124b3c3f4b9b423dc4deb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492744"
---
# <span data-ttu-id="5a566-101">Get-AzureRmJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5a566-101">Get-AzureRmJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="5a566-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5a566-102">SYNOPSIS</span></span>
<span data-ttu-id="5a566-103">A JIT hálózati hozzáférési házirendek beolvasása</span><span class="sxs-lookup"><span data-stu-id="5a566-103">Gets the JIT network access policies</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a566-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5a566-104">SYNTAX</span></span>

### <span data-ttu-id="5a566-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5a566-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmJitNetworkAccessPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a566-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="5a566-106">ResourceGroupScope</span></span>
```
Get-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5a566-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="5a566-107">ResourceGroupLevelResource</span></span>
```
Get-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a566-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a566-108">ResourceId</span></span>
```
Get-AzureRmJitNetworkAccessPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5a566-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="5a566-109">DESCRIPTION</span></span>
<span data-ttu-id="5a566-110">Éppen időben (JIT) a hálózat-hozzáférési házirendek lehetővé teszik a szabályok definiálását, amely lehetővé teszi, hogy az egyszerű felhasználók ideiglenes hálózati kapcsolatot hozzanak létre egy VM-kapcsolattal.</span><span class="sxs-lookup"><span data-stu-id="5a566-110">Just In Time (JIT) network access policies let you define a policy the will allow simple users to create a temporary network connection to a VM.</span></span>
<span data-ttu-id="5a566-111">A házirend azt határozza meg, hogy a portok, a protokollok és a forrás IP-címei hogyan igényelhetnek kapcsolatot a VM-vel és a maximális időtartammal, mielőtt a kapcsolat automatikusan bezárul.</span><span class="sxs-lookup"><span data-stu-id="5a566-111">The policy defines what ports, protocol and source IP addresses can request a connection to a VM and the max duration before the connection will be closed automatically.</span></span>
<span data-ttu-id="5a566-112">A házirendben megtekintheti az ezzel a házirenddel létrehozott kapcsolatkérelem-kérést is.</span><span class="sxs-lookup"><span data-stu-id="5a566-112">In the policy you can also see the connection request that were made with this policy.</span></span> 

## <span data-ttu-id="5a566-113">Példák</span><span class="sxs-lookup"><span data-stu-id="5a566-113">EXAMPLES</span></span>

### <span data-ttu-id="5a566-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5a566-114">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmJitNetworkAccessPolicy
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

<span data-ttu-id="5a566-115">Az összes JIT-hálózat hozzáférési rendőrének beszerzése előfizetéshez</span><span class="sxs-lookup"><span data-stu-id="5a566-115">Get all the JIT network access polices on a subscription</span></span>

### <span data-ttu-id="5a566-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="5a566-116">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1"
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

<span data-ttu-id="5a566-117">Az összes JIT-hálózati hozzáférési rendőr beszerzése a "myService1" erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="5a566-117">Get all the JIT network access polices on the "myService1" resource group</span></span>

### <span data-ttu-id="5a566-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="5a566-118">Example 3</span></span>
```powershell
PS C:\> Get-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="5a566-119">Meghatározott JIT-hálózati hozzáférési házirend beolvasása</span><span class="sxs-lookup"><span data-stu-id="5a566-119">Gets a specific JIT network access policy</span></span>

## <span data-ttu-id="5a566-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5a566-120">PARAMETERS</span></span>

### <span data-ttu-id="5a566-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a566-121">-DefaultProfile</span></span>
<span data-ttu-id="5a566-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5a566-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a566-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="5a566-123">-Location</span></span>
<span data-ttu-id="5a566-124">Helyre.</span><span class="sxs-lookup"><span data-stu-id="5a566-124">Location.</span></span>

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

### <span data-ttu-id="5a566-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5a566-125">-Name</span></span>
<span data-ttu-id="5a566-126">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="5a566-126">Resource name.</span></span>

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

### <span data-ttu-id="5a566-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a566-127">-ResourceGroupName</span></span>
<span data-ttu-id="5a566-128">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="5a566-128">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a566-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a566-129">-ResourceId</span></span>
<span data-ttu-id="5a566-130">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="5a566-130">Resource ID.</span></span>

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

### <span data-ttu-id="5a566-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a566-131">CommonParameters</span></span>
<span data-ttu-id="5a566-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5a566-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a566-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a566-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a566-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a566-134">INPUTS</span></span>

### <span data-ttu-id="5a566-135">System. String</span><span class="sxs-lookup"><span data-stu-id="5a566-135">System.String</span></span>

## <span data-ttu-id="5a566-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a566-136">OUTPUTS</span></span>

### <span data-ttu-id="5a566-137">Microsoft. Azure. commands. Security. models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5a566-137">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="5a566-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5a566-138">NOTES</span></span>

## <span data-ttu-id="5a566-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5a566-139">RELATED LINKS</span></span>
