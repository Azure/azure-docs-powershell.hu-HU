---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FE7689DE-4EC6-4C6B-94A4-D22C61CA569D
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchComputeNodeUser.md
ms.openlocfilehash: 5695f0bf0a7cc65b1eb032be33116cc40ec0618e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024907"
---
# <span data-ttu-id="76e49-101">New-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="76e49-101">New-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="76e49-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="76e49-102">SYNOPSIS</span></span>
<span data-ttu-id="76e49-103">Felhasználói fiókot hoz létre a kötegelt számítási csomóponton.</span><span class="sxs-lookup"><span data-stu-id="76e49-103">Creates a user account on a Batch compute node.</span></span>

## <span data-ttu-id="76e49-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="76e49-104">SYNTAX</span></span>

### <span data-ttu-id="76e49-105">Azonosító</span><span class="sxs-lookup"><span data-stu-id="76e49-105">Id</span></span>
```
New-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> -Name <String> -Password <SecureString>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76e49-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="76e49-106">ParentObject</span></span>
```
New-AzBatchComputeNodeUser [[-ComputeNode] <PSComputeNode>] -Name <String> -Password <SecureString>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76e49-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="76e49-107">DESCRIPTION</span></span>
<span data-ttu-id="76e49-108">A **New-AzBatchComputeNodeUser** parancsmag létrehoz egy felhasználói fiókot egy Azure batch számítási csomóponton.</span><span class="sxs-lookup"><span data-stu-id="76e49-108">The **New-AzBatchComputeNodeUser** cmdlet creates a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="76e49-109">Példák</span><span class="sxs-lookup"><span data-stu-id="76e49-109">EXAMPLES</span></span>

### <span data-ttu-id="76e49-110">Példa 1: rendszergazdai hitelesítő adatokkal rendelkező felhasználói fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="76e49-110">Example 1: Create a user account that has administrative credentials</span></span>
```
PS C:\>New-AzBatchComputeNodeUser -PoolId "MyPool01" -ComputeNodeId "ComputeNode01" -Name "TestUser" -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(7)) -IsAdmin -BatchContext $Context
```

<span data-ttu-id="76e49-111">Ez a parancs létrehoz egy felhasználói fiókot a számítási csomóponton, amely az azonosító ComputeNode01 tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="76e49-111">This command creates a user account on the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="76e49-112">A csomópont az azonosító MyPool01 tartalmazó készletben található.</span><span class="sxs-lookup"><span data-stu-id="76e49-112">The node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="76e49-113">A Felhasználónév tesztfelhasználó, a jelszó jelszó, a fiók hét napon lejár, és a fiók rendszergazdai hitelesítő adatokkal rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="76e49-113">The user name is TestUser, the password is Password, the account expires in seven days, and the account is has administrative credentials.</span></span>

