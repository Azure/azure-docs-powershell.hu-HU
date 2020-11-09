---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
ms.openlocfilehash: 65d47c57720e66ecad8267ae45f9e08eb3e4c4ca
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303079"
---
# <span data-ttu-id="7cdf7-101">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="7cdf7-101">Update-AzCustomIpPrefix</span></span>

## <span data-ttu-id="7cdf7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7cdf7-102">SYNOPSIS</span></span>
<span data-ttu-id="7cdf7-103">CustomIpPrefix frissítése</span><span class="sxs-lookup"><span data-stu-id="7cdf7-103">Updates a CustomIpPrefix</span></span>

## <span data-ttu-id="7cdf7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7cdf7-104">SYNTAX</span></span>

### <span data-ttu-id="7cdf7-105">UpdateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cdf7-105">UpdateByNameParameterSet</span></span>
```
Update-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Commission] [-Decomission]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7cdf7-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cdf7-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Commission] [-Decomission] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cdf7-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cdf7-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzCustomIpPrefix -ResourceId <String> [-Commission] [-Decomission] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cdf7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7cdf7-108">DESCRIPTION</span></span>
<span data-ttu-id="7cdf7-109">Az **Update-AzCustomIpPrefix** parancsmag segítségével a felhasználó megadhatja a CustomIpPrefix, illetve szerkesztheti az erőforrás címkéit.</span><span class="sxs-lookup"><span data-stu-id="7cdf7-109">The **Update-AzCustomIpPrefix** cmdlet allows the user to either commission or decommission their CustomIpPrefix, or edit the tags of the resource.</span></span>

## <span data-ttu-id="7cdf7-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7cdf7-110">EXAMPLES</span></span>

### <span data-ttu-id="7cdf7-111">1. példa: a Bizottság a CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="7cdf7-111">Example 1 : Commission the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Commission
```

<span data-ttu-id="7cdf7-112">A fenti parancs elindítja a CustomIpPrefix üzembe helyezési folyamatát.</span><span class="sxs-lookup"><span data-stu-id="7cdf7-112">The above command will start the commissioning process of the CustomIpPrefix.</span></span>

### <span data-ttu-id="7cdf7-113">2. példa: a CustomIpPrefix leszerelése</span><span class="sxs-lookup"><span data-stu-id="7cdf7-113">Example 2 : Decommission the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Decommission
```

<span data-ttu-id="7cdf7-114">A fenti parancs elindítja a CustomIpPrefix de-megbízási folyamatát.</span><span class="sxs-lookup"><span data-stu-id="7cdf7-114">The above command will start the de-commissioning process of the CustomIpPrefix.</span></span>

### <span data-ttu-id="7cdf7-115">3. példa: a CustomIpPrefix címkék frissítése</span><span class="sxs-lookup"><span data-stu-id="7cdf7-115">Example 3 : Update tags for the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Tag $tags
```

<span data-ttu-id="7cdf7-116">A fenti parancs frissíti a CustomIpPrefix címkéit.</span><span class="sxs-lookup"><span data-stu-id="7cdf7-116">The above command will update the tags for the CustomIpPrefix.</span></span>

## <span data-ttu-id="7cdf7-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7cdf7-117">PARAMETERS</span></span>

### <span data-ttu-id="7cdf7-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7cdf7-118">-AsJob</span></span>
<span data-ttu-id="7cdf7-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="7cdf7-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7cdf7-120">-Jutalék</span><span class="sxs-lookup"><span data-stu-id="7cdf7-120">-Commission</span></span>
<span data-ttu-id="7cdf7-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="7cdf7-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7cdf7-122">-Decomission</span><span class="sxs-lookup"><span data-stu-id="7cdf7-122">-Decomission</span></span>
<span data-ttu-id="7cdf7-123">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="7cdf7-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7cdf7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cdf7-124">-DefaultProfile</span></span>
<span data-ttu-id="7cdf7-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7cdf7-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cdf7-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7cdf7-126">-InputObject</span></span>
<span data-ttu-id="7cdf7-127">A beállítani kívánt CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="7cdf7-127">The CustomIpPrefix to set.</span></span>

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

### <span data-ttu-id="7cdf7-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7cdf7-128">-Name</span></span>
<span data-ttu-id="7cdf7-129">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="7cdf7-129">The resource name.</span></span>

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

### <span data-ttu-id="7cdf7-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cdf7-130">-ResourceGroupName</span></span>
<span data-ttu-id="7cdf7-131">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="7cdf7-131">The resource group name.</span></span>

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

### <span data-ttu-id="7cdf7-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7cdf7-132">-ResourceId</span></span>
<span data-ttu-id="7cdf7-133">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="7cdf7-133">The resource Id.</span></span>

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

### <span data-ttu-id="7cdf7-134">-Címke</span><span class="sxs-lookup"><span data-stu-id="7cdf7-134">-Tag</span></span>
<span data-ttu-id="7cdf7-135">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="7cdf7-135">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="7cdf7-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7cdf7-136">-Confirm</span></span>
<span data-ttu-id="7cdf7-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7cdf7-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cdf7-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cdf7-138">-WhatIf</span></span>
<span data-ttu-id="7cdf7-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7cdf7-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cdf7-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7cdf7-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cdf7-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cdf7-141">CommonParameters</span></span>
<span data-ttu-id="7cdf7-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7cdf7-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cdf7-143">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7cdf7-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cdf7-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7cdf7-144">INPUTS</span></span>

### <span data-ttu-id="7cdf7-145">System. String</span><span class="sxs-lookup"><span data-stu-id="7cdf7-145">System.String</span></span>

### <span data-ttu-id="7cdf7-146">Microsoft. Azure. commands. Network. models. PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="7cdf7-146">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

### <span data-ttu-id="7cdf7-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7cdf7-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7cdf7-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7cdf7-148">OUTPUTS</span></span>

### <span data-ttu-id="7cdf7-149">Microsoft. Azure. commands. Network. models. PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="7cdf7-149">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="7cdf7-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7cdf7-150">NOTES</span></span>

## <span data-ttu-id="7cdf7-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7cdf7-151">RELATED LINKS</span></span>

[<span data-ttu-id="7cdf7-152">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="7cdf7-152">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="7cdf7-153">Új – AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="7cdf7-153">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="7cdf7-154">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="7cdf7-154">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)