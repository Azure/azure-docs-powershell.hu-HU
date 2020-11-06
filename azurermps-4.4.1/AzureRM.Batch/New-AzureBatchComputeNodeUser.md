---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FE7689DE-4EC6-4C6B-94A4-D22C61CA569D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchComputeNodeUser.md
ms.openlocfilehash: 6289aa916b4d03559fccb11ea0a8897f4b506b53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497907"
---
# <span data-ttu-id="ceace-101">New-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="ceace-101">New-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="ceace-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ceace-102">SYNOPSIS</span></span>
<span data-ttu-id="ceace-103">Felhasználói fiókot hoz létre a kötegelt számítási csomóponton.</span><span class="sxs-lookup"><span data-stu-id="ceace-103">Creates a user account on a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ceace-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ceace-104">SYNTAX</span></span>

### <span data-ttu-id="ceace-105">Azonosító</span><span class="sxs-lookup"><span data-stu-id="ceace-105">Id</span></span>
```
New-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> -Name <String> -Password <String>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ceace-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="ceace-106">ParentObject</span></span>
```
New-AzureBatchComputeNodeUser [[-ComputeNode] <PSComputeNode>] -Name <String> -Password <String>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ceace-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ceace-107">DESCRIPTION</span></span>
<span data-ttu-id="ceace-108">A **New-AzureBatchComputeNodeUser** parancsmag létrehoz egy felhasználói fiókot egy Azure batch számítási csomóponton.</span><span class="sxs-lookup"><span data-stu-id="ceace-108">The **New-AzureBatchComputeNodeUser** cmdlet creates a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="ceace-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ceace-109">EXAMPLES</span></span>

### <span data-ttu-id="ceace-110">Példa 1: rendszergazdai hitelesítő adatokkal rendelkező felhasználói fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="ceace-110">Example 1: Create a user account that has administrative credentials</span></span>
```
PS C:\>New-AzureBatchComputeNodeUser -PoolId "MyPool01" -ComputeNodeId "ComputeNode01" -Name "TestUser" -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(7)) -IsAdmin -BatchContext $Context
```

<span data-ttu-id="ceace-111">Ez a parancs létrehoz egy felhasználói fiókot a számítási csomóponton, amely az azonosító ComputeNode01 tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="ceace-111">This command creates a user account on the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="ceace-112">A csomópont az azonosító MyPool01 tartalmazó készletben található.</span><span class="sxs-lookup"><span data-stu-id="ceace-112">The node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="ceace-113">A Felhasználónév tesztfelhasználó, a jelszó jelszó, a fiók hét napon lejár, és a fiók rendszergazdai hitelesítő adatokkal rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="ceace-113">The user name is TestUser, the password is Password, the account expires in seven days, and the account is has administrative credentials.</span></span>

