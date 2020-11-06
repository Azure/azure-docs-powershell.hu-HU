---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 23893EAE-47F3-45AA-AEB2-354FB8316C25
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPool.md
ms.openlocfilehash: d18a6bdc9a2064e21507c909005692d5d21c63f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499208"
---
# <span data-ttu-id="39aa0-101">Set-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="39aa0-101">Set-AzureBatchPool</span></span>

## <span data-ttu-id="39aa0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="39aa0-102">SYNOPSIS</span></span>
<span data-ttu-id="39aa0-103">Frissíti a készlet tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="39aa0-103">Updates the properties of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39aa0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="39aa0-104">SYNTAX</span></span>

```
Set-AzureBatchPool [-Pool] <PSCloudPool> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39aa0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="39aa0-105">DESCRIPTION</span></span>
<span data-ttu-id="39aa0-106">A **set-AzureBatchPool** parancsmag az Azure-köteg szolgáltatásban lévő készlet tulajdonságait frissíti.</span><span class="sxs-lookup"><span data-stu-id="39aa0-106">The **Set-AzureBatchPool** cmdlet updates the properties of a pool in the Azure Batch service.</span></span>
<span data-ttu-id="39aa0-107">A Get-AzureBatchPool parancsmaggal **PSCloudPool** objektumot hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="39aa0-107">Use the Get-AzureBatchPool cmdlet to get a **PSCloudPool** object.</span></span>
<span data-ttu-id="39aa0-108">Módosítsa az objektum tulajdonságait, majd az aktuális parancsmag segítségével végezze el a módosításokat a köteg szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="39aa0-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="39aa0-109">Példák</span><span class="sxs-lookup"><span data-stu-id="39aa0-109">EXAMPLES</span></span>

### <span data-ttu-id="39aa0-110">Példa 1: a készlet frissítése</span><span class="sxs-lookup"><span data-stu-id="39aa0-110">Example 1: Update a pool</span></span>
```
PS C:\>$Pool = Get-AzureBatchPool "ContosoPool" -BatchContext $Context
PS C:\> $StartTask = New-Object Microsoft.Azure.Commands.Batch.Models.PSStartTask
PS C:\> $StartTask.CommandLine = "cmd /c echo example"
PS C:\> $Pool.StartTask = $StartTask
PS C:\> Set-AzureBatchPool -Pool $Pool -BatchContext $Context
```

<span data-ttu-id="39aa0-111">Az első parancs beolvassa a készletet a **Get-AzureBatchPool** függvénnyel, majd a $Pool változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="39aa0-111">The first command gets a pool by using **Get-AzureBatchPool** , and then stores it in the $Pool variable.</span></span>

<span data-ttu-id="39aa0-112">A következő három parancs a $Pool objektum kezdési tevékenységének specifikációját módosítja.</span><span class="sxs-lookup"><span data-stu-id="39aa0-112">The next three commands modify the start task specification on the $Pool object.</span></span>

<span data-ttu-id="39aa0-113">A végleges parancs frissíti a kötegfájlt a $Pool helyi objektumának megfelelően.</span><span class="sxs-lookup"><span data-stu-id="39aa0-113">The final command updates the Batch service to match the local object in $Pool.</span></span>

## <span data-ttu-id="39aa0-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="39aa0-114">PARAMETERS</span></span>

### <span data-ttu-id="39aa0-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="39aa0-115">-BatchContext</span></span>
<span data-ttu-id="39aa0-116">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="39aa0-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="39aa0-117">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="39aa0-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="39aa0-118">-Pool (Pool)</span><span class="sxs-lookup"><span data-stu-id="39aa0-118">-Pool</span></span>
<span data-ttu-id="39aa0-119">Azt a **PSCloudPool** adja meg, amelyre a parancsmag frissíti a köteg szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="39aa0-119">Specifies the **PSCloudPool** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="39aa0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39aa0-120">-DefaultProfile</span></span>
<span data-ttu-id="39aa0-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="39aa0-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39aa0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39aa0-122">CommonParameters</span></span>
<span data-ttu-id="39aa0-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="39aa0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39aa0-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39aa0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39aa0-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="39aa0-125">INPUTS</span></span>

### <span data-ttu-id="39aa0-126">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="39aa0-126">BatchAccountContext</span></span>
<span data-ttu-id="39aa0-127">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="39aa0-127">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="39aa0-128">PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="39aa0-128">PSCloudPool</span></span>
<span data-ttu-id="39aa0-129">A "pool" paraméter elfogadja a "PSCloudPool" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="39aa0-129">Parameter 'Pool' accepts value of type 'PSCloudPool' from the pipeline</span></span>

## <span data-ttu-id="39aa0-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="39aa0-130">OUTPUTS</span></span>

## <span data-ttu-id="39aa0-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="39aa0-131">NOTES</span></span>

## <span data-ttu-id="39aa0-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="39aa0-132">RELATED LINKS</span></span>

[<span data-ttu-id="39aa0-133">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="39aa0-133">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="39aa0-134">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="39aa0-134">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="39aa0-135">Új – AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="39aa0-135">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="39aa0-136">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="39aa0-136">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="39aa0-137">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="39aa0-137">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


