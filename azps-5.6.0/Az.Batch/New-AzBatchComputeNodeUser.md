---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FE7689DE-4EC6-4C6B-94A4-D22C61CA569D
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchComputeNodeUser.md
ms.openlocfilehash: aaf020d61941057dd0dabac849adb37197e02882
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936306"
---
# <span data-ttu-id="48062-101">New-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="48062-101">New-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="48062-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48062-102">SYNOPSIS</span></span>
<span data-ttu-id="48062-103">Létrehoz egy felhasználói fiókot egy batch számítási csomóponton.</span><span class="sxs-lookup"><span data-stu-id="48062-103">Creates a user account on a Batch compute node.</span></span>

## <span data-ttu-id="48062-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="48062-104">SYNTAX</span></span>

### <span data-ttu-id="48062-105">Azonosító</span><span class="sxs-lookup"><span data-stu-id="48062-105">Id</span></span>
```
New-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> -Name <String> -Password <SecureString>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48062-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="48062-106">ParentObject</span></span>
```
New-AzBatchComputeNodeUser [[-ComputeNode] <PSComputeNode>] -Name <String> -Password <SecureString>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48062-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="48062-107">DESCRIPTION</span></span>
<span data-ttu-id="48062-108">A **New-AzBatchComputeNodeUser** parancsmag létrehoz egy felhasználói fiókot egy Azure Batch számítási csomóponton.</span><span class="sxs-lookup"><span data-stu-id="48062-108">The **New-AzBatchComputeNodeUser** cmdlet creates a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="48062-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="48062-109">EXAMPLES</span></span>

### <span data-ttu-id="48062-110">1. példa: Rendszergazdai hitelesítő adatokkal rendelkező felhasználói fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="48062-110">Example 1: Create a user account that has administrative credentials</span></span>
```
PS C:\>New-AzBatchComputeNodeUser -PoolId "MyPool01" -ComputeNodeId "ComputeNode01" -Name "TestUser" -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(7)) -IsAdmin -BatchContext $Context
```

<span data-ttu-id="48062-111">Ez a parancs létrehoz egy felhasználói fiókot a ComputeNode01 azonosítót használó számítási csomóponton.</span><span class="sxs-lookup"><span data-stu-id="48062-111">This command creates a user account on the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="48062-112">A csomópont abban a készletben található, amely a MyPool01 azonosítót tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="48062-112">The node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="48062-113">A felhasználónév Tesztfelhasználó, a jelszó Jelszó, a fiók hét nap múlva lejár, a fiók pedig rendszergazdai hitelesítő adatokkal rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="48062-113">The user name is TestUser, the password is Password, the account expires in seven days, and the account is has administrative credentials.</span></span>

### <span data-ttu-id="48062-114">2. példa: Felhasználói fiók létrehozása egy számítási csomóponton a folyamat használatával</span><span class="sxs-lookup"><span data-stu-id="48062-114">Example 2: Create a user account on a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode "MyPool01" -ComputeNodeId "ComputeNode01" -BatchContext $Context | New-AzBatchComputeNodeUser -Name "TestUser" -Password "Password" -BatchContext $Context
```

<span data-ttu-id="48062-115">Ez a parancs a ComputeNode01 nevű számítási csomópontot a **Get-AzBatchComputeNode** parancsmag használatával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="48062-115">This command gets the compute node named ComputeNode01 by using the **Get-AzBatchComputeNode** cmdlet.</span></span>
<span data-ttu-id="48062-116">Ez a csomópont abban a készletben található, amely a MyPool01 azonosítót tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="48062-116">That node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="48062-117">A parancs a csomópontot a folyamat műveleti operátorával átadja az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="48062-117">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="48062-118">A parancs létrehoz egy felhasználói fiókot, amely a TestUser felhasználónévvel és a jelszóval rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="48062-118">The command creates a user account that has the user name TestUser and the password Password.</span></span>

## <span data-ttu-id="48062-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48062-119">PARAMETERS</span></span>

### <span data-ttu-id="48062-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="48062-120">-BatchContext</span></span>
<span data-ttu-id="48062-121">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="48062-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="48062-122">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="48062-122">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="48062-123">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse le a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="48062-123">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="48062-124">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="48062-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="48062-125">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="48062-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="48062-126">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="48062-126">-ComputeNode</span></span>
<span data-ttu-id="48062-127">Azt a számítási csomópontot adja meg **PSComputeNode-objektumként,** amelyen ez a parancsmag létrehoz egy felhasználói fiókot.</span><span class="sxs-lookup"><span data-stu-id="48062-127">Specifies the compute node, as a **PSComputeNode** object, on which this cmdlet creates a user account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48062-128">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="48062-128">-ComputeNodeId</span></span>
<span data-ttu-id="48062-129">Annak a számítási csomópontnak az azonosítója, amelyen ez a parancsmag létrehoz egy felhasználói fiókot.</span><span class="sxs-lookup"><span data-stu-id="48062-129">Specifies the ID of the compute node on which this cmdlet creates a user account.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48062-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48062-130">-DefaultProfile</span></span>
<span data-ttu-id="48062-131">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="48062-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48062-132">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="48062-132">-ExpiryTime</span></span>
<span data-ttu-id="48062-133">Az új felhasználói fiók lejárati idejét adja meg.</span><span class="sxs-lookup"><span data-stu-id="48062-133">Specifies the expiry time for the new user account.</span></span>

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

### <span data-ttu-id="48062-134">-IsAdmin</span><span class="sxs-lookup"><span data-stu-id="48062-134">-IsAdmin</span></span>
<span data-ttu-id="48062-135">Azt jelzi, hogy a parancsmag rendszergazdai hitelesítő adatokkal rendelkező felhasználói fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="48062-135">Indicates that the cmdlet creates a user account that has administrative credentials.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48062-136">-Name</span><span class="sxs-lookup"><span data-stu-id="48062-136">-Name</span></span>
<span data-ttu-id="48062-137">Az új helyi Windows-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="48062-137">Specifies the name of the new local Windows account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48062-138">-Password</span><span class="sxs-lookup"><span data-stu-id="48062-138">-Password</span></span>
<span data-ttu-id="48062-139">A felhasználói fiók jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="48062-139">Specifies the user account password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48062-140">-PoolId</span><span class="sxs-lookup"><span data-stu-id="48062-140">-PoolId</span></span>
<span data-ttu-id="48062-141">Annak a készletnek az azonosítója, amely azt a számítási csomópontot tartalmazza, amelyen létre szeretné hozni a felhasználói fiókot.</span><span class="sxs-lookup"><span data-stu-id="48062-141">Specifies the ID of the pool that contains the compute node on which to create the user account.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48062-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48062-142">CommonParameters</span></span>
<span data-ttu-id="48062-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48062-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48062-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48062-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48062-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="48062-145">INPUTS</span></span>

### <span data-ttu-id="48062-146">Microsoft.Azure.Commands.Bat. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="48062-146">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="48062-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="48062-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="48062-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="48062-148">OUTPUTS</span></span>

### <span data-ttu-id="48062-149">System.Void</span><span class="sxs-lookup"><span data-stu-id="48062-149">System.Void</span></span>

## <span data-ttu-id="48062-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="48062-150">NOTES</span></span>

## <span data-ttu-id="48062-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="48062-151">RELATED LINKS</span></span>

[<span data-ttu-id="48062-152">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="48062-152">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="48062-153">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="48062-153">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="48062-154">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="48062-154">Remove-AzBatchComputeNodeUser</span></span>](./Remove-AzBatchComputeNodeUser.md)

[<span data-ttu-id="48062-155">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="48062-155">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
