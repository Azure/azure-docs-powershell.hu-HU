---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
ms.openlocfilehash: 2e474462983f15c0d58f8ada60b907c100508c6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495475"
---
# <span data-ttu-id="13746-101">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="13746-101">Remove-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="13746-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="13746-102">SYNOPSIS</span></span>
<span data-ttu-id="13746-103">A kötegelt feladat ütemezése törlődik.</span><span class="sxs-lookup"><span data-stu-id="13746-103">Removes a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13746-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="13746-104">SYNTAX</span></span>

```
Remove-AzureBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13746-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="13746-105">DESCRIPTION</span></span>
<span data-ttu-id="13746-106">A **Remove-AzureBatchJobSchedule** parancsmag az Azure-kötegek ütemtervét távolítja el.</span><span class="sxs-lookup"><span data-stu-id="13746-106">The **Remove-AzureBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="13746-107">Példák</span><span class="sxs-lookup"><span data-stu-id="13746-107">EXAMPLES</span></span>

## <span data-ttu-id="13746-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="13746-108">PARAMETERS</span></span>

### <span data-ttu-id="13746-109">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="13746-109">-BatchContext</span></span>
<span data-ttu-id="13746-110">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="13746-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="13746-111">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="13746-111">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="13746-112">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="13746-112">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="13746-113">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="13746-113">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="13746-114">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="13746-114">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13746-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13746-115">-DefaultProfile</span></span>
<span data-ttu-id="13746-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="13746-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13746-117">-Force</span><span class="sxs-lookup"><span data-stu-id="13746-117">-Force</span></span>
<span data-ttu-id="13746-118">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="13746-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="13746-119">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="13746-119">-Id</span></span>
<span data-ttu-id="13746-120">Az eltávolítandó munkaütemezés AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="13746-120">Specifies the ID of the job schedule to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13746-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="13746-121">-Confirm</span></span>
<span data-ttu-id="13746-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="13746-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13746-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13746-123">-WhatIf</span></span>
<span data-ttu-id="13746-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="13746-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13746-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="13746-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13746-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13746-126">CommonParameters</span></span>
<span data-ttu-id="13746-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="13746-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13746-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13746-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13746-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="13746-129">INPUTS</span></span>

### <span data-ttu-id="13746-130">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="13746-130">BatchAccountContext</span></span>
<span data-ttu-id="13746-131">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="13746-131">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="13746-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13746-132">OUTPUTS</span></span>

## <span data-ttu-id="13746-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="13746-133">NOTES</span></span>

## <span data-ttu-id="13746-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13746-134">RELATED LINKS</span></span>

[<span data-ttu-id="13746-135">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="13746-135">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="13746-136">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="13746-136">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="13746-137">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="13746-137">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="13746-138">Új – AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="13746-138">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="13746-139">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="13746-139">Set-AzureBatchJobSchedule</span></span>](./Set-AzureBatchJobSchedule.md)

[<span data-ttu-id="13746-140">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="13746-140">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


