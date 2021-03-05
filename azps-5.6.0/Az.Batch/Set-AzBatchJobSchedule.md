---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: https://docs.microsoft.com/powershell/module/az.batch/set-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
ms.openlocfilehash: cf4512bc0d219c164be6543d5633a43c9052cc4e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004614"
---
# <span data-ttu-id="06908-101">Set-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="06908-101">Set-AzBatchJobSchedule</span></span>

## <span data-ttu-id="06908-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06908-102">SYNOPSIS</span></span>
<span data-ttu-id="06908-103">Munkabeosztást állít be.</span><span class="sxs-lookup"><span data-stu-id="06908-103">Sets a job schedule.</span></span>

## <span data-ttu-id="06908-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="06908-104">SYNTAX</span></span>

```
Set-AzBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06908-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="06908-105">DESCRIPTION</span></span>
<span data-ttu-id="06908-106">A **Set-AzBatch JobSchedule** parancsmag feladatütemtervet állít be az Azure Batch szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="06908-106">The **Set-AzBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="06908-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="06908-107">EXAMPLES</span></span>

### <span data-ttu-id="06908-108">1. példa: Beosztás frissítése</span><span class="sxs-lookup"><span data-stu-id="06908-108">Example 1: Update a job schedule</span></span>
```
PS C:\> $JobSchedule = Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
PS C:\> $JobSchedule.Schedule.RecurrenceInterval = New-TimeSpan -Days 2
PS C:\> Set-AzBatchJobSchedule -JobSchedule $Job -BatchContext $Context
```

<span data-ttu-id="06908-109">Az első parancs a **Get-AzBatch JobSchedule** használatával kap feladatot, majd azt a $JobSchedule tárolja.</span><span class="sxs-lookup"><span data-stu-id="06908-109">The first command gets a job by using **Get-AzBatchJobSchedule**, and then stores it in the $JobSchedule variable.</span></span>
<span data-ttu-id="06908-110">A második parancs módosítja az objektum ismétlődési `$JobSchedule.Schedule` időközét.</span><span class="sxs-lookup"><span data-stu-id="06908-110">The second command modifies the recurrence interval on the `$JobSchedule.Schedule` object.</span></span>
<span data-ttu-id="06908-111">Az utolsó parancs frissíti a Batch szolgáltatást úgy, hogy megfeleljen a helyi objektumnak a $JobSchedule.</span><span class="sxs-lookup"><span data-stu-id="06908-111">The final command updates the Batch service to match the local object in $JobSchedule.</span></span>

## <span data-ttu-id="06908-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06908-112">PARAMETERS</span></span>

### <span data-ttu-id="06908-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="06908-113">-BatchContext</span></span>
<span data-ttu-id="06908-114">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="06908-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="06908-115">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="06908-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="06908-116">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse le a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="06908-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="06908-117">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="06908-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="06908-118">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="06908-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="06908-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06908-119">-DefaultProfile</span></span>
<span data-ttu-id="06908-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="06908-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06908-121">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="06908-121">-JobSchedule</span></span>
<span data-ttu-id="06908-122">Egy **feladatütemtervet képviselő PSCloudSchedule** objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="06908-122">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="06908-123">**PSCloudSchedule-objektum** beszerzéséhez használja a Get-AzBatchJobSchedule parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="06908-123">To obtain a **PSCloudJobSchedule** object, use the Get-AzBatchJobSchedule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06908-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06908-124">CommonParameters</span></span>
<span data-ttu-id="06908-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06908-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06908-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06908-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06908-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="06908-127">INPUTS</span></span>

### <span data-ttu-id="06908-128">Microsoft.Azure.Commands.Bat. Models.PSCloudSchedule</span><span class="sxs-lookup"><span data-stu-id="06908-128">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

### <span data-ttu-id="06908-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="06908-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="06908-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="06908-130">OUTPUTS</span></span>

### <span data-ttu-id="06908-131">System.Void</span><span class="sxs-lookup"><span data-stu-id="06908-131">System.Void</span></span>

## <span data-ttu-id="06908-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="06908-132">NOTES</span></span>

## <span data-ttu-id="06908-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="06908-133">RELATED LINKS</span></span>

[<span data-ttu-id="06908-134">Disable-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="06908-134">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="06908-135">Enable-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="06908-135">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="06908-136">Get-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="06908-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="06908-137">New-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="06908-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="06908-138">Remove-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="06908-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="06908-139">Stop-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="06908-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)


