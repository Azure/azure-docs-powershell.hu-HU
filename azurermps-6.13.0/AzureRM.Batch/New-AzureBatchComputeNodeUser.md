---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FE7689DE-4EC6-4C6B-94A4-D22C61CA569D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchComputeNodeUser.md
ms.openlocfilehash: 1e95eff4e93b1b7d55a099ad188fc196025cd06f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492874"
---
# <span data-ttu-id="9e284-101">New-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="9e284-101">New-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="9e284-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9e284-102">SYNOPSIS</span></span>
<span data-ttu-id="9e284-103">Felhasználói fiókot hoz létre a kötegelt számítási csomóponton.</span><span class="sxs-lookup"><span data-stu-id="9e284-103">Creates a user account on a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e284-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9e284-104">SYNTAX</span></span>

### <span data-ttu-id="9e284-105">Azonosító</span><span class="sxs-lookup"><span data-stu-id="9e284-105">Id</span></span>
```
New-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> -Name <String>
 -Password <SecureString> [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e284-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="9e284-106">ParentObject</span></span>
```
New-AzureBatchComputeNodeUser [[-ComputeNode] <PSComputeNode>] -Name <String> -Password <SecureString>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e284-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9e284-107">DESCRIPTION</span></span>
<span data-ttu-id="9e284-108">A **New-AzureBatchComputeNodeUser** parancsmag létrehoz egy felhasználói fiókot egy Azure batch számítási csomóponton.</span><span class="sxs-lookup"><span data-stu-id="9e284-108">The **New-AzureBatchComputeNodeUser** cmdlet creates a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="9e284-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9e284-109">EXAMPLES</span></span>

### <span data-ttu-id="9e284-110">Példa 1: rendszergazdai hitelesítő adatokkal rendelkező felhasználói fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="9e284-110">Example 1: Create a user account that has administrative credentials</span></span>
```
PS C:\>New-AzureBatchComputeNodeUser -PoolId "MyPool01" -ComputeNodeId "ComputeNode01" -Name "TestUser" -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(7)) -IsAdmin -BatchContext $Context
```

<span data-ttu-id="9e284-111">Ez a parancs létrehoz egy felhasználói fiókot a számítási csomóponton, amely az azonosító ComputeNode01 tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="9e284-111">This command creates a user account on the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="9e284-112">A csomópont az azonosító MyPool01 tartalmazó készletben található.</span><span class="sxs-lookup"><span data-stu-id="9e284-112">The node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="9e284-113">A Felhasználónév tesztfelhasználó, a jelszó jelszó, a fiók hét napon lejár, és a fiók rendszergazdai hitelesítő adatokkal rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="9e284-113">The user name is TestUser, the password is Password, the account expires in seven days, and the account is has administrative credentials.</span></span>

