---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzCustomIpPrefix.md
ms.openlocfilehash: bcb250c8967c10e5b200e62d843e99eab374d81d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188244"
---
# <span data-ttu-id="62e6d-101">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="62e6d-101">Remove-AzCustomIpPrefix</span></span>

## <span data-ttu-id="62e6d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="62e6d-102">SYNOPSIS</span></span>
<span data-ttu-id="62e6d-103">CustomIpPrefix eltávolítása</span><span class="sxs-lookup"><span data-stu-id="62e6d-103">Removes a CustomIpPrefix</span></span>

## <span data-ttu-id="62e6d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="62e6d-104">SYNTAX</span></span>

### <span data-ttu-id="62e6d-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="62e6d-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62e6d-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="62e6d-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzCustomIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62e6d-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="62e6d-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62e6d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="62e6d-108">DESCRIPTION</span></span>
<span data-ttu-id="62e6d-109">A **Remove-AzCustomIpPrefix** parancsmag eltávolítja a CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="62e6d-109">The **Remove-AzCustomIpPrefix** cmdlet removes a CustomIpPrefix.</span></span>

## <span data-ttu-id="62e6d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="62e6d-110">EXAMPLES</span></span>

### <span data-ttu-id="62e6d-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="62e6d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="62e6d-112">Eltávolítja a CustomIpPrefix nevű $prefixName az erőforráscsoport csoportból $rgName</span><span class="sxs-lookup"><span data-stu-id="62e6d-112">Removes the CustomIpPrefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="62e6d-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="62e6d-113">PARAMETERS</span></span>

### <span data-ttu-id="62e6d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="62e6d-114">-AsJob</span></span>
<span data-ttu-id="62e6d-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="62e6d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="62e6d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62e6d-116">-DefaultProfile</span></span>
<span data-ttu-id="62e6d-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="62e6d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62e6d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="62e6d-118">-Force</span></span>
<span data-ttu-id="62e6d-119">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="62e6d-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="62e6d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62e6d-120">-InputObject</span></span>
<span data-ttu-id="62e6d-121">Egy customIpPrefix objektum.</span><span class="sxs-lookup"><span data-stu-id="62e6d-121">A customIpPrefix object.</span></span>

```yaml
Type: PSCustomIpPrefix
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62e6d-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="62e6d-122">-Name</span></span>
<span data-ttu-id="62e6d-123">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="62e6d-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62e6d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62e6d-124">-PassThru</span></span>
<span data-ttu-id="62e6d-125">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="62e6d-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="62e6d-126">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="62e6d-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="62e6d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62e6d-127">-ResourceGroupName</span></span>
<span data-ttu-id="62e6d-128">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="62e6d-128">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62e6d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62e6d-129">-ResourceId</span></span>
<span data-ttu-id="62e6d-130">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="62e6d-130">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62e6d-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="62e6d-131">-Confirm</span></span>
<span data-ttu-id="62e6d-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="62e6d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62e6d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62e6d-133">-WhatIf</span></span>
<span data-ttu-id="62e6d-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="62e6d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62e6d-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="62e6d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62e6d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62e6d-136">CommonParameters</span></span>
<span data-ttu-id="62e6d-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="62e6d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62e6d-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="62e6d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62e6d-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="62e6d-139">INPUTS</span></span>

### <span data-ttu-id="62e6d-140">System. String</span><span class="sxs-lookup"><span data-stu-id="62e6d-140">System.String</span></span>

### <span data-ttu-id="62e6d-141">Microsoft. Azure. commands. Network. models. PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="62e6d-141">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="62e6d-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="62e6d-142">OUTPUTS</span></span>

### <span data-ttu-id="62e6d-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="62e6d-143">System.Boolean</span></span>

## <span data-ttu-id="62e6d-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="62e6d-144">NOTES</span></span>

## <span data-ttu-id="62e6d-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="62e6d-145">RELATED LINKS</span></span>

[<span data-ttu-id="62e6d-146">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="62e6d-146">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="62e6d-147">Új – AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="62e6d-147">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="62e6d-148">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="62e6d-148">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)