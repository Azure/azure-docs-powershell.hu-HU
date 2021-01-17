---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A0D620DA-B5A3-4F8F-BD43-A58630C95432
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchComputeNodeUser.md
ms.openlocfilehash: 636ceb216c7bb6aec2016bdd047a26f707108c9b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478193"
---
# <span data-ttu-id="09b44-101">Set-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="09b44-101">Set-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="09b44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09b44-102">SYNOPSIS</span></span>
<span data-ttu-id="09b44-103">Módosítja egy fiók tulajdonságait egy batch számítási csomóponton.</span><span class="sxs-lookup"><span data-stu-id="09b44-103">Modifies properties of an account on a Batch compute node.</span></span>

## <span data-ttu-id="09b44-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="09b44-104">SYNTAX</span></span>

```
Set-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 [-Password] <SecureString> [-ExpiryTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09b44-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="09b44-105">DESCRIPTION</span></span>
<span data-ttu-id="09b44-106">A **Set-AzBatchComputeNodeUser** parancsmag módosítja egy felhasználói fiók tulajdonságait egy Azure Batch-számítási csomóponton.</span><span class="sxs-lookup"><span data-stu-id="09b44-106">The **Set-AzBatchComputeNodeUser** cmdlet modifies properties of a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="09b44-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="09b44-107">EXAMPLES</span></span>

### <span data-ttu-id="09b44-108">1. példa: Felhasználói fiók frissítése</span><span class="sxs-lookup"><span data-stu-id="09b44-108">Example 1: Update a user account</span></span>
```
PS C:\>Set-AzBatchComputeNodeUser -PoolId "ContosoPool" -ComputeNodeId "tvm-3257026573_1-20150904t230807z" -Name "PFuller" -BatchContext $Context -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(14))
```

<span data-ttu-id="09b44-109">Ez a parancs módosítja a PFuller nevű felhasználói fiókot abban a számítási csomópontban, amely a ContosoPool nevű készletben tartalmazza a megadott azonosítót.</span><span class="sxs-lookup"><span data-stu-id="09b44-109">This command modifies user account named PFuller on the compute node that has the specified ID in the pool named ContosoPool.</span></span>
<span data-ttu-id="09b44-110">A parancs módosítja a fiók jelszavát és a lejárati időt.</span><span class="sxs-lookup"><span data-stu-id="09b44-110">The command changes the account password and expiry time.</span></span>

## <span data-ttu-id="09b44-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09b44-111">PARAMETERS</span></span>

### <span data-ttu-id="09b44-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="09b44-112">-BatchContext</span></span>
<span data-ttu-id="09b44-113">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="09b44-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="09b44-114">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="09b44-114">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="09b44-115">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse ki a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="09b44-115">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="09b44-116">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="09b44-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="09b44-117">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="09b44-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="09b44-118">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="09b44-118">-ComputeNodeId</span></span>
<span data-ttu-id="09b44-119">Annak a számítási csomópontnak az azonosítója, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="09b44-119">Specifies the ID of the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="09b44-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09b44-120">-DefaultProfile</span></span>
<span data-ttu-id="09b44-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="09b44-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09b44-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="09b44-122">-ExpiryTime</span></span>
<span data-ttu-id="09b44-123">A felhasználói fiók lejárati idejét adja meg.</span><span class="sxs-lookup"><span data-stu-id="09b44-123">Specifies the expiry time for the user account.</span></span>

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

### <span data-ttu-id="09b44-124">-Name</span><span class="sxs-lookup"><span data-stu-id="09b44-124">-Name</span></span>
<span data-ttu-id="09b44-125">Annak a felhasználói fióknak a nevét adja meg, amely módosítja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="09b44-125">Specifies the name of the user account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="09b44-126">-Password</span><span class="sxs-lookup"><span data-stu-id="09b44-126">-Password</span></span>
<span data-ttu-id="09b44-127">Megadja a felhasználói fiók jelszavát.</span><span class="sxs-lookup"><span data-stu-id="09b44-127">Specifies the password for the user account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09b44-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="09b44-128">-PoolId</span></span>
<span data-ttu-id="09b44-129">Annak a készletnek az azonosítóját adja meg, amelyen az a számítási csomópont található, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="09b44-129">Specifies the ID of the pool that contains the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="09b44-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09b44-130">CommonParameters</span></span>
<span data-ttu-id="09b44-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09b44-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09b44-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="09b44-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09b44-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="09b44-133">INPUTS</span></span>

### <span data-ttu-id="09b44-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="09b44-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="09b44-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="09b44-135">OUTPUTS</span></span>

### <span data-ttu-id="09b44-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="09b44-136">System.Void</span></span>

## <span data-ttu-id="09b44-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="09b44-137">NOTES</span></span>

## <span data-ttu-id="09b44-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="09b44-138">RELATED LINKS</span></span>

[<span data-ttu-id="09b44-139">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="09b44-139">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="09b44-140">New-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="09b44-140">New-AzBatchComputeNodeUser</span></span>](./New-AzBatchComputeNodeUser.md)

[<span data-ttu-id="09b44-141">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="09b44-141">Remove-AzBatchComputeNodeUser</span></span>](./Remove-AzBatchComputeNodeUser.md)

[<span data-ttu-id="09b44-142">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="09b44-142">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
