---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
ms.openlocfilehash: 608d4aaba26b6f9631d4f1c35e889ac5a7480154
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93671905"
---
# <span data-ttu-id="48536-101">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="48536-101">Enable-AzBatchJob</span></span>

## <span data-ttu-id="48536-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="48536-102">SYNOPSIS</span></span>
<span data-ttu-id="48536-103">Lehetővé teszi a kötegelt feladatok végrehajtását.</span><span class="sxs-lookup"><span data-stu-id="48536-103">Enables a Batch job.</span></span>

## <span data-ttu-id="48536-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="48536-104">SYNTAX</span></span>

```
Enable-AzBatchJob [-Id] <String> -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="48536-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="48536-105">DESCRIPTION</span></span>
<span data-ttu-id="48536-106">Az **enable-AzBatchJob** parancsmag lehetővé teszi az Azure-alapú kötegelt feladatok végrehajtását.</span><span class="sxs-lookup"><span data-stu-id="48536-106">The **Enable-AzBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="48536-107">Miután engedélyezte a feladatot, az új feladatok futhatnak.</span><span class="sxs-lookup"><span data-stu-id="48536-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="48536-108">Példák</span><span class="sxs-lookup"><span data-stu-id="48536-108">EXAMPLES</span></span>

### <span data-ttu-id="48536-109">1. példa: kötegelt feladat engedélyezése</span><span class="sxs-lookup"><span data-stu-id="48536-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="48536-110">Ez a parancs lehetővé teszi, hogy a 000001 AZONOSÍTÓJÚ feladat.</span><span class="sxs-lookup"><span data-stu-id="48536-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="48536-111">A Get-AzBatchAccountKeys parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="48536-111">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="48536-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="48536-112">PARAMETERS</span></span>

### <span data-ttu-id="48536-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="48536-113">-BatchContext</span></span>
<span data-ttu-id="48536-114">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="48536-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="48536-115">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="48536-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="48536-116">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="48536-116">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="48536-117">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="48536-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="48536-118">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="48536-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="48536-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48536-119">-DefaultProfile</span></span>
<span data-ttu-id="48536-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="48536-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48536-121">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="48536-121">-Id</span></span>
<span data-ttu-id="48536-122">Annak a projektnek az AZONOSÍTÓját adja meg, amelyre ez a parancsmag engedélyezi.</span><span class="sxs-lookup"><span data-stu-id="48536-122">Specifies the ID of the job that this cmdlet enables.</span></span>

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

### <span data-ttu-id="48536-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48536-123">CommonParameters</span></span>
<span data-ttu-id="48536-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="48536-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48536-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48536-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48536-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="48536-126">INPUTS</span></span>

### <span data-ttu-id="48536-127">System. String</span><span class="sxs-lookup"><span data-stu-id="48536-127">System.String</span></span>

### <span data-ttu-id="48536-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="48536-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="48536-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="48536-129">OUTPUTS</span></span>

### <span data-ttu-id="48536-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="48536-130">System.Void</span></span>

## <span data-ttu-id="48536-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="48536-131">NOTES</span></span>

## <span data-ttu-id="48536-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="48536-132">RELATED LINKS</span></span>

[<span data-ttu-id="48536-133">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="48536-133">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="48536-134">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="48536-134">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="48536-135">Új – AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="48536-135">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="48536-136">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="48536-136">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="48536-137">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="48536-137">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="48536-138">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="48536-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


