---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: CB2F472B-C792-4A11-A055-F4161DCFBB28
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJob.md
ms.openlocfilehash: 0d210056670baa974c7bf11e9c44142c11f2721e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501935"
---
# <span data-ttu-id="dc003-101">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="dc003-101">Remove-AzureBatchJob</span></span>

## <span data-ttu-id="dc003-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dc003-102">SYNOPSIS</span></span>
<span data-ttu-id="dc003-103">Töröl egy kötegelt feladatot.</span><span class="sxs-lookup"><span data-stu-id="dc003-103">Deletes a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc003-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dc003-104">SYNTAX</span></span>

```
Remove-AzureBatchJob [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc003-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dc003-105">DESCRIPTION</span></span>
<span data-ttu-id="dc003-106">A **Remove-AzureBatchJob** parancsmag egy Azure kötegelt feladatot töröl.</span><span class="sxs-lookup"><span data-stu-id="dc003-106">The **Remove-AzureBatchJob** cmdlet deletes an Azure Batch job.</span></span>
<span data-ttu-id="dc003-107">Ez a parancsmag arra kéri, hogy erősítse meg a feladat eltávolítását, hacsak nem adja meg az *erő* paramétert.</span><span class="sxs-lookup"><span data-stu-id="dc003-107">This cmdlet prompts you for confirmation before it removes a job, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="dc003-108">Példák</span><span class="sxs-lookup"><span data-stu-id="dc003-108">EXAMPLES</span></span>

### <span data-ttu-id="dc003-109">Példa 1: kötegelt feladat törlése</span><span class="sxs-lookup"><span data-stu-id="dc003-109">Example 1: Delete a Batch job</span></span>
```
PS C:\>Remove-AzureBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="dc003-110">Ez a parancs törli azt a feladatot, amely a 000001 AZONOSÍTÓval rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="dc003-110">This command deletes the job that has the ID Job-000001.</span></span>
<span data-ttu-id="dc003-111">A parancs a feladat törlése előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dc003-111">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="dc003-112">A Get-AzureRmBatchAccountKeys parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="dc003-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="dc003-113">2. példa: kötegelt feladat törlése megerősítés nélkül a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="dc003-113">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchJob -Id "Job-000002" -BatchContext $Context | Remove-AzureBatchJob -Force -BatchContext $Context
```

<span data-ttu-id="dc003-114">Ez a parancs a Get-AzureBatchJob parancsmaggal a 000002 AZONOSÍTÓJÚ feladatot kapja.</span><span class="sxs-lookup"><span data-stu-id="dc003-114">This command gets the job that has the ID Job-000002 by using the Get-AzureBatchJob cmdlet.</span></span>
<span data-ttu-id="dc003-115">A parancs a munkafolyamatot a csővezeték-kezelő használatával továbbítja az aktuális parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="dc003-115">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="dc003-116">A parancs törli azt a feladatot.</span><span class="sxs-lookup"><span data-stu-id="dc003-116">The command deletes that job.</span></span>
<span data-ttu-id="dc003-117">Mivel a parancs az *erő* paramétert tartalmazza, nem kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dc003-117">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="dc003-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dc003-118">PARAMETERS</span></span>

### <span data-ttu-id="dc003-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="dc003-119">-BatchContext</span></span>
<span data-ttu-id="dc003-120">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="dc003-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="dc003-121">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="dc003-121">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="dc003-122">-Force</span><span class="sxs-lookup"><span data-stu-id="dc003-122">-Force</span></span>
<span data-ttu-id="dc003-123">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="dc003-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dc003-124">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="dc003-124">-Id</span></span>
<span data-ttu-id="dc003-125">Annak a feladatnak az AZONOSÍTÓját adja meg, amelyre a parancsmag törlődik.</span><span class="sxs-lookup"><span data-stu-id="dc003-125">Specifies the ID of the job that this cmdlet deletes.</span></span>
<span data-ttu-id="dc003-126">A helyettesítő karakterek nem adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="dc003-126">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="dc003-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dc003-127">-Confirm</span></span>
<span data-ttu-id="dc003-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dc003-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc003-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc003-129">-WhatIf</span></span>
<span data-ttu-id="dc003-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dc003-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc003-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dc003-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc003-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc003-132">-DefaultProfile</span></span>
<span data-ttu-id="dc003-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dc003-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc003-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc003-134">CommonParameters</span></span>
<span data-ttu-id="dc003-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dc003-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc003-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc003-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc003-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc003-137">INPUTS</span></span>

### <span data-ttu-id="dc003-138">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="dc003-138">BatchAccountContext</span></span>
<span data-ttu-id="dc003-139">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="dc003-139">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="dc003-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc003-140">OUTPUTS</span></span>

## <span data-ttu-id="dc003-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dc003-141">NOTES</span></span>

## <span data-ttu-id="dc003-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dc003-142">RELATED LINKS</span></span>

[<span data-ttu-id="dc003-143">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="dc003-143">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="dc003-144">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="dc003-144">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="dc003-145">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="dc003-145">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="dc003-146">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="dc003-146">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="dc003-147">Új – AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="dc003-147">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="dc003-148">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="dc003-148">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="dc003-149">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="dc003-149">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


