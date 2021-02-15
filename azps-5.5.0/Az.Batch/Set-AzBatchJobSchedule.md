---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
ms.openlocfilehash: d6a17588b5718f9a6d735521a7a136cba472ead0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166754"
---
# <span data-ttu-id="a64d3-101">Set-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a64d3-101">Set-AzBatchJobSchedule</span></span>

## <span data-ttu-id="a64d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a64d3-102">SYNOPSIS</span></span>
<span data-ttu-id="a64d3-103">Munkabeosztást állít be.</span><span class="sxs-lookup"><span data-stu-id="a64d3-103">Sets a job schedule.</span></span>

## <span data-ttu-id="a64d3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a64d3-104">SYNTAX</span></span>

```
Set-AzBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a64d3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a64d3-105">DESCRIPTION</span></span>
<span data-ttu-id="a64d3-106">A **Set-AzBatchSchedule** parancsmag feladatütemtervet állít be az Azure Batch szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="a64d3-106">The **Set-AzBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="a64d3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a64d3-107">EXAMPLES</span></span>

### <span data-ttu-id="a64d3-108">1. példa: Beosztás frissítése</span><span class="sxs-lookup"><span data-stu-id="a64d3-108">Example 1: Update a job schedule</span></span>
```
PS C:\> $JobSchedule = Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
PS C:\> $JobSchedule.Schedule.RecurrenceInterval = New-TimeSpan -Days 2
PS C:\> Set-AzBatchJobSchedule -JobSchedule $Job -BatchContext $Context
```

<span data-ttu-id="a64d3-109">Az első parancs a **Get-AzBatch JobSchedule** használatával kap feladatot, majd azt a $JobSchedule tárolja.</span><span class="sxs-lookup"><span data-stu-id="a64d3-109">The first command gets a job by using **Get-AzBatchJobSchedule**, and then stores it in the $JobSchedule variable.</span></span>
<span data-ttu-id="a64d3-110">A második parancs módosítja az objektum ismétlődési `$JobSchedule.Schedule` időközét.</span><span class="sxs-lookup"><span data-stu-id="a64d3-110">The second command modifies the recurrence interval on the `$JobSchedule.Schedule` object.</span></span>
<span data-ttu-id="a64d3-111">Az utolsó parancs frissíti a Batch szolgáltatást úgy, hogy megfeleljen a helyi objektumnak a $JobSchedule.</span><span class="sxs-lookup"><span data-stu-id="a64d3-111">The final command updates the Batch service to match the local object in $JobSchedule.</span></span>

## <span data-ttu-id="a64d3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a64d3-112">PARAMETERS</span></span>

### <span data-ttu-id="a64d3-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a64d3-113">-BatchContext</span></span>
<span data-ttu-id="a64d3-114">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="a64d3-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a64d3-115">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="a64d3-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a64d3-116">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse le a BatchAccountContext objektumot, és töltse ki a hozzáférési kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="a64d3-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a64d3-117">Megosztott kulcsú hitelesítés használata esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="a64d3-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a64d3-118">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="a64d3-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a64d3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a64d3-119">-DefaultProfile</span></span>
<span data-ttu-id="a64d3-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a64d3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a64d3-121">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="a64d3-121">-JobSchedule</span></span>
<span data-ttu-id="a64d3-122">Egy **munkabeosztást képviselő PSCloudSchedule-objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="a64d3-122">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="a64d3-123">**PSCloudSchedule-objektum** beszerzéséhez használja a Get-AzBatchJobSchedule parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a64d3-123">To obtain a **PSCloudJobSchedule** object, use the Get-AzBatchJobSchedule cmdlet.</span></span>

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

### <span data-ttu-id="a64d3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a64d3-124">CommonParameters</span></span>
<span data-ttu-id="a64d3-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a64d3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a64d3-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a64d3-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a64d3-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a64d3-127">INPUTS</span></span>

### <span data-ttu-id="a64d3-128">Microsoft.Azure.Commands.Bat. Models.PSCloudSchedule</span><span class="sxs-lookup"><span data-stu-id="a64d3-128">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

### <span data-ttu-id="a64d3-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a64d3-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a64d3-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a64d3-130">OUTPUTS</span></span>

### <span data-ttu-id="a64d3-131">System.Void</span><span class="sxs-lookup"><span data-stu-id="a64d3-131">System.Void</span></span>

## <span data-ttu-id="a64d3-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a64d3-132">NOTES</span></span>

## <span data-ttu-id="a64d3-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a64d3-133">RELATED LINKS</span></span>

[<span data-ttu-id="a64d3-134">Disable-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a64d3-134">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="a64d3-135">Enable-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a64d3-135">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="a64d3-136">Get-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a64d3-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="a64d3-137">New-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a64d3-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="a64d3-138">Remove-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a64d3-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="a64d3-139">Stop-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a64d3-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)


