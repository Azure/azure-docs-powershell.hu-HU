---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/set-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Set-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Set-AzureRmMlOpCluster.md
ms.openlocfilehash: 142dd983b00b578f47e2c1f2eebcbd0686614430
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680411"
---
# <span data-ttu-id="2e412-101">Set-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="2e412-101">Set-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="2e412-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2e412-102">SYNOPSIS</span></span>
<span data-ttu-id="2e412-103">Beállítja egy operationalization-fürt tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="2e412-103">Sets the properties of an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e412-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2e412-104">SYNTAX</span></span>

### <span data-ttu-id="2e412-105">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="2e412-105">SetByInputObject</span></span>
```
Set-AzureRmMlOpCluster -InputObject <PSOperationalizationCluster> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="2e412-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2e412-106">SetByResourceId</span></span>
```
Set-AzureRmMlOpCluster -ResourceId <String> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="2e412-107">SetByIndividualParameters</span><span class="sxs-lookup"><span data-stu-id="2e412-107">SetByIndividualParameters</span></span>
```
Set-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="2e412-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2e412-108">DESCRIPTION</span></span>
<span data-ttu-id="2e412-109">Egy operationalization-fürt összes tulajdonságát beállítja.</span><span class="sxs-lookup"><span data-stu-id="2e412-109">Sets all the properties of an operationalization cluster.</span></span> <span data-ttu-id="2e412-110">Mivel a cluster objektum használatakor minden tulajdonságot beállítja, a teljes mértékben érvényes bemeneti objektumot át kell adni.</span><span class="sxs-lookup"><span data-stu-id="2e412-110">Since it sets all the properties when using a cluster object a fully valid input object must be passed.</span></span> <span data-ttu-id="2e412-111">A program figyelmen kívül hagyja a csak olvasható tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="2e412-111">Read-only properties will be ignored.</span></span> <span data-ttu-id="2e412-112">Csak néhány tulajdonság frissíthető, mint a paraméterek halmaza.</span><span class="sxs-lookup"><span data-stu-id="2e412-112">Only some properties are currently updatable, as shown in the parameter sets.</span></span>

## <span data-ttu-id="2e412-113">Példák</span><span class="sxs-lookup"><span data-stu-id="2e412-113">EXAMPLES</span></span>

### <span data-ttu-id="2e412-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2e412-114">Example 1</span></span>
<span data-ttu-id="2e412-115">Fürt frissítése az egyes paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="2e412-115">Update a cluster using individual parameters.</span></span>
```
PS C:\> Set-AzureRmMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster -AgentCount 5
```

### <span data-ttu-id="2e412-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="2e412-116">Example 2</span></span>
<span data-ttu-id="2e412-117">Fürt frissítése beviteli objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="2e412-117">Update a cluster using an input object.</span></span>
```
PS C:\> $cluster = Get-AzureRmMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster
PS C:\> $cluster.ContainerService.AgentCount = 5
PS C:\> Set-AzureRmMlOpCluster -InputObject $cluster
```

## <span data-ttu-id="2e412-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2e412-118">PARAMETERS</span></span>

### <span data-ttu-id="2e412-119">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="2e412-119">-AgentCount</span></span>
<span data-ttu-id="2e412-120">Az ügynök csomópontjainak száma az ACS-fürtben.</span><span class="sxs-lookup"><span data-stu-id="2e412-120">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByInputObject, SetByResourceId, SetByIndividualParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e412-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e412-121">-DefaultProfile</span></span>
<span data-ttu-id="2e412-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2e412-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e412-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e412-123">-InputObject</span></span>
<span data-ttu-id="2e412-124">A operationalization-fürt tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="2e412-124">The operationalization cluster properties.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: SetByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e412-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2e412-125">-Name</span></span>
<span data-ttu-id="2e412-126">A operationalization-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="2e412-126">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: SetByIndividualParameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e412-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e412-127">-ResourceGroupName</span></span>
<span data-ttu-id="2e412-128">A operationalization-fürt erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2e412-128">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: SetByIndividualParameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e412-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e412-129">-ResourceId</span></span>
<span data-ttu-id="2e412-130">Az Azure Resource id a operationalization-fürthöz.</span><span class="sxs-lookup"><span data-stu-id="2e412-130">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e412-131">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="2e412-131">-SslCertificate</span></span>
<span data-ttu-id="2e412-132">Az SSL-tanúsítványok PEM formátumban jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="2e412-132">The SSL certificate data in PEM format.</span></span>

```yaml
Type: String
Parameter Sets: SetByInputObject, SetByResourceId, SetByIndividualParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e412-133">-SslCName</span><span class="sxs-lookup"><span data-stu-id="2e412-133">-SslCName</span></span>
<span data-ttu-id="2e412-134">Az SSL-tanúsítvány CName rekordja.</span><span class="sxs-lookup"><span data-stu-id="2e412-134">The CName for the SSL certificate.</span></span>

```yaml
Type: String
Parameter Sets: SetByInputObject, SetByResourceId, SetByIndividualParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e412-135">-SslKey</span><span class="sxs-lookup"><span data-stu-id="2e412-135">-SslKey</span></span>
<span data-ttu-id="2e412-136">Az SSL-kulcs adatainak PEM formátumban való megjelenítése.</span><span class="sxs-lookup"><span data-stu-id="2e412-136">The SSL key data in PEM format.</span></span>

```yaml
Type: String
Parameter Sets: SetByInputObject, SetByResourceId, SetByIndividualParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e412-137">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="2e412-137">-SslStatus</span></span>
<span data-ttu-id="2e412-138">SSL-állapot</span><span class="sxs-lookup"><span data-stu-id="2e412-138">SSL status.</span></span>
<span data-ttu-id="2e412-139">A lehetséges értékek "engedélyezve" és "Letiltva".</span><span class="sxs-lookup"><span data-stu-id="2e412-139">Possible values are 'Enabled' and 'Disabled'.</span></span>

```yaml
Type: String
Parameter Sets: SetByInputObject, SetByResourceId, SetByIndividualParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e412-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2e412-140">-Confirm</span></span>
<span data-ttu-id="2e412-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2e412-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e412-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e412-142">-WhatIf</span></span>
<span data-ttu-id="2e412-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2e412-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e412-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2e412-144">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="2e412-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e412-145">INPUTS</span></span>

### <span data-ttu-id="2e412-146">Microsoft. Azure. Command. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="2e412-146">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
### <span data-ttu-id="2e412-147">System. String</span><span class="sxs-lookup"><span data-stu-id="2e412-147">System.String</span></span>
### <span data-ttu-id="2e412-148">System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="2e412-148">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>


## <span data-ttu-id="2e412-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e412-149">OUTPUTS</span></span>

### <span data-ttu-id="2e412-150">Microsoft. Azure. Command. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="2e412-150">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>


## <span data-ttu-id="2e412-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2e412-151">NOTES</span></span>

## <span data-ttu-id="2e412-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e412-152">RELATED LINKS</span></span>

