---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchAutoScale.md
ms.openlocfilehash: f0530b509bea965c1c901992f9a91b351dae9ae3
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "94017202"
---
# <span data-ttu-id="e9d35-101">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="e9d35-101">Disable-AzBatchAutoScale</span></span>

## <span data-ttu-id="e9d35-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e9d35-102">SYNOPSIS</span></span>
<span data-ttu-id="e9d35-103">Letiltja a készlet automatikus méretezését.</span><span class="sxs-lookup"><span data-stu-id="e9d35-103">Disables automatic scaling of a pool.</span></span>

## <span data-ttu-id="e9d35-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e9d35-104">SYNTAX</span></span>

```
Disable-AzBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9d35-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e9d35-105">DESCRIPTION</span></span>
<span data-ttu-id="e9d35-106">A **disable-AzBatchAutoScale** parancsmag letiltja a megadott készlet automatikus méretezését.</span><span class="sxs-lookup"><span data-stu-id="e9d35-106">The **Disable-AzBatchAutoScale** cmdlet disables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="e9d35-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e9d35-107">EXAMPLES</span></span>

### <span data-ttu-id="e9d35-108">1. példa: a készlet automatikus méretezésének letiltása</span><span class="sxs-lookup"><span data-stu-id="e9d35-108">Example 1: Disable automatic scaling of a pool</span></span>
```
PS C:\>Disable-AzBatchAutoScale -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="e9d35-109">Ez a parancs letiltja az automatikus méretezést a MyPool nevű alkalmazáskészlethez.</span><span class="sxs-lookup"><span data-stu-id="e9d35-109">This command disables automatic scaling for the pool named MyPool.</span></span>

## <span data-ttu-id="e9d35-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e9d35-110">PARAMETERS</span></span>

### <span data-ttu-id="e9d35-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e9d35-111">-BatchContext</span></span>
<span data-ttu-id="e9d35-112">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="e9d35-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e9d35-113">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="e9d35-113">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e9d35-114">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKey parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="e9d35-114">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e9d35-115">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="e9d35-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e9d35-116">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="e9d35-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e9d35-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9d35-117">-DefaultProfile</span></span>
<span data-ttu-id="e9d35-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e9d35-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9d35-119">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="e9d35-119">-Id</span></span>
<span data-ttu-id="e9d35-120">A készlet objektum-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e9d35-120">Specifies the object ID of the pool.</span></span>

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

### <span data-ttu-id="e9d35-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9d35-121">CommonParameters</span></span>
<span data-ttu-id="e9d35-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e9d35-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9d35-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e9d35-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9d35-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9d35-124">INPUTS</span></span>

### <span data-ttu-id="e9d35-125">System. String</span><span class="sxs-lookup"><span data-stu-id="e9d35-125">System.String</span></span>

### <span data-ttu-id="e9d35-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e9d35-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e9d35-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9d35-127">OUTPUTS</span></span>

### <span data-ttu-id="e9d35-128">System. Void</span><span class="sxs-lookup"><span data-stu-id="e9d35-128">System.Void</span></span>

## <span data-ttu-id="e9d35-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e9d35-129">NOTES</span></span>

## <span data-ttu-id="e9d35-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e9d35-130">RELATED LINKS</span></span>

[<span data-ttu-id="e9d35-131">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="e9d35-131">Enable-AzBatchAutoScale</span></span>](./Enable-AzBatchAutoScale.md)

[<span data-ttu-id="e9d35-132">Teszt-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="e9d35-132">Test-AzBatchAutoScale</span></span>](./Test-AzBatchAutoScale.md)

[<span data-ttu-id="e9d35-133">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="e9d35-133">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


