---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
ms.openlocfilehash: 94c4fe3292e07045382e432377111d0849db2668
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93847825"
---
# <span data-ttu-id="fc199-101">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="fc199-101">Stop-AzBatchJobSchedule</span></span>

## <span data-ttu-id="fc199-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fc199-102">SYNOPSIS</span></span>
<span data-ttu-id="fc199-103">Befejezi a kötegelt feladatok ütemezését.</span><span class="sxs-lookup"><span data-stu-id="fc199-103">Stops a Batch job schedule.</span></span>

## <span data-ttu-id="fc199-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fc199-104">SYNTAX</span></span>

```
Stop-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc199-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fc199-105">DESCRIPTION</span></span>
<span data-ttu-id="fc199-106">A **stop-AzBatchJobSchedule** parancsmag az Azure kötegelt feladatok ütemtervét leállítja.</span><span class="sxs-lookup"><span data-stu-id="fc199-106">The **Stop-AzBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="fc199-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fc199-107">EXAMPLES</span></span>

### <span data-ttu-id="fc199-108">1. példa: munkabeosztás leállítása</span><span class="sxs-lookup"><span data-stu-id="fc199-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="fc199-109">Ez a parancs leállítja a JobSchedule17 AZONOSÍTÓJÚ munkabeosztást.</span><span class="sxs-lookup"><span data-stu-id="fc199-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="fc199-110">A Get-AzBatchAccountKeys parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="fc199-110">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="fc199-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fc199-111">PARAMETERS</span></span>

### <span data-ttu-id="fc199-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="fc199-112">-BatchContext</span></span>
<span data-ttu-id="fc199-113">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="fc199-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="fc199-114">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="fc199-114">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="fc199-115">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="fc199-115">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="fc199-116">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="fc199-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="fc199-117">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="fc199-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="fc199-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc199-118">-DefaultProfile</span></span>
<span data-ttu-id="fc199-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fc199-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc199-120">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="fc199-120">-Id</span></span>
<span data-ttu-id="fc199-121">Annak a munkaütemezésnek az AZONOSÍTÓját adja meg, amelyre a parancsmag leáll.</span><span class="sxs-lookup"><span data-stu-id="fc199-121">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

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

### <span data-ttu-id="fc199-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc199-122">CommonParameters</span></span>
<span data-ttu-id="fc199-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fc199-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc199-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc199-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc199-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc199-125">INPUTS</span></span>

### <span data-ttu-id="fc199-126">System. String</span><span class="sxs-lookup"><span data-stu-id="fc199-126">System.String</span></span>

### <span data-ttu-id="fc199-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="fc199-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="fc199-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc199-128">OUTPUTS</span></span>

### <span data-ttu-id="fc199-129">System. Void</span><span class="sxs-lookup"><span data-stu-id="fc199-129">System.Void</span></span>

## <span data-ttu-id="fc199-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fc199-130">NOTES</span></span>

## <span data-ttu-id="fc199-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc199-131">RELATED LINKS</span></span>

[<span data-ttu-id="fc199-132">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="fc199-132">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="fc199-133">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="fc199-133">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="fc199-134">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="fc199-134">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="fc199-135">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="fc199-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="fc199-136">Új – AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="fc199-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="fc199-137">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="fc199-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="fc199-138">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="fc199-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


