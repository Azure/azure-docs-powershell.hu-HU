---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 23893EAE-47F3-45AA-AEB2-354FB8316C25
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
ms.openlocfilehash: 7ab0d9f64b14f6fbdd572f69ecb081114d78891d
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93847969"
---
# <span data-ttu-id="9f777-101">Set-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="9f777-101">Set-AzBatchPool</span></span>

## <span data-ttu-id="9f777-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9f777-102">SYNOPSIS</span></span>
<span data-ttu-id="9f777-103">Frissíti a készlet tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="9f777-103">Updates the properties of a pool.</span></span>

## <span data-ttu-id="9f777-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9f777-104">SYNTAX</span></span>

```
Set-AzBatchPool [-Pool] <PSCloudPool> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f777-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9f777-105">DESCRIPTION</span></span>
<span data-ttu-id="9f777-106">A **set-AzBatchPool** parancsmag az Azure-köteg szolgáltatásban lévő készlet tulajdonságait frissíti.</span><span class="sxs-lookup"><span data-stu-id="9f777-106">The **Set-AzBatchPool** cmdlet updates the properties of a pool in the Azure Batch service.</span></span>
<span data-ttu-id="9f777-107">A Get-AzBatchPool parancsmaggal **PSCloudPool** objektumot hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="9f777-107">Use the Get-AzBatchPool cmdlet to get a **PSCloudPool** object.</span></span>
<span data-ttu-id="9f777-108">Módosítsa az objektum tulajdonságait, majd az aktuális parancsmag segítségével végezze el a módosításokat a köteg szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="9f777-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="9f777-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9f777-109">EXAMPLES</span></span>

### <span data-ttu-id="9f777-110">Példa 1: a készlet frissítése</span><span class="sxs-lookup"><span data-stu-id="9f777-110">Example 1: Update a pool</span></span>
```
PS C:\>$Pool = Get-AzBatchPool "ContosoPool" -BatchContext $Context
PS C:\> $StartTask = New-Object Microsoft.Azure.Commands.Batch.Models.PSStartTask
PS C:\> $StartTask.CommandLine = "cmd /c echo example"
PS C:\> $Pool.StartTask = $StartTask
PS C:\> Set-AzBatchPool -Pool $Pool -BatchContext $Context
```

<span data-ttu-id="9f777-111">Az első parancs beolvassa a készletet a **Get-AzBatchPool** függvénnyel, majd a $Pool változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="9f777-111">The first command gets a pool by using **Get-AzBatchPool** , and then stores it in the $Pool variable.</span></span>
<span data-ttu-id="9f777-112">A következő három parancs a $Pool objektum kezdési tevékenységének specifikációját módosítja.</span><span class="sxs-lookup"><span data-stu-id="9f777-112">The next three commands modify the start task specification on the $Pool object.</span></span>
<span data-ttu-id="9f777-113">A végleges parancs frissíti a kötegfájlt a $Pool helyi objektumának megfelelően.</span><span class="sxs-lookup"><span data-stu-id="9f777-113">The final command updates the Batch service to match the local object in $Pool.</span></span>

## <span data-ttu-id="9f777-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9f777-114">PARAMETERS</span></span>

### <span data-ttu-id="9f777-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="9f777-115">-BatchContext</span></span>
<span data-ttu-id="9f777-116">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="9f777-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9f777-117">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="9f777-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="9f777-118">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="9f777-118">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="9f777-119">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="9f777-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="9f777-120">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="9f777-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="9f777-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f777-121">-DefaultProfile</span></span>
<span data-ttu-id="9f777-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9f777-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f777-123">-Pool (Pool)</span><span class="sxs-lookup"><span data-stu-id="9f777-123">-Pool</span></span>
<span data-ttu-id="9f777-124">Azt a **PSCloudPool** adja meg, amelyre a parancsmag frissíti a köteg szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="9f777-124">Specifies the **PSCloudPool** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="9f777-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f777-125">CommonParameters</span></span>
<span data-ttu-id="9f777-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9f777-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f777-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f777-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f777-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f777-128">INPUTS</span></span>

### <span data-ttu-id="9f777-129">Microsoft.Azure.Commands.BatCH. Modellek. PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="9f777-129">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="9f777-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9f777-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="9f777-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f777-131">OUTPUTS</span></span>

### <span data-ttu-id="9f777-132">System. Void</span><span class="sxs-lookup"><span data-stu-id="9f777-132">System.Void</span></span>

## <span data-ttu-id="9f777-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9f777-133">NOTES</span></span>

## <span data-ttu-id="9f777-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9f777-134">RELATED LINKS</span></span>

[<span data-ttu-id="9f777-135">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="9f777-135">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="9f777-136">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="9f777-136">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="9f777-137">Új – AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="9f777-137">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="9f777-138">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="9f777-138">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="9f777-139">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="9f777-139">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)

