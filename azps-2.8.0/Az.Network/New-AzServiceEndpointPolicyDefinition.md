---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 634beeaf33515ac5e89011ab47eaea34eccaa581
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837913"
---
# <span data-ttu-id="64717-101">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="64717-101">New-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="64717-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="64717-102">SYNOPSIS</span></span>
<span data-ttu-id="64717-103">Szolgáltatási végpont házirend-definícióját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="64717-103">Creates a service endpoint policy definition.</span></span>

## <span data-ttu-id="64717-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="64717-104">SYNTAX</span></span>

```
New-AzServiceEndpointPolicyDefinition -Name <String> [-Description <String>] [-ServiceResource <String[]>]
 [-Service <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64717-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="64717-105">DESCRIPTION</span></span>
<span data-ttu-id="64717-106">A **New-AzServiceEndpointPolicyDefinition** parancsmag a szolgáltatás végpont-házirendjének definícióját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="64717-106">The **New-AzServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="64717-107">Példák</span><span class="sxs-lookup"><span data-stu-id="64717-107">EXAMPLES</span></span>

### <span data-ttu-id="64717-108">Példa 1: szolgáltatás végpont-házirendjének létrehozása</span><span class="sxs-lookup"><span data-stu-id="64717-108">Example 1: Creates a service endpoint policy</span></span>
```
$policydef= New-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="64717-109">Ez a parancs létrehozza a szolgáltatás végpontjának házirend-definícióját a name ServiceEndpointPolicyDefinition1, a Service Microsoft. Storage, a Service Resources-előfizetés/sub1 és a Description (új definíció) című témakörben, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $policydef változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="64717-109">This command creates the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="64717-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="64717-110">PARAMETERS</span></span>

### <span data-ttu-id="64717-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64717-111">-DefaultProfile</span></span>
<span data-ttu-id="64717-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="64717-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64717-113">-Leírás</span><span class="sxs-lookup"><span data-stu-id="64717-113">-Description</span></span>
<span data-ttu-id="64717-114">A definíció leírása</span><span class="sxs-lookup"><span data-stu-id="64717-114">The description of the definition</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64717-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="64717-115">-Name</span></span>
<span data-ttu-id="64717-116">A szolgáltatás végpont-házirendjének neve</span><span class="sxs-lookup"><span data-stu-id="64717-116">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="64717-117">-Szolgáltatás</span><span class="sxs-lookup"><span data-stu-id="64717-117">-Service</span></span>
<span data-ttu-id="64717-118">A szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="64717-118">Name of the service</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64717-119">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="64717-119">-ServiceResource</span></span>
<span data-ttu-id="64717-120">A szolgáltatási erőforrások listája</span><span class="sxs-lookup"><span data-stu-id="64717-120">List of service resources</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64717-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="64717-121">-Confirm</span></span>
<span data-ttu-id="64717-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="64717-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64717-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64717-123">-WhatIf</span></span>
<span data-ttu-id="64717-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="64717-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="64717-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="64717-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64717-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64717-126">CommonParameters</span></span>
<span data-ttu-id="64717-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="64717-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64717-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64717-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64717-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="64717-129">INPUTS</span></span>

### <span data-ttu-id="64717-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="64717-130">None</span></span>

## <span data-ttu-id="64717-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64717-131">OUTPUTS</span></span>

### <span data-ttu-id="64717-132">Microsoft. Azure. commands. Network. models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="64717-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="64717-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="64717-133">NOTES</span></span>

## <span data-ttu-id="64717-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64717-134">RELATED LINKS</span></span>

[<span data-ttu-id="64717-135">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="64717-135">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="64717-136">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="64717-136">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="64717-137">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="64717-137">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="64717-138">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="64717-138">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
