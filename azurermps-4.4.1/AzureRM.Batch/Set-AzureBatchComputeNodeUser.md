---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A0D620DA-B5A3-4F8F-BD43-A58630C95432
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchComputeNodeUser.md
ms.openlocfilehash: a5e8fd6e6cfba8832365f385cc90357bac59efb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497872"
---
# <span data-ttu-id="35ca0-101">Set-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="35ca0-101">Set-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="35ca0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="35ca0-102">SYNOPSIS</span></span>
<span data-ttu-id="35ca0-103">Egy köteg számítási csomóponton lévő fiók tulajdonságainak módosítása</span><span class="sxs-lookup"><span data-stu-id="35ca0-103">Modifies properties of an account on a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35ca0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="35ca0-104">SYNTAX</span></span>

```
Set-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 [-Password] <String> [-ExpiryTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35ca0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="35ca0-105">DESCRIPTION</span></span>
<span data-ttu-id="35ca0-106">A **set-AzureBatchComputeNodeUser** parancsmag a felhasználói fiókok tulajdonságait egy Azure batch számítási csomóponton módosítja.</span><span class="sxs-lookup"><span data-stu-id="35ca0-106">The **Set-AzureBatchComputeNodeUser** cmdlet modifies properties of a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="35ca0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="35ca0-107">EXAMPLES</span></span>

### <span data-ttu-id="35ca0-108">Példa 1: felhasználói fiók frissítése</span><span class="sxs-lookup"><span data-stu-id="35ca0-108">Example 1: Update a user account</span></span>
```
PS C:\>Set-AzureBatchComputeNodeUser -PoolId "ContosoPool" -ComputeNodeId "tvm-3257026573_1-20150904t230807z" -Name "PFuller" -BatchContext $Context -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(14))
```

<span data-ttu-id="35ca0-109">Ez a parancs módosítja a PFuller nevű felhasználói fiókot a ContosoPool nevű alkalmazáskészletben megadott azonosítót tartalmazó számítási csomóponton.</span><span class="sxs-lookup"><span data-stu-id="35ca0-109">This command modifies user account named PFuller on the compute node that has the specified ID in the pool named ContosoPool.</span></span>
<span data-ttu-id="35ca0-110">A parancs a fiók jelszavát és lejárati idejét módosítja.</span><span class="sxs-lookup"><span data-stu-id="35ca0-110">The command changes the account password and expiry time.</span></span>

## <span data-ttu-id="35ca0-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="35ca0-111">PARAMETERS</span></span>

### <span data-ttu-id="35ca0-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="35ca0-112">-BatchContext</span></span>
<span data-ttu-id="35ca0-113">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="35ca0-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="35ca0-114">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="35ca0-114">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="35ca0-115">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="35ca0-115">-ComputeNodeId</span></span>
<span data-ttu-id="35ca0-116">Annak a számítási csomópontnak az AZONOSÍTÓját adja meg, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="35ca0-116">Specifies the ID of the compute node on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35ca0-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="35ca0-117">-ExpiryTime</span></span>
<span data-ttu-id="35ca0-118">A felhasználói fiók lejárati időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="35ca0-118">Specifies the expiry time for the user account.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35ca0-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="35ca0-119">-Name</span></span>
<span data-ttu-id="35ca0-120">A parancsmag által módosított felhasználói fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="35ca0-120">Specifies the name of the user account that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35ca0-121">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="35ca0-121">-Password</span></span>
<span data-ttu-id="35ca0-122">A felhasználói fiók jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="35ca0-122">Specifies the password for the user account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35ca0-123">-PoolId</span><span class="sxs-lookup"><span data-stu-id="35ca0-123">-PoolId</span></span>
<span data-ttu-id="35ca0-124">Annak a készletnek az AZONOSÍTÓját adja meg, amely a parancsmag által üzemeltetett számítási csomópontot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="35ca0-124">Specifies the ID of the pool that contains the compute node on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35ca0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35ca0-125">-DefaultProfile</span></span>
<span data-ttu-id="35ca0-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="35ca0-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35ca0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35ca0-127">CommonParameters</span></span>
<span data-ttu-id="35ca0-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="35ca0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35ca0-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35ca0-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35ca0-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="35ca0-130">INPUTS</span></span>

### <span data-ttu-id="35ca0-131">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="35ca0-131">BatchAccountContext</span></span>
<span data-ttu-id="35ca0-132">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="35ca0-132">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="35ca0-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="35ca0-133">OUTPUTS</span></span>

## <span data-ttu-id="35ca0-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="35ca0-134">NOTES</span></span>

## <span data-ttu-id="35ca0-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="35ca0-135">RELATED LINKS</span></span>

[<span data-ttu-id="35ca0-136">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="35ca0-136">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="35ca0-137">Új – AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="35ca0-137">New-AzureBatchComputeNodeUser</span></span>](./New-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="35ca0-138">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="35ca0-138">Remove-AzureBatchComputeNodeUser</span></span>](./Remove-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="35ca0-139">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="35ca0-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


