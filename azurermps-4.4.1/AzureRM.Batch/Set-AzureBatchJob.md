---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
ms.openlocfilehash: eb15991e0bf7aefd60b53dbb02785a1b2004cb22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505240"
---
# <span data-ttu-id="a85ae-101">Set-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a85ae-101">Set-AzureBatchJob</span></span>

## <span data-ttu-id="a85ae-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a85ae-102">SYNOPSIS</span></span>
<span data-ttu-id="a85ae-103">Kötegelt feladatot frissít.</span><span class="sxs-lookup"><span data-stu-id="a85ae-103">Updates a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a85ae-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a85ae-104">SYNTAX</span></span>

```
Set-AzureBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a85ae-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a85ae-105">DESCRIPTION</span></span>
<span data-ttu-id="a85ae-106">A **set-AzureBatchJob** parancsmag egy Azure-köteg-feladatot frissít.</span><span class="sxs-lookup"><span data-stu-id="a85ae-106">The **Set-AzureBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="a85ae-107">A Get-AzureBatchJob parancsmaggal **PSCloudJob** objektumot hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="a85ae-107">Use the Get-AzureBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="a85ae-108">Módosítsa az objektum tulajdonságait, majd az aktuális parancsmag segítségével végezze el a módosításokat a köteg szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="a85ae-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="a85ae-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a85ae-109">EXAMPLES</span></span>

### <span data-ttu-id="a85ae-110">Példa 1: feladat frissítése</span><span class="sxs-lookup"><span data-stu-id="a85ae-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzureBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzureBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="a85ae-111">Az első parancs beolvassa a készletet a **Get-AzureBatchJob** függvénnyel, majd a $Job változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a85ae-111">The first command gets a pool by using **Get-AzureBatchJob** , and then stores it in the $Job variable.</span></span>

<span data-ttu-id="a85ae-112">A második parancs módosítja a $Job objektum prioritási specifikációját.</span><span class="sxs-lookup"><span data-stu-id="a85ae-112">The second command modifies the priority specification on the $Job object.</span></span>

<span data-ttu-id="a85ae-113">A végleges parancs frissíti a kötegfájlt a $Job helyi objektumának megfelelően.</span><span class="sxs-lookup"><span data-stu-id="a85ae-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="a85ae-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a85ae-114">PARAMETERS</span></span>

### <span data-ttu-id="a85ae-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a85ae-115">-BatchContext</span></span>
<span data-ttu-id="a85ae-116">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="a85ae-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a85ae-117">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a85ae-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="a85ae-118">-Job</span><span class="sxs-lookup"><span data-stu-id="a85ae-118">-Job</span></span>
<span data-ttu-id="a85ae-119">Itt adhatja meg azt a **PSCloudJob** , amelyre a parancsmag frissíti a köteg szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="a85ae-119">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a85ae-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a85ae-120">-DefaultProfile</span></span>
<span data-ttu-id="a85ae-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a85ae-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a85ae-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a85ae-122">CommonParameters</span></span>
<span data-ttu-id="a85ae-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a85ae-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a85ae-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a85ae-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a85ae-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a85ae-125">INPUTS</span></span>

### <span data-ttu-id="a85ae-126">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a85ae-126">BatchAccountContext</span></span>
<span data-ttu-id="a85ae-127">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="a85ae-127">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="a85ae-128">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="a85ae-128">PSCloudJob</span></span>
<span data-ttu-id="a85ae-129">A ' Job ' paraméter elfogadja a "PSCloudJob" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="a85ae-129">Parameter 'Job' accepts value of type 'PSCloudJob' from the pipeline</span></span>

## <span data-ttu-id="a85ae-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a85ae-130">OUTPUTS</span></span>

## <span data-ttu-id="a85ae-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a85ae-131">NOTES</span></span>

## <span data-ttu-id="a85ae-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a85ae-132">RELATED LINKS</span></span>

[<span data-ttu-id="a85ae-133">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a85ae-133">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="a85ae-134">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a85ae-134">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="a85ae-135">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a85ae-135">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="a85ae-136">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a85ae-136">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="a85ae-137">Új – AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a85ae-137">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="a85ae-138">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a85ae-138">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="a85ae-139">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a85ae-139">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="a85ae-140">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a85ae-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


