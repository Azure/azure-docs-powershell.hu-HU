---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
ms.openlocfilehash: 59afa8f2ad5b1cf8739bece249d63574c8db6e4c
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93671909"
---
# <span data-ttu-id="cedb9-101">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cedb9-101">Disable-AzBatchJobSchedule</span></span>

## <span data-ttu-id="cedb9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cedb9-102">SYNOPSIS</span></span>
<span data-ttu-id="cedb9-103">Letilt egy kötegelt feladatok ütemezését.</span><span class="sxs-lookup"><span data-stu-id="cedb9-103">Disables a Batch job schedule.</span></span>

## <span data-ttu-id="cedb9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cedb9-104">SYNTAX</span></span>

```
Disable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cedb9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cedb9-105">DESCRIPTION</span></span>
<span data-ttu-id="cedb9-106">A **disable-AzBatchJobSchedule** parancsmag letiltja az Azure-alapú kötegelt feladatok ütemezését.</span><span class="sxs-lookup"><span data-stu-id="cedb9-106">The **Disable-AzBatchJobSchedule** cmdlet disables an Azure Batch job schedule.</span></span>
<span data-ttu-id="cedb9-107">Ha letiltja az ütemtervet, a feladatok nem az adott ütemterv szerint jönnek létre.</span><span class="sxs-lookup"><span data-stu-id="cedb9-107">If you disable a schedule, jobs are not created according to that schedule.</span></span>
<span data-ttu-id="cedb9-108">Később is engedélyezheti a letiltott ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="cedb9-108">You can enable a disabled schedule later.</span></span>

## <span data-ttu-id="cedb9-109">Példák</span><span class="sxs-lookup"><span data-stu-id="cedb9-109">EXAMPLES</span></span>

### <span data-ttu-id="cedb9-110">1. példa: munkabeosztás letiltása</span><span class="sxs-lookup"><span data-stu-id="cedb9-110">Example 1: Disable a job schedule</span></span>
```
PS C:\>Disable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="cedb9-111">Ez a parancs letiltja a JobSchedule17 azonosító munkabeosztást.</span><span class="sxs-lookup"><span data-stu-id="cedb9-111">This command disables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="cedb9-112">A **Get-AzBatchAccountKeys** parancsmaggal rendelhet környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="cedb9-112">Use the **Get-AzBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="cedb9-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cedb9-113">PARAMETERS</span></span>

### <span data-ttu-id="cedb9-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="cedb9-114">-BatchContext</span></span>
<span data-ttu-id="cedb9-115">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="cedb9-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="cedb9-116">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="cedb9-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="cedb9-117">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="cedb9-117">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="cedb9-118">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="cedb9-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="cedb9-119">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="cedb9-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="cedb9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cedb9-120">-DefaultProfile</span></span>
<span data-ttu-id="cedb9-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cedb9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cedb9-122">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="cedb9-122">-Id</span></span>
<span data-ttu-id="cedb9-123">Annak az ütemezésnek az AZONOSÍTÓját adja meg, amelyre a parancsmag letiltja.</span><span class="sxs-lookup"><span data-stu-id="cedb9-123">Specifies the ID of the job schedule that this cmdlet disables.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cedb9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cedb9-124">CommonParameters</span></span>
<span data-ttu-id="cedb9-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cedb9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cedb9-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cedb9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cedb9-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cedb9-127">INPUTS</span></span>

### <span data-ttu-id="cedb9-128">System. String</span><span class="sxs-lookup"><span data-stu-id="cedb9-128">System.String</span></span>

### <span data-ttu-id="cedb9-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="cedb9-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="cedb9-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cedb9-130">OUTPUTS</span></span>

### <span data-ttu-id="cedb9-131">System. Void</span><span class="sxs-lookup"><span data-stu-id="cedb9-131">System.Void</span></span>

## <span data-ttu-id="cedb9-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cedb9-132">NOTES</span></span>

## <span data-ttu-id="cedb9-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cedb9-133">RELATED LINKS</span></span>

[<span data-ttu-id="cedb9-134">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cedb9-134">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="cedb9-135">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="cedb9-135">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="cedb9-136">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cedb9-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="cedb9-137">Új – AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cedb9-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="cedb9-138">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cedb9-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="cedb9-139">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cedb9-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="cedb9-140">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="cedb9-140">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


