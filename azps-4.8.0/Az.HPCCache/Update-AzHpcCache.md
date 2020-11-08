---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/update-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Update-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Update-AzHpcCache.md
ms.openlocfilehash: 8f84323df269d8e0fbd0f60525e54595ef89f3e8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184935"
---
# <span data-ttu-id="cca84-101">Update-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="cca84-101">Update-AzHpcCache</span></span>

## <span data-ttu-id="cca84-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cca84-102">SYNOPSIS</span></span>
<span data-ttu-id="cca84-103">Frissíti a HPC-gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="cca84-103">Updates a HPC Cache.</span></span>

## <span data-ttu-id="cca84-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cca84-104">SYNTAX</span></span>

### <span data-ttu-id="cca84-105">FlushParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cca84-105">FlushParameterSet (Default)</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> [-Flush] [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cca84-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cca84-106">ByResourceIdParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cca84-107">UpgradeParameterSet</span><span class="sxs-lookup"><span data-stu-id="cca84-107">UpgradeParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> [-Upgrade] [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cca84-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cca84-108">ByObjectParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> -InputObject <PSHPCCache> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cca84-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="cca84-109">DESCRIPTION</span></span>
<span data-ttu-id="cca84-110">Az **Update-AzHpcCache** parancsmag az Azure HPC-gyorsítótárát frissíti.</span><span class="sxs-lookup"><span data-stu-id="cca84-110">The **Update-AzHpcCache** cmdlet updates a Azure HPC Cache.</span></span>

## <span data-ttu-id="cca84-111">Példák</span><span class="sxs-lookup"><span data-stu-id="cca84-111">EXAMPLES</span></span>

### <span data-ttu-id="cca84-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cca84-112">Example 1</span></span>
```powershell
PS C:\> Update-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="cca84-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cca84-113">PARAMETERS</span></span>

### <span data-ttu-id="cca84-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cca84-114">-AsJob</span></span>
<span data-ttu-id="cca84-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="cca84-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cca84-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cca84-116">-DefaultProfile</span></span>
<span data-ttu-id="cca84-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cca84-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cca84-118">-Flush</span><span class="sxs-lookup"><span data-stu-id="cca84-118">-Flush</span></span>
<span data-ttu-id="cca84-119">A HPC-gyorsítótár kiürítése</span><span class="sxs-lookup"><span data-stu-id="cca84-119">Flushes HPC Cache.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FlushParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cca84-120">-Force</span><span class="sxs-lookup"><span data-stu-id="cca84-120">-Force</span></span>
<span data-ttu-id="cca84-121">Azt jelzi, hogy a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cca84-121">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="cca84-122">Ez a parancsmag alapértelmezés szerint arra kéri, hogy erősítse meg, hogy szeretné-e frissíteni a gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="cca84-122">By default, this cmdlet prompts you to confirm that you want to update the cache.</span></span>

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

### <span data-ttu-id="cca84-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cca84-123">-InputObject</span></span>
<span data-ttu-id="cca84-124">A frissítendő gyorsítótár-objektum.</span><span class="sxs-lookup"><span data-stu-id="cca84-124">The cache object to update.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cca84-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cca84-125">-Name</span></span>
<span data-ttu-id="cca84-126">A gyorsítótár neve.</span><span class="sxs-lookup"><span data-stu-id="cca84-126">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CacheName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cca84-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cca84-127">-PassThru</span></span>
<span data-ttu-id="cca84-128">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="cca84-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cca84-129">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="cca84-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cca84-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cca84-130">-ResourceGroupName</span></span>
<span data-ttu-id="cca84-131">Annak az erőforráscsoport-csoportnak a neve, amely alatt frissíteni szeretné a gyorsítótárat.</span><span class="sxs-lookup"><span data-stu-id="cca84-131">Name of resource group under which you want to update cache.</span></span>

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

### <span data-ttu-id="cca84-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cca84-132">-ResourceId</span></span>
<span data-ttu-id="cca84-133">A gyorsítótár erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="cca84-133">The resource id of the Cache</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cca84-134">-Upgrade</span><span class="sxs-lookup"><span data-stu-id="cca84-134">-Upgrade</span></span>
<span data-ttu-id="cca84-135">Frissítse a HpcCache.</span><span class="sxs-lookup"><span data-stu-id="cca84-135">Upgrade HpcCache.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpgradeParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cca84-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cca84-136">-Confirm</span></span>
<span data-ttu-id="cca84-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cca84-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cca84-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cca84-138">-WhatIf</span></span>
<span data-ttu-id="cca84-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cca84-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cca84-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cca84-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cca84-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cca84-141">CommonParameters</span></span>
<span data-ttu-id="cca84-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cca84-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cca84-143">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cca84-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cca84-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cca84-144">INPUTS</span></span>

### <span data-ttu-id="cca84-145">System. String</span><span class="sxs-lookup"><span data-stu-id="cca84-145">System.String</span></span>

## <span data-ttu-id="cca84-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cca84-146">OUTPUTS</span></span>

## <span data-ttu-id="cca84-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cca84-147">NOTES</span></span>

## <span data-ttu-id="cca84-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cca84-148">RELATED LINKS</span></span>