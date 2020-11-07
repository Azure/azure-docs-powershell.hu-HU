---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
ms.openlocfilehash: 91ac0d6202eb02f724f3ea17e57846e6db6b7412
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667683"
---
# <span data-ttu-id="35a34-101">Set-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="35a34-101">Set-AzBatchJobSchedule</span></span>

## <span data-ttu-id="35a34-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="35a34-102">SYNOPSIS</span></span>
<span data-ttu-id="35a34-103">Ütemtervet állít be.</span><span class="sxs-lookup"><span data-stu-id="35a34-103">Sets a job schedule.</span></span>

## <span data-ttu-id="35a34-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="35a34-104">SYNTAX</span></span>

```
Set-AzBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35a34-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="35a34-105">DESCRIPTION</span></span>
<span data-ttu-id="35a34-106">A **set-AzBatchJobSchedule** parancsmag az Azure kötegelt szolgáltatásban végez ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="35a34-106">The **Set-AzBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="35a34-107">Példák</span><span class="sxs-lookup"><span data-stu-id="35a34-107">EXAMPLES</span></span>

### <span data-ttu-id="35a34-108">Példa 1: projekt ütemtervének frissítése</span><span class="sxs-lookup"><span data-stu-id="35a34-108">Example 1: Update a job schedule</span></span>
```
PS C:\> $JobSchedule = Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
PS C:\> $JobSchedule.Schedule.RecurrenceInterval = New-TimeSpan -Days 2
PS C:\> Set-AzBatchJobSchedule -JobSchedule $Job -BatchContext $Context
```

<span data-ttu-id="35a34-109">Az első parancs a **Get-AzBatchJobSchedule** használatával kap munkát, majd a $JobSchedule változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="35a34-109">The first command gets a job by using **Get-AzBatchJobSchedule** , and then stores it in the $JobSchedule variable.</span></span>
<span data-ttu-id="35a34-110">A második parancs módosítja az objektum ismétlődési intervallumát `$JobSchedule.Schedule` .</span><span class="sxs-lookup"><span data-stu-id="35a34-110">The second command modifies the recurrence interval on the `$JobSchedule.Schedule` object.</span></span>
<span data-ttu-id="35a34-111">A végleges parancs frissíti a kötegfájlt a $JobSchedule helyi objektumának megfelelően.</span><span class="sxs-lookup"><span data-stu-id="35a34-111">The final command updates the Batch service to match the local object in $JobSchedule.</span></span>

## <span data-ttu-id="35a34-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="35a34-112">PARAMETERS</span></span>

### <span data-ttu-id="35a34-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="35a34-113">-BatchContext</span></span>
<span data-ttu-id="35a34-114">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="35a34-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="35a34-115">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="35a34-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="35a34-116">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="35a34-116">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="35a34-117">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="35a34-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="35a34-118">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="35a34-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="35a34-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35a34-119">-DefaultProfile</span></span>
<span data-ttu-id="35a34-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="35a34-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35a34-121">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="35a34-121">-JobSchedule</span></span>
<span data-ttu-id="35a34-122">Olyan **PSCloudJobSchedule** -objektumot ad meg, amely egy projekt ütemtervét képviseli.</span><span class="sxs-lookup"><span data-stu-id="35a34-122">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="35a34-123">**PSCloudJobSchedule** objektum beolvasásához használja az Get-AzBatchJobSchedule parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="35a34-123">To obtain a **PSCloudJobSchedule** object, use the Get-AzBatchJobSchedule cmdlet.</span></span>

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

### <span data-ttu-id="35a34-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35a34-124">CommonParameters</span></span>
<span data-ttu-id="35a34-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="35a34-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35a34-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35a34-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35a34-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="35a34-127">INPUTS</span></span>

### <span data-ttu-id="35a34-128">Microsoft.Azure.Commands.BatCH. Modellek. PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="35a34-128">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

### <span data-ttu-id="35a34-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="35a34-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="35a34-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="35a34-130">OUTPUTS</span></span>

### <span data-ttu-id="35a34-131">System. Void</span><span class="sxs-lookup"><span data-stu-id="35a34-131">System.Void</span></span>

## <span data-ttu-id="35a34-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="35a34-132">NOTES</span></span>

## <span data-ttu-id="35a34-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="35a34-133">RELATED LINKS</span></span>

[<span data-ttu-id="35a34-134">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="35a34-134">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="35a34-135">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="35a34-135">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="35a34-136">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="35a34-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="35a34-137">Új – AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="35a34-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="35a34-138">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="35a34-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="35a34-139">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="35a34-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)


