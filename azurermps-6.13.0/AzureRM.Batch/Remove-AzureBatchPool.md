---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DB0A8E4B-AD3F-4BAC-A0B2-031913E019D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchPool.md
ms.openlocfilehash: 4cfb497b98d20b5cf3741c90934e9e104b93ddcb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492872"
---
# <span data-ttu-id="d11e6-101">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="d11e6-101">Remove-AzureBatchPool</span></span>

## <span data-ttu-id="d11e6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d11e6-102">SYNOPSIS</span></span>
<span data-ttu-id="d11e6-103">Törli a megadott köteg-készletet.</span><span class="sxs-lookup"><span data-stu-id="d11e6-103">Deletes the specified Batch pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d11e6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d11e6-104">SYNTAX</span></span>

```
Remove-AzureBatchPool [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d11e6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d11e6-105">DESCRIPTION</span></span>
<span data-ttu-id="d11e6-106">A **Remove-AzureBatchPool** parancsmag törli a megadott Azure-köteg készletet.</span><span class="sxs-lookup"><span data-stu-id="d11e6-106">The **Remove-AzureBatchPool** cmdlet deletes the specified Azure Batch pool.</span></span>
<span data-ttu-id="d11e6-107">Csak akkor kér megerősítést, ha az *erő* paramétert használja.</span><span class="sxs-lookup"><span data-stu-id="d11e6-107">You are prompted for confirmation unless you use the *Force* parameter.</span></span>

## <span data-ttu-id="d11e6-108">Példák</span><span class="sxs-lookup"><span data-stu-id="d11e6-108">EXAMPLES</span></span>

### <span data-ttu-id="d11e6-109">1. példa: egy köteg-készlet törlése a készlet-AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="d11e6-109">Example 1: Delete a Batch pool by pool ID</span></span>
```
PS C:\>Remove-AzureBatchPool -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="d11e6-110">Ez a parancs törli a készletet az ID MyPool.</span><span class="sxs-lookup"><span data-stu-id="d11e6-110">This command deletes the pool with ID MyPool.</span></span>
<span data-ttu-id="d11e6-111">A rendszer megerősítést kér a felhasználótól a törlési művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="d11e6-111">The user is prompted for confirmation before the delete operation takes place.</span></span>

### <span data-ttu-id="d11e6-112">2. példa: az összes kötegelt készlet törlése kényszerítve</span><span class="sxs-lookup"><span data-stu-id="d11e6-112">Example 2: Delete all Batch pools by force</span></span>
```
PS C:\>Get-AzureBatchPool -BatchContext $Context | Remove-AzureBatchPool -Force -BatchContext $Context
```

<span data-ttu-id="d11e6-113">Ez a parancs törli az összes köteg-gyűjtőt.</span><span class="sxs-lookup"><span data-stu-id="d11e6-113">This command deletes all Batch pools.</span></span>
<span data-ttu-id="d11e6-114">Mivel az *erő* paraméter megtalálható, a megerősítést kérő üzenet le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="d11e6-114">Because the *Force* parameter is present, the confirmation prompt is suppressed.</span></span>

## <span data-ttu-id="d11e6-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d11e6-115">PARAMETERS</span></span>

### <span data-ttu-id="d11e6-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d11e6-116">-BatchContext</span></span>
<span data-ttu-id="d11e6-117">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="d11e6-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d11e6-118">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="d11e6-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d11e6-119">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="d11e6-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d11e6-120">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="d11e6-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d11e6-121">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="d11e6-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d11e6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d11e6-122">-DefaultProfile</span></span>
<span data-ttu-id="d11e6-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d11e6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d11e6-124">-Force</span><span class="sxs-lookup"><span data-stu-id="d11e6-124">-Force</span></span>
<span data-ttu-id="d11e6-125">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="d11e6-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d11e6-126">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="d11e6-126">-Id</span></span>
<span data-ttu-id="d11e6-127">A törlendő készlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d11e6-127">Specifies the ID of the pool to delete.</span></span>
<span data-ttu-id="d11e6-128">A helyettesítő karakterek nem adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="d11e6-128">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="d11e6-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d11e6-129">-Confirm</span></span>
<span data-ttu-id="d11e6-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d11e6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d11e6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d11e6-131">-WhatIf</span></span>
<span data-ttu-id="d11e6-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d11e6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d11e6-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d11e6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d11e6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d11e6-134">CommonParameters</span></span>
<span data-ttu-id="d11e6-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d11e6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d11e6-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d11e6-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d11e6-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d11e6-137">INPUTS</span></span>

### <span data-ttu-id="d11e6-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d11e6-138">System.String</span></span>

### <span data-ttu-id="d11e6-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d11e6-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="d11e6-140">Paraméterek: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d11e6-140">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="d11e6-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d11e6-141">OUTPUTS</span></span>

### <span data-ttu-id="d11e6-142">System. Void</span><span class="sxs-lookup"><span data-stu-id="d11e6-142">System.Void</span></span>

## <span data-ttu-id="d11e6-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d11e6-143">NOTES</span></span>

## <span data-ttu-id="d11e6-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d11e6-144">RELATED LINKS</span></span>

[<span data-ttu-id="d11e6-145">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="d11e6-145">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="d11e6-146">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="d11e6-146">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="d11e6-147">Új – AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="d11e6-147">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="d11e6-148">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d11e6-148">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


