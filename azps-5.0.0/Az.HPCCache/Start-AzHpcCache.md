---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/start-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Start-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Start-AzHpcCache.md
ms.openlocfilehash: 7465a74db4da777d60e097fe959ef69bed11918c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187391"
---
# <span data-ttu-id="4d742-101">Start-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="4d742-101">Start-AzHpcCache</span></span>

## <span data-ttu-id="4d742-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4d742-102">SYNOPSIS</span></span>
<span data-ttu-id="4d742-103">Elindítja a HPC gyorsítótárát.</span><span class="sxs-lookup"><span data-stu-id="4d742-103">Starts HPC cache.</span></span>

## <span data-ttu-id="4d742-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4d742-104">SYNTAX</span></span>

### <span data-ttu-id="4d742-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4d742-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d742-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d742-106">ByResourceIdParameterSet</span></span>
```
Start-AzHpcCache -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d742-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d742-107">ByObjectParameterSet</span></span>
```
Start-AzHpcCache -InputObject <PSHPCCache> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d742-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4d742-108">DESCRIPTION</span></span>
<span data-ttu-id="4d742-109">A **Start-AzHpcCache** parancsmag az Azure HPC-gyorsítótárat indítja el.</span><span class="sxs-lookup"><span data-stu-id="4d742-109">The **Start-AzHpcCache** cmdlet starts a Azure HPC Cache.</span></span>

## <span data-ttu-id="4d742-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4d742-110">EXAMPLES</span></span>

### <span data-ttu-id="4d742-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4d742-111">Example 1</span></span>
```powershell
PS C:\> Start-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="4d742-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4d742-112">PARAMETERS</span></span>

### <span data-ttu-id="4d742-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d742-113">-AsJob</span></span>
<span data-ttu-id="4d742-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="4d742-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4d742-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d742-115">-DefaultProfile</span></span>
<span data-ttu-id="4d742-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4d742-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d742-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4d742-117">-Force</span></span>
<span data-ttu-id="4d742-118">Azt jelzi, hogy a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4d742-118">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="4d742-119">Ez a parancsmag alapértelmezés szerint arra kéri, hogy erősítse meg, hogy a gyorsítótárat szeretné elindítani.</span><span class="sxs-lookup"><span data-stu-id="4d742-119">By default, this cmdlet prompts you to confirm that you want to start the cache.</span></span>

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

### <span data-ttu-id="4d742-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d742-120">-InputObject</span></span>
<span data-ttu-id="4d742-121">Az elindítani kívánt gyorsítótár-objektum.</span><span class="sxs-lookup"><span data-stu-id="4d742-121">The cache object to start.</span></span>

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

### <span data-ttu-id="4d742-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4d742-122">-Name</span></span>
<span data-ttu-id="4d742-123">A gyorsítótár neve.</span><span class="sxs-lookup"><span data-stu-id="4d742-123">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: CacheName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d742-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4d742-124">-PassThru</span></span>
<span data-ttu-id="4d742-125">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="4d742-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4d742-126">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="4d742-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4d742-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d742-127">-ResourceGroupName</span></span>
<span data-ttu-id="4d742-128">Annak az erőforráscsoport-csoportnak a neve, amelynek a gyorsítótárát el szeretné indítani.</span><span class="sxs-lookup"><span data-stu-id="4d742-128">Name of resource group under which you want to start cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d742-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d742-129">-ResourceId</span></span>
<span data-ttu-id="4d742-130">A gyorsítótár erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="4d742-130">The resource id of the Cache</span></span>

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

### <span data-ttu-id="4d742-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4d742-131">-Confirm</span></span>
<span data-ttu-id="4d742-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4d742-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d742-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d742-133">-WhatIf</span></span>
<span data-ttu-id="4d742-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4d742-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4d742-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4d742-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d742-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d742-136">CommonParameters</span></span>
<span data-ttu-id="4d742-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4d742-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d742-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4d742-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d742-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d742-139">INPUTS</span></span>

### <span data-ttu-id="4d742-140">System. String</span><span class="sxs-lookup"><span data-stu-id="4d742-140">System.String</span></span>

## <span data-ttu-id="4d742-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d742-141">OUTPUTS</span></span>

## <span data-ttu-id="4d742-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4d742-142">NOTES</span></span>

## <span data-ttu-id="4d742-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4d742-143">RELATED LINKS</span></span>