### <span data-ttu-id="9e284-114">2. példa: felhasználói fiók létrehozása számítási csomóponton a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="9e284-114">Example 2: Create a user account on a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchComputeNode "MyPool01" -ComputeNodeId "ComputeNode01" -BatchContext $Context | New-AzureBatchComputeNodeUser -Name "TestUser" -Password "Password" -BatchContext $Context
```

<span data-ttu-id="9e284-115">Ez a parancs a **Get-AzureBatchComputeNode** parancsmag használatával kapja meg a ComputeNode01 nevű számítási csomópontot.</span><span class="sxs-lookup"><span data-stu-id="9e284-115">This command gets the compute node named ComputeNode01 by using the **Get-AzureBatchComputeNode** cmdlet.</span></span>
<span data-ttu-id="9e284-116">Ez a csomópont abban a készletben található, amely az azonosító MyPool01 tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="9e284-116">That node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="9e284-117">A parancs a csővezeték-kezelő segítségével átadja az aktuális parancsmaghoz tartozó csomópontot.</span><span class="sxs-lookup"><span data-stu-id="9e284-117">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9e284-118">A parancs létrehozza azt a felhasználói fiókot, amelynek a felhasználónevét TestUserand a jelszó.</span><span class="sxs-lookup"><span data-stu-id="9e284-118">The command creates a user account that has the user name TestUserand the password Password.</span></span>

## <span data-ttu-id="9e284-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9e284-119">PARAMETERS</span></span>

### <span data-ttu-id="9e284-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="9e284-120">-BatchContext</span></span>
<span data-ttu-id="9e284-121">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="9e284-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9e284-122">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="9e284-122">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="9e284-123">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="9e284-123">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="9e284-124">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="9e284-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="9e284-125">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="9e284-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="9e284-126">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="9e284-126">-ComputeNode</span></span>
<span data-ttu-id="9e284-127">A számítási csomópontot **PSComputeNode** objektumként adja meg, amelyen ez a parancsmag felhasználói fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9e284-127">Specifies the compute node, as a **PSComputeNode** object, on which this cmdlet creates a user account.</span></span>

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

### <span data-ttu-id="9e284-128">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="9e284-128">-ComputeNodeId</span></span>
<span data-ttu-id="9e284-129">Annak a számítási csomópontnak az AZONOSÍTÓját adja meg, amelyen ez a parancsmag létrehoz egy felhasználói fiókot.</span><span class="sxs-lookup"><span data-stu-id="9e284-129">Specifies the ID of the compute node on which this cmdlet creates a user account.</span></span>

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

### <span data-ttu-id="9e284-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e284-130">-DefaultProfile</span></span>
<span data-ttu-id="9e284-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9e284-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e284-132">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="9e284-132">-ExpiryTime</span></span>
<span data-ttu-id="9e284-133">Az új felhasználói fiók lejárati időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e284-133">Specifies the expiry time for the new user account.</span></span>

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

### <span data-ttu-id="9e284-134">-IsAdmin</span><span class="sxs-lookup"><span data-stu-id="9e284-134">-IsAdmin</span></span>
<span data-ttu-id="9e284-135">Azt jelzi, hogy a parancsmag olyan felhasználói fiókot hoz létre, amely rendszergazdai hitelesítő adatokkal rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="9e284-135">Indicates that the cmdlet creates a user account that has administrative credentials.</span></span>

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

### <span data-ttu-id="9e284-136">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9e284-136">-Name</span></span>
<span data-ttu-id="9e284-137">Az új helyi Windows-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e284-137">Specifies the name of the new local Windows account.</span></span>

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

### <span data-ttu-id="9e284-138">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="9e284-138">-Password</span></span>
<span data-ttu-id="9e284-139">A felhasználói fiók jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e284-139">Specifies the user account password.</span></span>

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

### <span data-ttu-id="9e284-140">-PoolId</span><span class="sxs-lookup"><span data-stu-id="9e284-140">-PoolId</span></span>
<span data-ttu-id="9e284-141">Annak a készletnek az AZONOSÍTÓját adja meg, amely a felhasználói fiókot létrehozó számítási csomópontot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="9e284-141">Specifies the ID of the pool that contains the compute node on which to create the user account.</span></span>

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

### <span data-ttu-id="9e284-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e284-142">CommonParameters</span></span>
<span data-ttu-id="9e284-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9e284-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e284-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e284-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e284-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e284-145">INPUTS</span></span>

### <span data-ttu-id="9e284-146">Microsoft.Azure.Commands.BatCH. Modellek. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="9e284-146">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>
<span data-ttu-id="9e284-147">Paraméterek: ComputeNode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9e284-147">Parameters: ComputeNode (ByValue)</span></span>

### <span data-ttu-id="9e284-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9e284-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="9e284-149">Paraméterek: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9e284-149">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="9e284-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e284-150">OUTPUTS</span></span>

### <span data-ttu-id="9e284-151">System. Void</span><span class="sxs-lookup"><span data-stu-id="9e284-151">System.Void</span></span>

## <span data-ttu-id="9e284-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9e284-152">NOTES</span></span>

## <span data-ttu-id="9e284-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9e284-153">RELATED LINKS</span></span>

[<span data-ttu-id="9e284-154">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="9e284-154">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="9e284-155">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="9e284-155">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="9e284-156">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="9e284-156">Remove-AzureBatchComputeNodeUser</span></span>](./Remove-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="9e284-157">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="9e284-157">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


