---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
ms.openlocfilehash: 9d0bca8be88c0448916df27544ce35bf7a6ddee1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918466"
---
# <span data-ttu-id="eac5c-101">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="eac5c-101">Update-AzCustomIpPrefix</span></span>

## <span data-ttu-id="eac5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eac5c-102">SYNOPSIS</span></span>
<span data-ttu-id="eac5c-103">CustomIpPrefix frissítése</span><span class="sxs-lookup"><span data-stu-id="eac5c-103">Updates a CustomIpPrefix</span></span>

## <span data-ttu-id="eac5c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="eac5c-104">SYNTAX</span></span>

### <span data-ttu-id="eac5c-105">UpdateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="eac5c-105">UpdateByNameParameterSet</span></span>
```
Update-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Commission] [-Decomission]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eac5c-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eac5c-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Commission] [-Decomission] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eac5c-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eac5c-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzCustomIpPrefix -ResourceId <String> [-Commission] [-Decomission] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eac5c-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="eac5c-108">DESCRIPTION</span></span>
<span data-ttu-id="eac5c-109">Az **Update-AzCustomIpPrefix** parancsmaggal a felhasználó jutalékot vagy leszerelheti CustomIpPrefix eszközét, vagy szerkesztheti az erőforrás címkéit.</span><span class="sxs-lookup"><span data-stu-id="eac5c-109">The **Update-AzCustomIpPrefix** cmdlet allows the user to either commission or decommission their CustomIpPrefix, or edit the tags of the resource.</span></span>

## <span data-ttu-id="eac5c-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="eac5c-110">EXAMPLES</span></span>

### <span data-ttu-id="eac5c-111">1. példa: A CustomIpPrefix jutaléka</span><span class="sxs-lookup"><span data-stu-id="eac5c-111">Example 1 : Commission the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Commission
```

<span data-ttu-id="eac5c-112">A fenti parancs elindítja a CustomIpPrefix rendelési folyamatát.</span><span class="sxs-lookup"><span data-stu-id="eac5c-112">The above command will start the commissioning process of the CustomIpPrefix.</span></span>

### <span data-ttu-id="eac5c-113">2. példa: A CustomIpPrefix leszerelése</span><span class="sxs-lookup"><span data-stu-id="eac5c-113">Example 2 : Decommission the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Decommission
```

<span data-ttu-id="eac5c-114">A fenti parancs elindítja a CustomIpPrefix de-commissioning folyamatát.</span><span class="sxs-lookup"><span data-stu-id="eac5c-114">The above command will start the de-commissioning process of the CustomIpPrefix.</span></span>

### <span data-ttu-id="eac5c-115">3. példa: A CustomIpPrefix címkéinek frissítése</span><span class="sxs-lookup"><span data-stu-id="eac5c-115">Example 3 : Update tags for the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Tag $tags
```

<span data-ttu-id="eac5c-116">A fenti parancs frissíti a CustomIpPrefix címkéit.</span><span class="sxs-lookup"><span data-stu-id="eac5c-116">The above command will update the tags for the CustomIpPrefix.</span></span>

## <span data-ttu-id="eac5c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eac5c-117">PARAMETERS</span></span>

### <span data-ttu-id="eac5c-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eac5c-118">-AsJob</span></span>
<span data-ttu-id="eac5c-119">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="eac5c-119">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eac5c-120">-Commission</span><span class="sxs-lookup"><span data-stu-id="eac5c-120">-Commission</span></span>
<span data-ttu-id="eac5c-121">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="eac5c-121">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eac5c-122">-Dekomera</span><span class="sxs-lookup"><span data-stu-id="eac5c-122">-Decomission</span></span>
<span data-ttu-id="eac5c-123">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="eac5c-123">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eac5c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eac5c-124">-DefaultProfile</span></span>
<span data-ttu-id="eac5c-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eac5c-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eac5c-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eac5c-126">-InputObject</span></span>
<span data-ttu-id="eac5c-127">A beállítható CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="eac5c-127">The CustomIpPrefix to set.</span></span>

```yaml
Type: PSCustomIpPrefix
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eac5c-128">-Name</span><span class="sxs-lookup"><span data-stu-id="eac5c-128">-Name</span></span>
<span data-ttu-id="eac5c-129">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="eac5c-129">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eac5c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eac5c-130">-ResourceGroupName</span></span>
<span data-ttu-id="eac5c-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="eac5c-131">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eac5c-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eac5c-132">-ResourceId</span></span>
<span data-ttu-id="eac5c-133">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="eac5c-133">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eac5c-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="eac5c-134">-Tag</span></span>
<span data-ttu-id="eac5c-135">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="eac5c-135">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Hashtable
Parameter Sets: SetByInputObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eac5c-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eac5c-136">-Confirm</span></span>
<span data-ttu-id="eac5c-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="eac5c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eac5c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eac5c-138">-WhatIf</span></span>
<span data-ttu-id="eac5c-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="eac5c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eac5c-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eac5c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eac5c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eac5c-141">CommonParameters</span></span>
<span data-ttu-id="eac5c-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eac5c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eac5c-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eac5c-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eac5c-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eac5c-144">INPUTS</span></span>

### <span data-ttu-id="eac5c-145">System.String</span><span class="sxs-lookup"><span data-stu-id="eac5c-145">System.String</span></span>

### <span data-ttu-id="eac5c-146">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="eac5c-146">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

### <span data-ttu-id="eac5c-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="eac5c-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="eac5c-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eac5c-148">OUTPUTS</span></span>

### <span data-ttu-id="eac5c-149">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="eac5c-149">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="eac5c-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="eac5c-150">NOTES</span></span>

## <span data-ttu-id="eac5c-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eac5c-151">RELATED LINKS</span></span>

[<span data-ttu-id="eac5c-152">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="eac5c-152">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="eac5c-153">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="eac5c-153">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="eac5c-154">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="eac5c-154">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)