---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DB0A8E4B-AD3F-4BAC-A0B2-031913E019D4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchPool.md
ms.openlocfilehash: 01098a20ebb754d4445a85dd5a6bb0d327453234
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497875"
---
# <span data-ttu-id="f1a1b-101">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="f1a1b-101">Remove-AzureBatchPool</span></span>

## <span data-ttu-id="f1a1b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f1a1b-102">SYNOPSIS</span></span>
<span data-ttu-id="f1a1b-103">Törli a megadott köteg-készletet.</span><span class="sxs-lookup"><span data-stu-id="f1a1b-103">Deletes the specified Batch pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1a1b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f1a1b-104">SYNTAX</span></span>

```
Remove-AzureBatchPool [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1a1b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f1a1b-105">DESCRIPTION</span></span>
<span data-ttu-id="f1a1b-106">A **Remove-AzureBatchPool** parancsmag törli a megadott Azure-köteg készletet.</span><span class="sxs-lookup"><span data-stu-id="f1a1b-106">The **Remove-AzureBatchPool** cmdlet deletes the specified Azure Batch pool.</span></span>
<span data-ttu-id="f1a1b-107">Csak akkor kér megerősítést, ha az *erő* paramétert használja.</span><span class="sxs-lookup"><span data-stu-id="f1a1b-107">You are prompted for confirmation unless you use the *Force* parameter.</span></span>

## <span data-ttu-id="f1a1b-108">Példák</span><span class="sxs-lookup"><span data-stu-id="f1a1b-108">EXAMPLES</span></span>

### <span data-ttu-id="f1a1b-109">1. példa: egy köteg-készlet törlése a készlet-AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="f1a1b-109">Example 1: Delete a Batch pool by pool ID</span></span>
```
PS C:\>Remove-AzureBatchPool -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="f1a1b-110">Ez a parancs törli a készletet az ID MyPool.</span><span class="sxs-lookup"><span data-stu-id="f1a1b-110">This command deletes the pool with ID MyPool.</span></span>
<span data-ttu-id="f1a1b-111">A rendszer megerősítést kér a felhasználótól a törlési művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="f1a1b-111">The user is prompted for confirmation before the delete operation takes place.</span></span>

### <span data-ttu-id="f1a1b-112">2. példa: az összes kötegelt készlet törlése kényszerítve</span><span class="sxs-lookup"><span data-stu-id="f1a1b-112">Example 2: Delete all Batch pools by force</span></span>
```
PS C:\>Get-AzureBatchPool -BatchContext $Context | Remove-AzureBatchPool -Force -BatchContext $Context
```

<span data-ttu-id="f1a1b-113">Ez a parancs törli az összes köteg-gyűjtőt.</span><span class="sxs-lookup"><span data-stu-id="f1a1b-113">This command deletes all Batch pools.</span></span>
<span data-ttu-id="f1a1b-114">Mivel az *erő* paraméter megtalálható, a megerősítést kérő üzenet le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="f1a1b-114">Because the *Force* parameter is present, the confirmation prompt is suppressed.</span></span>

## <span data-ttu-id="f1a1b-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f1a1b-115">PARAMETERS</span></span>

### <span data-ttu-id="f1a1b-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f1a1b-116">-BatchContext</span></span>
<span data-ttu-id="f1a1b-117">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="f1a1b-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f1a1b-118">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f1a1b-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="f1a1b-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f1a1b-119">-Force</span></span>
<span data-ttu-id="f1a1b-120">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="f1a1b-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f1a1b-121">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="f1a1b-121">-Id</span></span>
<span data-ttu-id="f1a1b-122">A törlendő készlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f1a1b-122">Specifies the ID of the pool to delete.</span></span>
<span data-ttu-id="f1a1b-123">A helyettesítő karakterek nem adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="f1a1b-123">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="f1a1b-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f1a1b-124">-Confirm</span></span>
<span data-ttu-id="f1a1b-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f1a1b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1a1b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1a1b-126">-WhatIf</span></span>
<span data-ttu-id="f1a1b-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f1a1b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1a1b-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f1a1b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1a1b-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1a1b-129">-DefaultProfile</span></span>
<span data-ttu-id="f1a1b-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f1a1b-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1a1b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1a1b-131">CommonParameters</span></span>
<span data-ttu-id="f1a1b-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f1a1b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1a1b-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1a1b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1a1b-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1a1b-134">INPUTS</span></span>

### <span data-ttu-id="f1a1b-135">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f1a1b-135">BatchAccountContext</span></span>
<span data-ttu-id="f1a1b-136">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="f1a1b-136">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="f1a1b-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1a1b-137">OUTPUTS</span></span>

## <span data-ttu-id="f1a1b-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f1a1b-138">NOTES</span></span>

## <span data-ttu-id="f1a1b-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f1a1b-139">RELATED LINKS</span></span>

[<span data-ttu-id="f1a1b-140">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="f1a1b-140">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="f1a1b-141">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="f1a1b-141">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="f1a1b-142">Új – AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="f1a1b-142">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="f1a1b-143">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="f1a1b-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


