---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
ms.openlocfilehash: f874432bc26ae2a579a54e4068c719b236ad4c45
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017908"
---
# <span data-ttu-id="17d8f-101">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="17d8f-101">Disable-AzBatchJobSchedule</span></span>

## <span data-ttu-id="17d8f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="17d8f-102">SYNOPSIS</span></span>
<span data-ttu-id="17d8f-103">Letilt egy kötegelt feladatok ütemezését.</span><span class="sxs-lookup"><span data-stu-id="17d8f-103">Disables a Batch job schedule.</span></span>

## <span data-ttu-id="17d8f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="17d8f-104">SYNTAX</span></span>

```
Disable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17d8f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="17d8f-105">DESCRIPTION</span></span>
<span data-ttu-id="17d8f-106">A **disable-AzBatchJobSchedule** parancsmag letiltja az Azure-alapú kötegelt feladatok ütemezését.</span><span class="sxs-lookup"><span data-stu-id="17d8f-106">The **Disable-AzBatchJobSchedule** cmdlet disables an Azure Batch job schedule.</span></span>
<span data-ttu-id="17d8f-107">Ha letiltja az ütemtervet, a feladatok nem az adott ütemterv szerint jönnek létre.</span><span class="sxs-lookup"><span data-stu-id="17d8f-107">If you disable a schedule, jobs are not created according to that schedule.</span></span>
<span data-ttu-id="17d8f-108">Később is engedélyezheti a letiltott ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="17d8f-108">You can enable a disabled schedule later.</span></span>

## <span data-ttu-id="17d8f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="17d8f-109">EXAMPLES</span></span>

### <span data-ttu-id="17d8f-110">1. példa: munkabeosztás letiltása</span><span class="sxs-lookup"><span data-stu-id="17d8f-110">Example 1: Disable a job schedule</span></span>
```
PS C:\>Disable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="17d8f-111">Ez a parancs letiltja a JobSchedule17 azonosító munkabeosztást.</span><span class="sxs-lookup"><span data-stu-id="17d8f-111">This command disables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="17d8f-112">A **Get-AzBatchAccountKey** parancsmaggal rendelhet környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="17d8f-112">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="17d8f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="17d8f-113">PARAMETERS</span></span>

### <span data-ttu-id="17d8f-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="17d8f-114">-BatchContext</span></span>
<span data-ttu-id="17d8f-115">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="17d8f-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="17d8f-116">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="17d8f-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="17d8f-117">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKey parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="17d8f-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="17d8f-118">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="17d8f-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="17d8f-119">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="17d8f-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="17d8f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17d8f-120">-DefaultProfile</span></span>
<span data-ttu-id="17d8f-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="17d8f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17d8f-122">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="17d8f-122">-Id</span></span>
<span data-ttu-id="17d8f-123">Annak az ütemezésnek az AZONOSÍTÓját adja meg, amelyre a parancsmag letiltja.</span><span class="sxs-lookup"><span data-stu-id="17d8f-123">Specifies the ID of the job schedule that this cmdlet disables.</span></span>

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

### <span data-ttu-id="17d8f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17d8f-124">CommonParameters</span></span>
<span data-ttu-id="17d8f-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="17d8f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17d8f-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="17d8f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17d8f-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="17d8f-127">INPUTS</span></span>

### <span data-ttu-id="17d8f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="17d8f-128">System.String</span></span>

### <span data-ttu-id="17d8f-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="17d8f-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="17d8f-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="17d8f-130">OUTPUTS</span></span>

### <span data-ttu-id="17d8f-131">System. Void</span><span class="sxs-lookup"><span data-stu-id="17d8f-131">System.Void</span></span>

## <span data-ttu-id="17d8f-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="17d8f-132">NOTES</span></span>

## <span data-ttu-id="17d8f-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="17d8f-133">RELATED LINKS</span></span>

[<span data-ttu-id="17d8f-134">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="17d8f-134">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="17d8f-135">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="17d8f-135">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="17d8f-136">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="17d8f-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="17d8f-137">Új – AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="17d8f-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="17d8f-138">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="17d8f-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="17d8f-139">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="17d8f-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="17d8f-140">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="17d8f-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