### <span data-ttu-id="ceace-114">2. példa: felhasználói fiók létrehozása számítási csomóponton a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="ceace-114">Example 2: Create a user account on a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchComputeNode "MyPool01" -ComputeNodeId "ComputeNode01" -BatchContext $Context | New-AzureBatchComputeNodeUser -Name "TestUser" -Password "Password" -BatchContext $Context
```

<span data-ttu-id="ceace-115">Ez a parancs a **Get-AzureBatchComputeNode** parancsmag használatával kapja meg a ComputeNode01 nevű számítási csomópontot.</span><span class="sxs-lookup"><span data-stu-id="ceace-115">This command gets the compute node named ComputeNode01 by using the **Get-AzureBatchComputeNode** cmdlet.</span></span>
<span data-ttu-id="ceace-116">Ez a csomópont abban a készletben található, amely az azonosító MyPool01 tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="ceace-116">That node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="ceace-117">A parancs a csővezeték-kezelő segítségével átadja az aktuális parancsmaghoz tartozó csomópontot.</span><span class="sxs-lookup"><span data-stu-id="ceace-117">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ceace-118">A parancs létrehozza azt a felhasználói fiókot, amelynek a felhasználónevét TestUserand a jelszó.</span><span class="sxs-lookup"><span data-stu-id="ceace-118">The command creates a user account that has the user name TestUserand the password Password.</span></span>

## <span data-ttu-id="ceace-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ceace-119">PARAMETERS</span></span>

### <span data-ttu-id="ceace-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ceace-120">-BatchContext</span></span>
<span data-ttu-id="ceace-121">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="ceace-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ceace-122">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ceace-122">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="ceace-123">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="ceace-123">-ComputeNode</span></span>
<span data-ttu-id="ceace-124">A számítási csomópontot **PSComputeNode** objektumként adja meg, amelyen ez a parancsmag felhasználói fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ceace-124">Specifies the compute node, as a **PSComputeNode** object, on which this cmdlet creates a user account.</span></span>

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

### <span data-ttu-id="ceace-125">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="ceace-125">-ComputeNodeId</span></span>
<span data-ttu-id="ceace-126">Annak a számítási csomópontnak az AZONOSÍTÓját adja meg, amelyen ez a parancsmag létrehoz egy felhasználói fiókot.</span><span class="sxs-lookup"><span data-stu-id="ceace-126">Specifies the ID of the compute node on which this cmdlet creates a user account.</span></span>

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

### <span data-ttu-id="ceace-127">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="ceace-127">-ExpiryTime</span></span>
<span data-ttu-id="ceace-128">Az új felhasználói fiók lejárati időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ceace-128">Specifies the expiry time for the new user account.</span></span>

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

### <span data-ttu-id="ceace-129">-IsAdmin</span><span class="sxs-lookup"><span data-stu-id="ceace-129">-IsAdmin</span></span>
<span data-ttu-id="ceace-130">Azt jelzi, hogy a parancsmag olyan felhasználói fiókot hoz létre, amely rendszergazdai hitelesítő adatokkal rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="ceace-130">Indicates that the cmdlet creates a user account that has administrative credentials.</span></span>

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

### <span data-ttu-id="ceace-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ceace-131">-Name</span></span>
<span data-ttu-id="ceace-132">Az új helyi Windows-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ceace-132">Specifies the name of the new local Windows account.</span></span>

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

### <span data-ttu-id="ceace-133">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="ceace-133">-Password</span></span>
<span data-ttu-id="ceace-134">A felhasználói fiók jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ceace-134">Specifies the user account password.</span></span>

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

### <span data-ttu-id="ceace-135">-PoolId</span><span class="sxs-lookup"><span data-stu-id="ceace-135">-PoolId</span></span>
<span data-ttu-id="ceace-136">Annak a készletnek az AZONOSÍTÓját adja meg, amely a felhasználói fiókot létrehozó számítási csomópontot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="ceace-136">Specifies the ID of the pool that contains the compute node on which to create the user account.</span></span>

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

### <span data-ttu-id="ceace-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceace-137">-DefaultProfile</span></span>
<span data-ttu-id="ceace-138">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ceace-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ceace-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceace-139">CommonParameters</span></span>
<span data-ttu-id="ceace-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ceace-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceace-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ceace-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceace-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ceace-142">INPUTS</span></span>

### <span data-ttu-id="ceace-143">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ceace-143">BatchAccountContext</span></span>
<span data-ttu-id="ceace-144">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="ceace-144">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="ceace-145">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="ceace-145">PSComputeNode</span></span>
<span data-ttu-id="ceace-146">A ' ComputeNode ' paraméter az "PSComputeNode" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="ceace-146">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="ceace-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ceace-147">OUTPUTS</span></span>

## <span data-ttu-id="ceace-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ceace-148">NOTES</span></span>

## <span data-ttu-id="ceace-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ceace-149">RELATED LINKS</span></span>

[<span data-ttu-id="ceace-150">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ceace-150">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="ceace-151">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="ceace-151">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="ceace-152">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="ceace-152">Remove-AzureBatchComputeNodeUser</span></span>](./Remove-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="ceace-153">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="ceace-153">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


