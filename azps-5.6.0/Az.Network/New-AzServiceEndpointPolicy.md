---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
ms.openlocfilehash: b5f555a0df848c86dbbc0a04297d45b4132e6972
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919513"
---
# <span data-ttu-id="e1e17-101">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e1e17-101">New-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="e1e17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1e17-102">SYNOPSIS</span></span>
<span data-ttu-id="e1e17-103">Szolgáltatási végpont házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e1e17-103">Creates a service endpoint policy.</span></span>

## <span data-ttu-id="e1e17-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e1e17-104">SYNTAX</span></span>

```
New-AzServiceEndpointPolicy -Name <String>
 [-ServiceEndpointPolicyDefinition <PSServiceEndpointPolicyDefinition[]>] -ResourceGroupName <String>
 -Location <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e1e17-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e1e17-105">DESCRIPTION</span></span>
<span data-ttu-id="e1e17-106">A **New-AzServiceEndpointPolicy** parancsmag szolgáltatási végponti házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e1e17-106">The **New-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="e1e17-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e1e17-107">EXAMPLES</span></span>

### <span data-ttu-id="e1e17-108">1. példa: Szolgáltatásvégpont-házirendet hoz létre</span><span class="sxs-lookup"><span data-stu-id="e1e17-108">Example 1: Creates a service endpoint policy</span></span>
```
$serviceEndpointPolicy = New-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicyDefinition $serviceEndpointDefinition -Location "location";
```

<span data-ttu-id="e1e17-109">Ez a parancs létrehoz egy Házirend1 nevű szolgáltatásvégpont-házirendet, amely az objektum által definiált definíciókat $serviceEndpointDefinition és tárolja azt a $serviceEndpointPolicy változóban.</span><span class="sxs-lookup"><span data-stu-id="e1e17-109">This command creates a service endpoint policy named Policy1 with definitions defined by the object $serviceEndpointDefinition and stores it in the $serviceEndpointPolicy variable.</span></span>

## <span data-ttu-id="e1e17-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1e17-110">PARAMETERS</span></span>

### <span data-ttu-id="e1e17-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1e17-111">-DefaultProfile</span></span>
<span data-ttu-id="e1e17-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e1e17-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1e17-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e1e17-113">-Force</span></span>
<span data-ttu-id="e1e17-114">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="e1e17-114">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="e1e17-115">-Location</span><span class="sxs-lookup"><span data-stu-id="e1e17-115">-Location</span></span>
<span data-ttu-id="e1e17-116">helyére.</span><span class="sxs-lookup"><span data-stu-id="e1e17-116">location.</span></span>

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

### <span data-ttu-id="e1e17-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e1e17-117">-Name</span></span>
<span data-ttu-id="e1e17-118">Az alhálózat neve</span><span class="sxs-lookup"><span data-stu-id="e1e17-118">The name of the subnet</span></span>

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

### <span data-ttu-id="e1e17-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1e17-119">-ResourceGroupName</span></span>
<span data-ttu-id="e1e17-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e1e17-120">The resource group name.</span></span>

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

### <span data-ttu-id="e1e17-121">-ServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e1e17-121">-ServiceEndpointPolicyDefinition</span></span>
<span data-ttu-id="e1e17-122">Szolgáltatásvégpont-definíciók listája</span><span class="sxs-lookup"><span data-stu-id="e1e17-122">List of service endpoint definitions</span></span>

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

### <span data-ttu-id="e1e17-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1e17-123">-Confirm</span></span>
<span data-ttu-id="e1e17-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e1e17-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1e17-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1e17-125">-WhatIf</span></span>
<span data-ttu-id="e1e17-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e1e17-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1e17-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e1e17-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1e17-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1e17-128">CommonParameters</span></span>
<span data-ttu-id="e1e17-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1e17-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1e17-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1e17-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1e17-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e1e17-131">INPUTS</span></span>

### <span data-ttu-id="e1e17-132">System.String</span><span class="sxs-lookup"><span data-stu-id="e1e17-132">System.String</span></span>

## <span data-ttu-id="e1e17-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1e17-133">OUTPUTS</span></span>

### <span data-ttu-id="e1e17-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e1e17-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="e1e17-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e1e17-135">NOTES</span></span>

## <span data-ttu-id="e1e17-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e1e17-136">RELATED LINKS</span></span>

[<span data-ttu-id="e1e17-137">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e1e17-137">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="e1e17-138">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e1e17-138">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="e1e17-139">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e1e17-139">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
