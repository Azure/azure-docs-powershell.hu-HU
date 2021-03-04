---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
ms.openlocfilehash: 3e1caeb5dec11188cf824bdcddf2b0de78f707c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941537"
---
# <span data-ttu-id="03202-101">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="03202-101">Remove-AzPrivateEndpoint</span></span>

## <span data-ttu-id="03202-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03202-102">SYNOPSIS</span></span>
<span data-ttu-id="03202-103">Eltávolít egy privát végpontot.</span><span class="sxs-lookup"><span data-stu-id="03202-103">Removes a private endpoint.</span></span>

## <span data-ttu-id="03202-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="03202-104">SYNTAX</span></span>

```
Remove-AzPrivateEndpoint -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03202-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="03202-105">DESCRIPTION</span></span>
<span data-ttu-id="03202-106">A **Remove-AzPrivateEndpoint** parancsmag eltávolít egy privát végpontot.</span><span class="sxs-lookup"><span data-stu-id="03202-106">The **Remove-AzPrivateEndpoint** cmdlet removes a private endpoint.</span></span> 

## <span data-ttu-id="03202-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="03202-107">EXAMPLES</span></span>

### <span data-ttu-id="03202-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="03202-108">Example 1</span></span>
```
Remove-AzPrivateEndpoint -Name MyPrivateEndpoint1 -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="03202-109">Ebben a példában eltávolítunk egy MyPrivateEndpoint1 nevű privát végpontot.</span><span class="sxs-lookup"><span data-stu-id="03202-109">This example remove a private endpoint named MyPrivateEndpoint1.</span></span>

## <span data-ttu-id="03202-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03202-110">PARAMETERS</span></span>

### <span data-ttu-id="03202-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03202-111">-AsJob</span></span>
<span data-ttu-id="03202-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="03202-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="03202-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03202-113">-DefaultProfile</span></span>
<span data-ttu-id="03202-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="03202-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03202-115">-Force</span><span class="sxs-lookup"><span data-stu-id="03202-115">-Force</span></span>
<span data-ttu-id="03202-116">Ne kérjen megerősítést, ha erőforrást szeretne törölni</span><span class="sxs-lookup"><span data-stu-id="03202-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="03202-117">-Name</span><span class="sxs-lookup"><span data-stu-id="03202-117">-Name</span></span>
<span data-ttu-id="03202-118">A magánjellegű végpont neve.</span><span class="sxs-lookup"><span data-stu-id="03202-118">The name of the private endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03202-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03202-119">-PassThru</span></span>
<span data-ttu-id="03202-120">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="03202-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="03202-121">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="03202-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="03202-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03202-122">-ResourceGroupName</span></span>
<span data-ttu-id="03202-123">A magánjellegű végpont erőforráscsoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="03202-123">The resource group name of the private endpoint.</span></span>

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

### <span data-ttu-id="03202-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03202-124">-Confirm</span></span>
<span data-ttu-id="03202-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="03202-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03202-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03202-126">-WhatIf</span></span>
<span data-ttu-id="03202-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="03202-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03202-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="03202-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03202-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03202-129">CommonParameters</span></span>
<span data-ttu-id="03202-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03202-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03202-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="03202-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03202-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="03202-132">INPUTS</span></span>

### <span data-ttu-id="03202-133">System.String</span><span class="sxs-lookup"><span data-stu-id="03202-133">System.String</span></span>

## <span data-ttu-id="03202-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="03202-134">OUTPUTS</span></span>

### <span data-ttu-id="03202-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="03202-135">System.Boolean</span></span>

## <span data-ttu-id="03202-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="03202-136">NOTES</span></span>

## <span data-ttu-id="03202-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="03202-137">RELATED LINKS</span></span>

[<span data-ttu-id="03202-138">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="03202-138">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="03202-139">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="03202-139">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)