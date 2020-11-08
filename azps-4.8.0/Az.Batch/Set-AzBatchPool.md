---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 23893EAE-47F3-45AA-AEB2-354FB8316C25
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
ms.openlocfilehash: 423f249a7971883cbe47d8f499fdd780980362f3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024885"
---
# <span data-ttu-id="eb7f7-101">Set-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="eb7f7-101">Set-AzBatchPool</span></span>

## <span data-ttu-id="eb7f7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eb7f7-102">SYNOPSIS</span></span>
<span data-ttu-id="eb7f7-103">Frissíti a készlet tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="eb7f7-103">Updates the properties of a pool.</span></span>

## <span data-ttu-id="eb7f7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eb7f7-104">SYNTAX</span></span>

```
Set-AzBatchPool [-Pool] <PSCloudPool> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb7f7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="eb7f7-105">DESCRIPTION</span></span>
<span data-ttu-id="eb7f7-106">A **set-AzBatchPool** parancsmag az Azure-köteg szolgáltatásban lévő készlet tulajdonságait frissíti.</span><span class="sxs-lookup"><span data-stu-id="eb7f7-106">The **Set-AzBatchPool** cmdlet updates the properties of a pool in the Azure Batch service.</span></span>
<span data-ttu-id="eb7f7-107">A Get-AzBatchPool parancsmaggal **PSCloudPool** objektumot hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="eb7f7-107">Use the Get-AzBatchPool cmdlet to get a **PSCloudPool** object.</span></span>
<span data-ttu-id="eb7f7-108">Módosítsa az objektum tulajdonságait, majd az aktuális parancsmag segítségével végezze el a módosításokat a köteg szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="eb7f7-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="eb7f7-109">Példák</span><span class="sxs-lookup"><span data-stu-id="eb7f7-109">EXAMPLES</span></span>

### <span data-ttu-id="eb7f7-110">Példa 1: a készlet frissítése</span><span class="sxs-lookup"><span data-stu-id="eb7f7-110">Example 1: Update a pool</span></span>
```
PS C:\>$Pool = Get-AzBatchPool "ContosoPool" -BatchContext $Context
PS C:\> $StartTask = New-Object Microsoft.Azure.Commands.Batch.Models.PSStartTask
PS C:\> $StartTask.CommandLine = "cmd /c echo example"
PS C:\> $Pool.StartTask = $StartTask
PS C:\> Set-AzBatchPool -Pool $Pool -BatchContext $Context
```

<span data-ttu-id="eb7f7-111">Az első parancs beolvassa a készletet a **Get-AzBatchPool** függvénnyel, majd a $Pool változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="eb7f7-111">The first command gets a pool by using **Get-AzBatchPool** , and then stores it in the $Pool variable.</span></span>
<span data-ttu-id="eb7f7-112">A következő három parancs a $Pool objektum kezdési tevékenységének specifikációját módosítja.</span><span class="sxs-lookup"><span data-stu-id="eb7f7-112">The next three commands modify the start task specification on the $Pool object.</span></span>
<span data-ttu-id="eb7f7-113">A végleges parancs frissíti a kötegfájlt a $Pool helyi objektumának megfelelően.</span><span class="sxs-lookup"><span data-stu-id="eb7f7-113">The final command updates the Batch service to match the local object in $Pool.</span></span>

## <span data-ttu-id="eb7f7-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eb7f7-114">PARAMETERS</span></span>

### <span data-ttu-id="eb7f7-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="eb7f7-115">-BatchContext</span></span>
<span data-ttu-id="eb7f7-116">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="eb7f7-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="eb7f7-117">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="eb7f7-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="eb7f7-118">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKey parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="eb7f7-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="eb7f7-119">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="eb7f7-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="eb7f7-120">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="eb7f7-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="eb7f7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb7f7-121">-DefaultProfile</span></span>
<span data-ttu-id="eb7f7-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eb7f7-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb7f7-123">-Pool (Pool)</span><span class="sxs-lookup"><span data-stu-id="eb7f7-123">-Pool</span></span>
<span data-ttu-id="eb7f7-124">Azt a **PSCloudPool** adja meg, amelyre a parancsmag frissíti a köteg szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="eb7f7-124">Specifies the **PSCloudPool** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="eb7f7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb7f7-125">CommonParameters</span></span>
<span data-ttu-id="eb7f7-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eb7f7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb7f7-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="eb7f7-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb7f7-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb7f7-128">INPUTS</span></span>

### <span data-ttu-id="eb7f7-129">Microsoft.Azure.Commands.BatCH. Modellek. PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="eb7f7-129">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="eb7f7-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="eb7f7-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="eb7f7-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb7f7-131">OUTPUTS</span></span>

### <span data-ttu-id="eb7f7-132">System. Void</span><span class="sxs-lookup"><span data-stu-id="eb7f7-132">System.Void</span></span>

## <span data-ttu-id="eb7f7-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eb7f7-133">NOTES</span></span>

## <span data-ttu-id="eb7f7-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eb7f7-134">RELATED LINKS</span></span>

[<span data-ttu-id="eb7f7-135">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="eb7f7-135">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="eb7f7-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="eb7f7-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="eb7f7-137">Új – AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="eb7f7-137">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="eb7f7-138">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="eb7f7-138">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="eb7f7-139">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="eb7f7-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
