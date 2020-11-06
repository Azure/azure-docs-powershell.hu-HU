---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 23893EAE-47F3-45AA-AEB2-354FB8316C25
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPool.md
ms.openlocfilehash: c0f1dc4972e3b71dce74bffb7a72e782774a2734
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492005"
---
# <span data-ttu-id="b0b68-101">Set-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="b0b68-101">Set-AzureBatchPool</span></span>

## <span data-ttu-id="b0b68-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b0b68-102">SYNOPSIS</span></span>
<span data-ttu-id="b0b68-103">Frissíti a készlet tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="b0b68-103">Updates the properties of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0b68-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b0b68-104">SYNTAX</span></span>

```
Set-AzureBatchPool [-Pool] <PSCloudPool> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0b68-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b0b68-105">DESCRIPTION</span></span>
<span data-ttu-id="b0b68-106">A **set-AzureBatchPool** parancsmag az Azure-köteg szolgáltatásban lévő készlet tulajdonságait frissíti.</span><span class="sxs-lookup"><span data-stu-id="b0b68-106">The **Set-AzureBatchPool** cmdlet updates the properties of a pool in the Azure Batch service.</span></span>
<span data-ttu-id="b0b68-107">A Get-AzureBatchPool parancsmaggal **PSCloudPool** objektumot hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="b0b68-107">Use the Get-AzureBatchPool cmdlet to get a **PSCloudPool** object.</span></span>
<span data-ttu-id="b0b68-108">Módosítsa az objektum tulajdonságait, majd az aktuális parancsmag segítségével végezze el a módosításokat a köteg szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="b0b68-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="b0b68-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b0b68-109">EXAMPLES</span></span>

### <span data-ttu-id="b0b68-110">Példa 1: a készlet frissítése</span><span class="sxs-lookup"><span data-stu-id="b0b68-110">Example 1: Update a pool</span></span>
```
PS C:\>$Pool = Get-AzureBatchPool "ContosoPool" -BatchContext $Context
PS C:\> $StartTask = New-Object Microsoft.Azure.Commands.Batch.Models.PSStartTask
PS C:\> $StartTask.CommandLine = "cmd /c echo example"
PS C:\> $Pool.StartTask = $StartTask
PS C:\> Set-AzureBatchPool -Pool $Pool -BatchContext $Context
```

<span data-ttu-id="b0b68-111">Az első parancs beolvassa a készletet a **Get-AzureBatchPool** függvénnyel, majd a $Pool változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b0b68-111">The first command gets a pool by using **Get-AzureBatchPool** , and then stores it in the $Pool variable.</span></span>
<span data-ttu-id="b0b68-112">A következő három parancs a $Pool objektum kezdési tevékenységének specifikációját módosítja.</span><span class="sxs-lookup"><span data-stu-id="b0b68-112">The next three commands modify the start task specification on the $Pool object.</span></span>
<span data-ttu-id="b0b68-113">A végleges parancs frissíti a kötegfájlt a $Pool helyi objektumának megfelelően.</span><span class="sxs-lookup"><span data-stu-id="b0b68-113">The final command updates the Batch service to match the local object in $Pool.</span></span>

## <span data-ttu-id="b0b68-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b0b68-114">PARAMETERS</span></span>

### <span data-ttu-id="b0b68-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b0b68-115">-BatchContext</span></span>
<span data-ttu-id="b0b68-116">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="b0b68-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b0b68-117">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="b0b68-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b0b68-118">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="b0b68-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b0b68-119">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="b0b68-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b0b68-120">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="b0b68-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b0b68-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0b68-121">-DefaultProfile</span></span>
<span data-ttu-id="b0b68-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b0b68-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0b68-123">-Pool (Pool)</span><span class="sxs-lookup"><span data-stu-id="b0b68-123">-Pool</span></span>
<span data-ttu-id="b0b68-124">Azt a **PSCloudPool** adja meg, amelyre a parancsmag frissíti a köteg szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="b0b68-124">Specifies the **PSCloudPool** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudPool
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0b68-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0b68-125">CommonParameters</span></span>
<span data-ttu-id="b0b68-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b0b68-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0b68-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0b68-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0b68-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0b68-128">INPUTS</span></span>

### <span data-ttu-id="b0b68-129">Microsoft.Azure.Commands.BatCH. Modellek. PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="b0b68-129">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>
<span data-ttu-id="b0b68-130">Paraméterek: Pool (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b0b68-130">Parameters: Pool (ByValue)</span></span>

### <span data-ttu-id="b0b68-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b0b68-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="b0b68-132">Paraméterek: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b0b68-132">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="b0b68-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0b68-133">OUTPUTS</span></span>

### <span data-ttu-id="b0b68-134">System. Void</span><span class="sxs-lookup"><span data-stu-id="b0b68-134">System.Void</span></span>

## <span data-ttu-id="b0b68-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b0b68-135">NOTES</span></span>

## <span data-ttu-id="b0b68-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b0b68-136">RELATED LINKS</span></span>

[<span data-ttu-id="b0b68-137">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="b0b68-137">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="b0b68-138">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b0b68-138">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="b0b68-139">Új – AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="b0b68-139">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="b0b68-140">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="b0b68-140">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="b0b68-141">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="b0b68-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


