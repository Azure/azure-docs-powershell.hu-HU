---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
ms.openlocfilehash: d0ed76dfc656e52ec7f83344346957334627e086
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344802"
---
# <span data-ttu-id="2e5d3-101">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="2e5d3-101">Remove-AzPublicIpPrefix</span></span>

## <span data-ttu-id="2e5d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e5d3-102">SYNOPSIS</span></span>
<span data-ttu-id="2e5d3-103">Nyilvános IP-előtag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="2e5d3-103">Removes a public IP prefix</span></span>

## <span data-ttu-id="2e5d3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2e5d3-104">SYNTAX</span></span>

### <span data-ttu-id="2e5d3-105">RemoveByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2e5d3-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e5d3-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e5d3-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzPublicIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e5d3-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e5d3-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzPublicIpPrefix -InputObject <PSPublicIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e5d3-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2e5d3-108">DESCRIPTION</span></span>
<span data-ttu-id="2e5d3-109">A **Remove-AzPublicIpPrefix** parancsmag eltávolítja az Azure nyilvános IP-előtagját, ha nem rendeltek hozzá nyilvános IP-címeket.</span><span class="sxs-lookup"><span data-stu-id="2e5d3-109">The **Remove-AzPublicIpPrefix** cmdlet removes an Azure public IP prefix as long as there are no public IP addresses allocated from it.</span></span>

## <span data-ttu-id="2e5d3-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2e5d3-110">EXAMPLES</span></span>

### <span data-ttu-id="2e5d3-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="2e5d3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="2e5d3-112">Eltávolítja a Name $prefixName nyilvános IP-előtagot az erőforráscsoportból $rgName</span><span class="sxs-lookup"><span data-stu-id="2e5d3-112">Removes the public IP prefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="2e5d3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e5d3-113">PARAMETERS</span></span>

### <span data-ttu-id="2e5d3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2e5d3-114">-AsJob</span></span>
<span data-ttu-id="2e5d3-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="2e5d3-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2e5d3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e5d3-116">-DefaultProfile</span></span>
<span data-ttu-id="2e5d3-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2e5d3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e5d3-118">-Force</span><span class="sxs-lookup"><span data-stu-id="2e5d3-118">-Force</span></span>
<span data-ttu-id="2e5d3-119">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2e5d3-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2e5d3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e5d3-120">-InputObject</span></span>
<span data-ttu-id="2e5d3-121">PublicIpPrefix objektum</span><span class="sxs-lookup"><span data-stu-id="2e5d3-121">A PublicIpPrefix object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e5d3-122">-Name</span><span class="sxs-lookup"><span data-stu-id="2e5d3-122">-Name</span></span>
<span data-ttu-id="2e5d3-123">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="2e5d3-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e5d3-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e5d3-124">-PassThru</span></span>
<span data-ttu-id="2e5d3-125">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="2e5d3-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2e5d3-126">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="2e5d3-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2e5d3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e5d3-127">-ResourceGroupName</span></span>
<span data-ttu-id="2e5d3-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2e5d3-128">The resource group name.</span></span>

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

### <span data-ttu-id="2e5d3-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e5d3-129">-ResourceId</span></span>
<span data-ttu-id="2e5d3-130">Az eltávolítható erőforrás erőforrásazonosítója</span><span class="sxs-lookup"><span data-stu-id="2e5d3-130">The resourceId for the resource to remove</span></span>

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

### <span data-ttu-id="2e5d3-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e5d3-131">-Confirm</span></span>
<span data-ttu-id="2e5d3-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2e5d3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e5d3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e5d3-133">-WhatIf</span></span>
<span data-ttu-id="2e5d3-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2e5d3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e5d3-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2e5d3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e5d3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e5d3-136">CommonParameters</span></span>
<span data-ttu-id="2e5d3-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e5d3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e5d3-138">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e5d3-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e5d3-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2e5d3-139">INPUTS</span></span>

### <span data-ttu-id="2e5d3-140">System.String</span><span class="sxs-lookup"><span data-stu-id="2e5d3-140">System.String</span></span>

### <span data-ttu-id="2e5d3-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="2e5d3-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="2e5d3-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e5d3-142">OUTPUTS</span></span>

### <span data-ttu-id="2e5d3-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2e5d3-143">System.Boolean</span></span>

## <span data-ttu-id="2e5d3-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2e5d3-144">NOTES</span></span>

## <span data-ttu-id="2e5d3-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e5d3-145">RELATED LINKS</span></span>

[<span data-ttu-id="2e5d3-146">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="2e5d3-146">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="2e5d3-147">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="2e5d3-147">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="2e5d3-148">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="2e5d3-148">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
