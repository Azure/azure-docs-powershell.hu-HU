---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJobSchedule.md
ms.openlocfilehash: 2f1660a2273482b57e9bb6a39bb3d21a8433bce6
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93671903"
---
# <span data-ttu-id="20b37-101">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="20b37-101">Enable-AzBatchJobSchedule</span></span>

## <span data-ttu-id="20b37-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="20b37-102">SYNOPSIS</span></span>
<span data-ttu-id="20b37-103">Lehetővé teszi a kötegelt feladatok ütemezését.</span><span class="sxs-lookup"><span data-stu-id="20b37-103">Enables a Batch job schedule.</span></span>

## <span data-ttu-id="20b37-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="20b37-104">SYNTAX</span></span>

```
Enable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20b37-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="20b37-105">DESCRIPTION</span></span>
<span data-ttu-id="20b37-106">Az **enable-AzBatchJobSchedule** parancsmag az Azure kötegelt feladatok ütemtervét engedélyezi.</span><span class="sxs-lookup"><span data-stu-id="20b37-106">The **Enable-AzBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="20b37-107">Miután engedélyezte a projekt ütemezését, a munkahelyeket az adott ütemterv szerint hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="20b37-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="20b37-108">Példák</span><span class="sxs-lookup"><span data-stu-id="20b37-108">EXAMPLES</span></span>

### <span data-ttu-id="20b37-109">1. példa: projekt-ütemezés engedélyezése</span><span class="sxs-lookup"><span data-stu-id="20b37-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="20b37-110">Ez a parancs engedélyezi az ID JobSchedule17 tartalmazó ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="20b37-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="20b37-111">A **Get-AzBatchAccountKeys** parancsmaggal rendelhet környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="20b37-111">Use the **Get-AzBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="20b37-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="20b37-112">PARAMETERS</span></span>

### <span data-ttu-id="20b37-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="20b37-113">-BatchContext</span></span>
<span data-ttu-id="20b37-114">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="20b37-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="20b37-115">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="20b37-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="20b37-116">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="20b37-116">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="20b37-117">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="20b37-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="20b37-118">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="20b37-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="20b37-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20b37-119">-DefaultProfile</span></span>
<span data-ttu-id="20b37-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="20b37-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20b37-121">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="20b37-121">-Id</span></span>
<span data-ttu-id="20b37-122">Annak az ütemezésnek az AZONOSÍTÓját adja meg, amelyre a parancsmag engedélyezi.</span><span class="sxs-lookup"><span data-stu-id="20b37-122">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

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

### <span data-ttu-id="20b37-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20b37-123">CommonParameters</span></span>
<span data-ttu-id="20b37-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="20b37-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20b37-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20b37-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20b37-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="20b37-126">INPUTS</span></span>

### <span data-ttu-id="20b37-127">System. String</span><span class="sxs-lookup"><span data-stu-id="20b37-127">System.String</span></span>

### <span data-ttu-id="20b37-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="20b37-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="20b37-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="20b37-129">OUTPUTS</span></span>

### <span data-ttu-id="20b37-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="20b37-130">System.Void</span></span>

## <span data-ttu-id="20b37-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="20b37-131">NOTES</span></span>

## <span data-ttu-id="20b37-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="20b37-132">RELATED LINKS</span></span>

[<span data-ttu-id="20b37-133">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="20b37-133">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="20b37-134">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="20b37-134">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="20b37-135">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="20b37-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="20b37-136">Új – AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="20b37-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="20b37-137">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="20b37-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="20b37-138">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="20b37-138">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="20b37-139">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="20b37-139">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


