---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
ms.openlocfilehash: e7025a48fd1d83a0018ac18de01673b0deeed742
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670277"
---
# <span data-ttu-id="971c2-101">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="971c2-101">New-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="971c2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="971c2-102">SYNOPSIS</span></span>
<span data-ttu-id="971c2-103">Létrehoz egy szolgáltatási végpont-házirendet.</span><span class="sxs-lookup"><span data-stu-id="971c2-103">Creates a service endpoint policy.</span></span>

## <span data-ttu-id="971c2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="971c2-104">SYNTAX</span></span>

```
New-AzServiceEndpointPolicy -Name <String>
 [-ServiceEndpointPolicyDefinition <PSServiceEndpointPolicyDefinition[]>] -ResourceGroupName <String>
 -Location <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="971c2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="971c2-105">DESCRIPTION</span></span>
<span data-ttu-id="971c2-106">A **New-AzServiceEndpointPolicy** parancsmag létrehoz egy szolgáltatási végpont-házirendet.</span><span class="sxs-lookup"><span data-stu-id="971c2-106">The **New-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="971c2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="971c2-107">EXAMPLES</span></span>

### <span data-ttu-id="971c2-108">Példa 1: szolgáltatás végpont-házirendjének létrehozása</span><span class="sxs-lookup"><span data-stu-id="971c2-108">Example 1: Creates a service endpoint policy</span></span>
```
$serviceEndpointPolicy = New-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicyDefinition $serviceEndpointDefinition -Location "location";
```

<span data-ttu-id="971c2-109">Ez a parancs létrehoz egy Házirend1 nevű szolgáltatási végpont-házirendet az objektum által definiált definíciókkal $serviceEndpointDefinition és a $serviceEndpointPolicy változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="971c2-109">This command creates a service endpoint policy named Policy1 with definitions defined by the object $serviceEndpointDefinition and stores it in the $serviceEndpointPolicy variable.</span></span>

## <span data-ttu-id="971c2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="971c2-110">PARAMETERS</span></span>

### <span data-ttu-id="971c2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="971c2-111">-DefaultProfile</span></span>
<span data-ttu-id="971c2-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="971c2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="971c2-113">-Force</span><span class="sxs-lookup"><span data-stu-id="971c2-113">-Force</span></span>
<span data-ttu-id="971c2-114">Ne kérjen megerősítést, ha egy erőforrást szeretne átgondolni?</span><span class="sxs-lookup"><span data-stu-id="971c2-114">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="971c2-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="971c2-115">-Location</span></span>
<span data-ttu-id="971c2-116">helyre.</span><span class="sxs-lookup"><span data-stu-id="971c2-116">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="971c2-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="971c2-117">-Name</span></span>
<span data-ttu-id="971c2-118">Az alhálózat neve</span><span class="sxs-lookup"><span data-stu-id="971c2-118">The name of the subnet</span></span>

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

### <span data-ttu-id="971c2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="971c2-119">-ResourceGroupName</span></span>
<span data-ttu-id="971c2-120">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="971c2-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="971c2-121">-ServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="971c2-121">-ServiceEndpointPolicyDefinition</span></span>
<span data-ttu-id="971c2-122">A szolgáltatás végpont-definícióinak listája</span><span class="sxs-lookup"><span data-stu-id="971c2-122">List of service endpoint definitions</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="971c2-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="971c2-123">-Confirm</span></span>
<span data-ttu-id="971c2-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="971c2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="971c2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="971c2-125">-WhatIf</span></span>
<span data-ttu-id="971c2-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="971c2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="971c2-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="971c2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="971c2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="971c2-128">CommonParameters</span></span>
<span data-ttu-id="971c2-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="971c2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="971c2-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="971c2-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="971c2-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="971c2-131">INPUTS</span></span>

### <span data-ttu-id="971c2-132">System. String</span><span class="sxs-lookup"><span data-stu-id="971c2-132">System.String</span></span>

## <span data-ttu-id="971c2-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="971c2-133">OUTPUTS</span></span>

### <span data-ttu-id="971c2-134">Microsoft. Azure. commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="971c2-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="971c2-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="971c2-135">NOTES</span></span>

## <span data-ttu-id="971c2-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="971c2-136">RELATED LINKS</span></span>

[<span data-ttu-id="971c2-137">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="971c2-137">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="971c2-138">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="971c2-138">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="971c2-139">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="971c2-139">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
