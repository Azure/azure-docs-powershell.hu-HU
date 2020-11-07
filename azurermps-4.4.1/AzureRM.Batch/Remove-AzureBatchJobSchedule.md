---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
ms.openlocfilehash: 673d9e5034b1e7c97d3b6b7cfdd6f89e9a79a34f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672770"
---
# <span data-ttu-id="6d8ea-101">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6d8ea-101">Remove-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="6d8ea-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6d8ea-102">SYNOPSIS</span></span>
<span data-ttu-id="6d8ea-103">A kötegelt feladat ütemezése törlődik.</span><span class="sxs-lookup"><span data-stu-id="6d8ea-103">Removes a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d8ea-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6d8ea-104">SYNTAX</span></span>

```
Remove-AzureBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d8ea-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6d8ea-105">DESCRIPTION</span></span>
<span data-ttu-id="6d8ea-106">A **Remove-AzureBatchJobSchedule** parancsmag az Azure-kötegek ütemtervét távolítja el.</span><span class="sxs-lookup"><span data-stu-id="6d8ea-106">The **Remove-AzureBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="6d8ea-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6d8ea-107">EXAMPLES</span></span>

## <span data-ttu-id="6d8ea-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6d8ea-108">PARAMETERS</span></span>

### <span data-ttu-id="6d8ea-109">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6d8ea-109">-BatchContext</span></span>
<span data-ttu-id="6d8ea-110">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="6d8ea-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6d8ea-111">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="6d8ea-111">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="6d8ea-112">-Force</span><span class="sxs-lookup"><span data-stu-id="6d8ea-112">-Force</span></span>
<span data-ttu-id="6d8ea-113">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="6d8ea-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6d8ea-114">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="6d8ea-114">-Id</span></span>
<span data-ttu-id="6d8ea-115">Az eltávolítandó munkaütemezés AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6d8ea-115">Specifies the ID of the job schedule to remove.</span></span>

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

### <span data-ttu-id="6d8ea-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6d8ea-116">-Confirm</span></span>
<span data-ttu-id="6d8ea-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6d8ea-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d8ea-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d8ea-118">-WhatIf</span></span>
<span data-ttu-id="6d8ea-119">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6d8ea-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d8ea-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6d8ea-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d8ea-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d8ea-121">-DefaultProfile</span></span>
<span data-ttu-id="6d8ea-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6d8ea-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d8ea-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d8ea-123">CommonParameters</span></span>
<span data-ttu-id="6d8ea-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6d8ea-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d8ea-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d8ea-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d8ea-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d8ea-126">INPUTS</span></span>

### <span data-ttu-id="6d8ea-127">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6d8ea-127">BatchAccountContext</span></span>
<span data-ttu-id="6d8ea-128">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="6d8ea-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="6d8ea-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d8ea-129">OUTPUTS</span></span>

## <span data-ttu-id="6d8ea-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6d8ea-130">NOTES</span></span>

## <span data-ttu-id="6d8ea-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6d8ea-131">RELATED LINKS</span></span>

[<span data-ttu-id="6d8ea-132">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6d8ea-132">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="6d8ea-133">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6d8ea-133">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="6d8ea-134">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6d8ea-134">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="6d8ea-135">Új – AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6d8ea-135">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="6d8ea-136">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6d8ea-136">Set-AzureBatchJobSchedule</span></span>](./Set-AzureBatchJobSchedule.md)

[<span data-ttu-id="6d8ea-137">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6d8ea-137">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


