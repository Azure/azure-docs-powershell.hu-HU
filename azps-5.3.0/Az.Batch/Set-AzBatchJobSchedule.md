---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
ms.openlocfilehash: d6a17588b5718f9a6d735521a7a136cba472ead0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478189"
---
# <span data-ttu-id="28ba0-101">Set-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="28ba0-101">Set-AzBatchJobSchedule</span></span>

## <span data-ttu-id="28ba0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28ba0-102">SYNOPSIS</span></span>
<span data-ttu-id="28ba0-103">Munkabeosztást állít be.</span><span class="sxs-lookup"><span data-stu-id="28ba0-103">Sets a job schedule.</span></span>

## <span data-ttu-id="28ba0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="28ba0-104">SYNTAX</span></span>

```
Set-AzBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28ba0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="28ba0-105">DESCRIPTION</span></span>
<span data-ttu-id="28ba0-106">A **Set-AzBatch JobSchedule** parancsmag feladatütemtervet állít be az Azure Batch szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="28ba0-106">The **Set-AzBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="28ba0-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="28ba0-107">EXAMPLES</span></span>

### <span data-ttu-id="28ba0-108">1. példa: Beosztás frissítése</span><span class="sxs-lookup"><span data-stu-id="28ba0-108">Example 1: Update a job schedule</span></span>
```
PS C:\> $JobSchedule = Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
PS C:\> $JobSchedule.Schedule.RecurrenceInterval = New-TimeSpan -Days 2
PS C:\> Set-AzBatchJobSchedule -JobSchedule $Job -BatchContext $Context
```

<span data-ttu-id="28ba0-109">Az első parancs a **Get-AzBatch JobSchedule** használatával kap feladatot, majd azt a $JobSchedule tárolja.</span><span class="sxs-lookup"><span data-stu-id="28ba0-109">The first command gets a job by using **Get-AzBatchJobSchedule**, and then stores it in the $JobSchedule variable.</span></span>
<span data-ttu-id="28ba0-110">A második parancs módosítja az objektum ismétlődési `$JobSchedule.Schedule` időközét.</span><span class="sxs-lookup"><span data-stu-id="28ba0-110">The second command modifies the recurrence interval on the `$JobSchedule.Schedule` object.</span></span>
<span data-ttu-id="28ba0-111">Az utolsó parancs frissíti a Batch szolgáltatást úgy, hogy megfeleljen a helyi objektumnak a $JobSchedule.</span><span class="sxs-lookup"><span data-stu-id="28ba0-111">The final command updates the Batch service to match the local object in $JobSchedule.</span></span>

## <span data-ttu-id="28ba0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28ba0-112">PARAMETERS</span></span>

### <span data-ttu-id="28ba0-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="28ba0-113">-BatchContext</span></span>
<span data-ttu-id="28ba0-114">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="28ba0-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="28ba0-115">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="28ba0-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="28ba0-116">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse ki a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="28ba0-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="28ba0-117">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="28ba0-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="28ba0-118">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="28ba0-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="28ba0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28ba0-119">-DefaultProfile</span></span>
<span data-ttu-id="28ba0-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="28ba0-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28ba0-121">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="28ba0-121">-JobSchedule</span></span>
<span data-ttu-id="28ba0-122">Egy **munkabeosztást képviselő PSCloudSchedule** objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="28ba0-122">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="28ba0-123">**PSCloudSchedule-objektum** beszerzéséhez használja a Get-AzBatchJobSchedule parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="28ba0-123">To obtain a **PSCloudJobSchedule** object, use the Get-AzBatchJobSchedule cmdlet.</span></span>

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

### <span data-ttu-id="28ba0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28ba0-124">CommonParameters</span></span>
<span data-ttu-id="28ba0-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28ba0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28ba0-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="28ba0-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28ba0-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="28ba0-127">INPUTS</span></span>

### <span data-ttu-id="28ba0-128">Microsoft.Azure.Commands.Bat. Models.PSCloudSchedule</span><span class="sxs-lookup"><span data-stu-id="28ba0-128">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

### <span data-ttu-id="28ba0-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="28ba0-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="28ba0-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="28ba0-130">OUTPUTS</span></span>

### <span data-ttu-id="28ba0-131">System.Void</span><span class="sxs-lookup"><span data-stu-id="28ba0-131">System.Void</span></span>

## <span data-ttu-id="28ba0-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="28ba0-132">NOTES</span></span>

## <span data-ttu-id="28ba0-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="28ba0-133">RELATED LINKS</span></span>

[<span data-ttu-id="28ba0-134">Disable-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="28ba0-134">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="28ba0-135">Enable-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="28ba0-135">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="28ba0-136">Get-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="28ba0-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="28ba0-137">New-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="28ba0-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="28ba0-138">Remove-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="28ba0-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="28ba0-139">Stop-AzBatchSchedule</span><span class="sxs-lookup"><span data-stu-id="28ba0-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)


