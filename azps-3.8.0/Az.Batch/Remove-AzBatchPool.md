---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DB0A8E4B-AD3F-4BAC-A0B2-031913E019D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
ms.openlocfilehash: ce2a7c6d01af33de585d4ac8adef83d03dbd33bc
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "94017205"
---
# <span data-ttu-id="7270a-101">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="7270a-101">Remove-AzBatchPool</span></span>

## <span data-ttu-id="7270a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7270a-102">SYNOPSIS</span></span>
<span data-ttu-id="7270a-103">Törli a megadott köteg-készletet.</span><span class="sxs-lookup"><span data-stu-id="7270a-103">Deletes the specified Batch pool.</span></span>

## <span data-ttu-id="7270a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7270a-104">SYNTAX</span></span>

```
Remove-AzBatchPool [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7270a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7270a-105">DESCRIPTION</span></span>
<span data-ttu-id="7270a-106">A **Remove-AzBatchPool** parancsmag törli a megadott Azure-köteg készletet.</span><span class="sxs-lookup"><span data-stu-id="7270a-106">The **Remove-AzBatchPool** cmdlet deletes the specified Azure Batch pool.</span></span>
<span data-ttu-id="7270a-107">Csak akkor kér megerősítést, ha az *erő* paramétert használja.</span><span class="sxs-lookup"><span data-stu-id="7270a-107">You are prompted for confirmation unless you use the *Force* parameter.</span></span>

## <span data-ttu-id="7270a-108">Példák</span><span class="sxs-lookup"><span data-stu-id="7270a-108">EXAMPLES</span></span>

### <span data-ttu-id="7270a-109">1. példa: egy köteg-készlet törlése a készlet-AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="7270a-109">Example 1: Delete a Batch pool by pool ID</span></span>
```
PS C:\>Remove-AzBatchPool -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="7270a-110">Ez a parancs törli a készletet az ID MyPool.</span><span class="sxs-lookup"><span data-stu-id="7270a-110">This command deletes the pool with ID MyPool.</span></span>
<span data-ttu-id="7270a-111">A rendszer megerősítést kér a felhasználótól a törlési művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="7270a-111">The user is prompted for confirmation before the delete operation takes place.</span></span>

### <span data-ttu-id="7270a-112">2. példa: az összes kötegelt készlet törlése kényszerítve</span><span class="sxs-lookup"><span data-stu-id="7270a-112">Example 2: Delete all Batch pools by force</span></span>
```
PS C:\>Get-AzBatchPool -BatchContext $Context | Remove-AzBatchPool -Force -BatchContext $Context
```

<span data-ttu-id="7270a-113">Ez a parancs törli az összes köteg-gyűjtőt.</span><span class="sxs-lookup"><span data-stu-id="7270a-113">This command deletes all Batch pools.</span></span>
<span data-ttu-id="7270a-114">Mivel az *erő* paraméter megtalálható, a megerősítést kérő üzenet le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="7270a-114">Because the *Force* parameter is present, the confirmation prompt is suppressed.</span></span>

## <span data-ttu-id="7270a-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7270a-115">PARAMETERS</span></span>

### <span data-ttu-id="7270a-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="7270a-116">-BatchContext</span></span>
<span data-ttu-id="7270a-117">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="7270a-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7270a-118">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="7270a-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="7270a-119">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKey parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="7270a-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="7270a-120">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="7270a-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="7270a-121">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="7270a-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7270a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7270a-122">-DefaultProfile</span></span>
<span data-ttu-id="7270a-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7270a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7270a-124">-Force</span><span class="sxs-lookup"><span data-stu-id="7270a-124">-Force</span></span>
<span data-ttu-id="7270a-125">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="7270a-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7270a-126">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="7270a-126">-Id</span></span>
<span data-ttu-id="7270a-127">A törlendő készlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7270a-127">Specifies the ID of the pool to delete.</span></span>
<span data-ttu-id="7270a-128">A helyettesítő karakterek nem adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="7270a-128">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7270a-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7270a-129">-Confirm</span></span>
<span data-ttu-id="7270a-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7270a-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7270a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7270a-131">-WhatIf</span></span>
<span data-ttu-id="7270a-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7270a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7270a-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7270a-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7270a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7270a-134">CommonParameters</span></span>
<span data-ttu-id="7270a-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7270a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7270a-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7270a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7270a-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7270a-137">INPUTS</span></span>

### <span data-ttu-id="7270a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="7270a-138">System.String</span></span>

### <span data-ttu-id="7270a-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7270a-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="7270a-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7270a-140">OUTPUTS</span></span>

### <span data-ttu-id="7270a-141">System. Void</span><span class="sxs-lookup"><span data-stu-id="7270a-141">System.Void</span></span>

## <span data-ttu-id="7270a-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7270a-142">NOTES</span></span>

## <span data-ttu-id="7270a-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7270a-143">RELATED LINKS</span></span>

[<span data-ttu-id="7270a-144">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="7270a-144">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="7270a-145">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="7270a-145">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="7270a-146">Új – AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="7270a-146">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="7270a-147">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="7270a-147">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


