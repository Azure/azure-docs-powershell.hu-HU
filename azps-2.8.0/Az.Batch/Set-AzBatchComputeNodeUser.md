---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A0D620DA-B5A3-4F8F-BD43-A58630C95432
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchComputeNodeUser.md
ms.openlocfilehash: 95530c75575742e848f39861bed1710be75e318c
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93847977"
---
# <span data-ttu-id="2eee8-101">Set-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="2eee8-101">Set-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="2eee8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2eee8-102">SYNOPSIS</span></span>
<span data-ttu-id="2eee8-103">Egy köteg számítási csomóponton lévő fiók tulajdonságainak módosítása</span><span class="sxs-lookup"><span data-stu-id="2eee8-103">Modifies properties of an account on a Batch compute node.</span></span>

## <span data-ttu-id="2eee8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2eee8-104">SYNTAX</span></span>

```
Set-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 [-Password] <SecureString> [-ExpiryTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2eee8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2eee8-105">DESCRIPTION</span></span>
<span data-ttu-id="2eee8-106">A **set-AzBatchComputeNodeUser** parancsmag a felhasználói fiókok tulajdonságait egy Azure batch számítási csomóponton módosítja.</span><span class="sxs-lookup"><span data-stu-id="2eee8-106">The **Set-AzBatchComputeNodeUser** cmdlet modifies properties of a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="2eee8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2eee8-107">EXAMPLES</span></span>

### <span data-ttu-id="2eee8-108">Példa 1: felhasználói fiók frissítése</span><span class="sxs-lookup"><span data-stu-id="2eee8-108">Example 1: Update a user account</span></span>
```
PS C:\>Set-AzBatchComputeNodeUser -PoolId "ContosoPool" -ComputeNodeId "tvm-3257026573_1-20150904t230807z" -Name "PFuller" -BatchContext $Context -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(14))
```

<span data-ttu-id="2eee8-109">Ez a parancs módosítja a PFuller nevű felhasználói fiókot a ContosoPool nevű alkalmazáskészletben megadott azonosítót tartalmazó számítási csomóponton.</span><span class="sxs-lookup"><span data-stu-id="2eee8-109">This command modifies user account named PFuller on the compute node that has the specified ID in the pool named ContosoPool.</span></span>
<span data-ttu-id="2eee8-110">A parancs a fiók jelszavát és lejárati idejét módosítja.</span><span class="sxs-lookup"><span data-stu-id="2eee8-110">The command changes the account password and expiry time.</span></span>

## <span data-ttu-id="2eee8-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2eee8-111">PARAMETERS</span></span>

### <span data-ttu-id="2eee8-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="2eee8-112">-BatchContext</span></span>
<span data-ttu-id="2eee8-113">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="2eee8-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2eee8-114">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="2eee8-114">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="2eee8-115">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="2eee8-115">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="2eee8-116">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="2eee8-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="2eee8-117">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="2eee8-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="2eee8-118">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="2eee8-118">-ComputeNodeId</span></span>
<span data-ttu-id="2eee8-119">Annak a számítási csomópontnak az AZONOSÍTÓját adja meg, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="2eee8-119">Specifies the ID of the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="2eee8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eee8-120">-DefaultProfile</span></span>
<span data-ttu-id="2eee8-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2eee8-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2eee8-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="2eee8-122">-ExpiryTime</span></span>
<span data-ttu-id="2eee8-123">A felhasználói fiók lejárati időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2eee8-123">Specifies the expiry time for the user account.</span></span>

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

### <span data-ttu-id="2eee8-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2eee8-124">-Name</span></span>
<span data-ttu-id="2eee8-125">A parancsmag által módosított felhasználói fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2eee8-125">Specifies the name of the user account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="2eee8-126">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="2eee8-126">-Password</span></span>
<span data-ttu-id="2eee8-127">A felhasználói fiók jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2eee8-127">Specifies the password for the user account.</span></span>

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

### <span data-ttu-id="2eee8-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="2eee8-128">-PoolId</span></span>
<span data-ttu-id="2eee8-129">Annak a készletnek az AZONOSÍTÓját adja meg, amely a parancsmag által üzemeltetett számítási csomópontot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="2eee8-129">Specifies the ID of the pool that contains the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="2eee8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eee8-130">CommonParameters</span></span>
<span data-ttu-id="2eee8-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2eee8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eee8-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2eee8-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eee8-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2eee8-133">INPUTS</span></span>

### <span data-ttu-id="2eee8-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2eee8-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="2eee8-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2eee8-135">OUTPUTS</span></span>

### <span data-ttu-id="2eee8-136">System. Void</span><span class="sxs-lookup"><span data-stu-id="2eee8-136">System.Void</span></span>

## <span data-ttu-id="2eee8-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2eee8-137">NOTES</span></span>

## <span data-ttu-id="2eee8-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2eee8-138">RELATED LINKS</span></span>

[<span data-ttu-id="2eee8-139">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="2eee8-139">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="2eee8-140">Új – AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="2eee8-140">New-AzBatchComputeNodeUser</span></span>](./New-AzBatchComputeNodeUser.md)

[<span data-ttu-id="2eee8-141">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="2eee8-141">Remove-AzBatchComputeNodeUser</span></span>](./Remove-AzBatchComputeNodeUser.md)

[<span data-ttu-id="2eee8-142">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="2eee8-142">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)