### <span data-ttu-id="76e49-114">2. példa: felhasználói fiók létrehozása számítási csomóponton a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="76e49-114">Example 2: Create a user account on a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode "MyPool01" -ComputeNodeId "ComputeNode01" -BatchContext $Context | New-AzBatchComputeNodeUser -Name "TestUser" -Password "Password" -BatchContext $Context
```

<span data-ttu-id="76e49-115">Ez a parancs a **Get-AzBatchComputeNode** parancsmag használatával kapja meg a ComputeNode01 nevű számítási csomópontot.</span><span class="sxs-lookup"><span data-stu-id="76e49-115">This command gets the compute node named ComputeNode01 by using the **Get-AzBatchComputeNode** cmdlet.</span></span>
<span data-ttu-id="76e49-116">Ez a csomópont abban a készletben található, amely az azonosító MyPool01 tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="76e49-116">That node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="76e49-117">A parancs a csővezeték-kezelő segítségével átadja az aktuális parancsmaghoz tartozó csomópontot.</span><span class="sxs-lookup"><span data-stu-id="76e49-117">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="76e49-118">A parancs létrehoz egy olyan felhasználói fiókot, amely rendelkezik a Felhasználónév tesztfelhasználó és a jelszó jelszavával.</span><span class="sxs-lookup"><span data-stu-id="76e49-118">The command creates a user account that has the user name TestUser and the password Password.</span></span>

## <span data-ttu-id="76e49-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="76e49-119">PARAMETERS</span></span>

### <span data-ttu-id="76e49-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="76e49-120">-BatchContext</span></span>
<span data-ttu-id="76e49-121">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="76e49-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="76e49-122">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="76e49-122">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="76e49-123">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKey parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="76e49-123">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="76e49-124">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="76e49-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="76e49-125">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="76e49-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="76e49-126">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="76e49-126">-ComputeNode</span></span>
<span data-ttu-id="76e49-127">A számítási csomópontot **PSComputeNode** objektumként adja meg, amelyen ez a parancsmag felhasználói fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="76e49-127">Specifies the compute node, as a **PSComputeNode** object, on which this cmdlet creates a user account.</span></span>

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

### <span data-ttu-id="76e49-128">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="76e49-128">-ComputeNodeId</span></span>
<span data-ttu-id="76e49-129">Annak a számítási csomópontnak az AZONOSÍTÓját adja meg, amelyen ez a parancsmag létrehoz egy felhasználói fiókot.</span><span class="sxs-lookup"><span data-stu-id="76e49-129">Specifies the ID of the compute node on which this cmdlet creates a user account.</span></span>

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

### <span data-ttu-id="76e49-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76e49-130">-DefaultProfile</span></span>
<span data-ttu-id="76e49-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="76e49-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76e49-132">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="76e49-132">-ExpiryTime</span></span>
<span data-ttu-id="76e49-133">Az új felhasználói fiók lejárati időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="76e49-133">Specifies the expiry time for the new user account.</span></span>

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

### <span data-ttu-id="76e49-134">-IsAdmin</span><span class="sxs-lookup"><span data-stu-id="76e49-134">-IsAdmin</span></span>
<span data-ttu-id="76e49-135">Azt jelzi, hogy a parancsmag olyan felhasználói fiókot hoz létre, amely rendszergazdai hitelesítő adatokkal rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="76e49-135">Indicates that the cmdlet creates a user account that has administrative credentials.</span></span>

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

### <span data-ttu-id="76e49-136">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="76e49-136">-Name</span></span>
<span data-ttu-id="76e49-137">Az új helyi Windows-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="76e49-137">Specifies the name of the new local Windows account.</span></span>

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

### <span data-ttu-id="76e49-138">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="76e49-138">-Password</span></span>
<span data-ttu-id="76e49-139">A felhasználói fiók jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="76e49-139">Specifies the user account password.</span></span>

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

### <span data-ttu-id="76e49-140">-PoolId</span><span class="sxs-lookup"><span data-stu-id="76e49-140">-PoolId</span></span>
<span data-ttu-id="76e49-141">Annak a készletnek az AZONOSÍTÓját adja meg, amely a felhasználói fiókot létrehozó számítási csomópontot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="76e49-141">Specifies the ID of the pool that contains the compute node on which to create the user account.</span></span>

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

### <span data-ttu-id="76e49-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76e49-142">CommonParameters</span></span>
<span data-ttu-id="76e49-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="76e49-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76e49-144">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="76e49-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76e49-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="76e49-145">INPUTS</span></span>

### <span data-ttu-id="76e49-146">Microsoft.Azure.Commands.BatCH. Modellek. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="76e49-146">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="76e49-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="76e49-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="76e49-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="76e49-148">OUTPUTS</span></span>

### <span data-ttu-id="76e49-149">System. Void</span><span class="sxs-lookup"><span data-stu-id="76e49-149">System.Void</span></span>

## <span data-ttu-id="76e49-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="76e49-150">NOTES</span></span>

## <span data-ttu-id="76e49-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="76e49-151">RELATED LINKS</span></span>

[<span data-ttu-id="76e49-152">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="76e49-152">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="76e49-153">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="76e49-153">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="76e49-154">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="76e49-154">Remove-AzBatchComputeNodeUser</span></span>](./Remove-AzBatchComputeNodeUser.md)

[<span data-ttu-id="76e49-155">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="76e49-155">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
