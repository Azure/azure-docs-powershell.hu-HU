---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
ms.openlocfilehash: 95da37a36c8a97bf507ec8d191728b34a88a25a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006149"
---
# <span data-ttu-id="09d29-101">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="09d29-101">Remove-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="09d29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09d29-102">SYNOPSIS</span></span>
<span data-ttu-id="09d29-103">Szolgáltatásvégpont-házirend eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="09d29-103">Removes a service endpoint policy.</span></span>

## <span data-ttu-id="09d29-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="09d29-104">SYNTAX</span></span>

### <span data-ttu-id="09d29-105">RemoveByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="09d29-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09d29-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="09d29-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09d29-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="09d29-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject <PSServiceEndpointPolicy> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09d29-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="09d29-108">DESCRIPTION</span></span>
<span data-ttu-id="09d29-109">A **Remove-AzServiceEndpointPolicy** parancsmag eltávolít egy szolgáltatásvégpont-házirendet.</span><span class="sxs-lookup"><span data-stu-id="09d29-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="09d29-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="09d29-110">EXAMPLES</span></span>

### <span data-ttu-id="09d29-111">1. példa: Szolgáltatásvégpont-házirend eltávolítása név használatával</span><span class="sxs-lookup"><span data-stu-id="09d29-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicy -Name "Policy1" -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="09d29-112">Ez a parancs eltávolítja a "resourcegroup1" nevű erőforráscsoporthoz tartozó szolgáltatásvégpont-házirendet a Házirend1 névvel.</span><span class="sxs-lookup"><span data-stu-id="09d29-112">This command removes a service endpoint policy with name Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

### <span data-ttu-id="09d29-113">2. példa: Szolgáltatásvégpont-házirend eltávolítása bemeneti objektum használatával</span><span class="sxs-lookup"><span data-stu-id="09d29-113">Example 2: Remove a service endpoint policy using input object</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject $Policy1 -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="09d29-114">Ez a parancs eltávolítja az "erőforráscsoport1" nevű erőforráscsoporthoz tartozó szolgáltatásvégpont-házirendobjektum-házirend1-et.</span><span class="sxs-lookup"><span data-stu-id="09d29-114">This command removes a service endpoint policy object Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

## <span data-ttu-id="09d29-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09d29-115">PARAMETERS</span></span>

### <span data-ttu-id="09d29-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09d29-116">-DefaultProfile</span></span>
<span data-ttu-id="09d29-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="09d29-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09d29-118">-Force</span><span class="sxs-lookup"><span data-stu-id="09d29-118">-Force</span></span>
<span data-ttu-id="09d29-119">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="09d29-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="09d29-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09d29-120">-InputObject</span></span>
<span data-ttu-id="09d29-121">A szolgáltatás végponti házirendobjektuma.</span><span class="sxs-lookup"><span data-stu-id="09d29-121">The service endpoint policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09d29-122">-Name</span><span class="sxs-lookup"><span data-stu-id="09d29-122">-Name</span></span>
<span data-ttu-id="09d29-123">A szolgáltatás végponti házirendjának neve</span><span class="sxs-lookup"><span data-stu-id="09d29-123">The name of the service endpoint policy</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09d29-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="09d29-124">-PassThru</span></span>
<span data-ttu-id="09d29-125">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="09d29-125">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="09d29-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09d29-126">-ResourceGroupName</span></span>
<span data-ttu-id="09d29-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="09d29-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09d29-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09d29-128">-ResourceId</span></span>
<span data-ttu-id="09d29-129">A szolgáltatásvégpont-házirend azonosítója.</span><span class="sxs-lookup"><span data-stu-id="09d29-129">The ID of service endpoint policy.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09d29-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="09d29-130">-Confirm</span></span>
<span data-ttu-id="09d29-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="09d29-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09d29-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09d29-132">-WhatIf</span></span>
<span data-ttu-id="09d29-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="09d29-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09d29-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="09d29-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09d29-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09d29-135">CommonParameters</span></span>
<span data-ttu-id="09d29-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09d29-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09d29-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09d29-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09d29-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="09d29-138">INPUTS</span></span>

### <span data-ttu-id="09d29-139">System.String</span><span class="sxs-lookup"><span data-stu-id="09d29-139">System.String</span></span>

### <span data-ttu-id="09d29-140">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="09d29-140">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="09d29-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="09d29-141">OUTPUTS</span></span>

### <span data-ttu-id="09d29-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="09d29-142">System.Boolean</span></span>

## <span data-ttu-id="09d29-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="09d29-143">NOTES</span></span>

## <span data-ttu-id="09d29-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="09d29-144">RELATED LINKS</span></span>

[<span data-ttu-id="09d29-145">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="09d29-145">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="09d29-146">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="09d29-146">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="09d29-147">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="09d29-147">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
