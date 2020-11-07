---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/set-azmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Set-AzMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Set-AzMlOpCluster.md
ms.openlocfilehash: 833b3456cd39e4589ceaf37e0c86fd654c250ddc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665957"
---
# <span data-ttu-id="7ea31-101">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="7ea31-101">Set-AzMlOpCluster</span></span>

## <span data-ttu-id="7ea31-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7ea31-102">SYNOPSIS</span></span>
<span data-ttu-id="7ea31-103">Beállítja egy operationalization-fürt tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="7ea31-103">Sets the properties of an operationalization cluster.</span></span>

## <span data-ttu-id="7ea31-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7ea31-104">SYNTAX</span></span>

### <span data-ttu-id="7ea31-105">SetByIndividualParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7ea31-105">SetByIndividualParameters (Default)</span></span>
```
Set-AzMlOpCluster -ResourceGroupName <String> -Name <String> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ea31-106">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="7ea31-106">SetByInputObject</span></span>
```
Set-AzMlOpCluster -InputObject <PSOperationalizationCluster> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ea31-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7ea31-107">SetByResourceId</span></span>
```
Set-AzMlOpCluster -ResourceId <String> [-AgentCount <Int32>] [-SslStatus <String>] [-SslCertificate <String>]
 [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7ea31-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7ea31-108">DESCRIPTION</span></span>
<span data-ttu-id="7ea31-109">Egy operationalization-fürt összes tulajdonságát beállítja.</span><span class="sxs-lookup"><span data-stu-id="7ea31-109">Sets all the properties of an operationalization cluster.</span></span> <span data-ttu-id="7ea31-110">Mivel a cluster objektum használatakor minden tulajdonságot beállítja, a teljes mértékben érvényes bemeneti objektumot át kell adni.</span><span class="sxs-lookup"><span data-stu-id="7ea31-110">Since it sets all the properties when using a cluster object a fully valid input object must be passed.</span></span> <span data-ttu-id="7ea31-111">A program figyelmen kívül hagyja a csak olvasható tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="7ea31-111">Read-only properties will be ignored.</span></span> <span data-ttu-id="7ea31-112">Csak néhány tulajdonság frissíthető, mint a paraméterek halmaza.</span><span class="sxs-lookup"><span data-stu-id="7ea31-112">Only some properties are currently updatable, as shown in the parameter sets.</span></span>

## <span data-ttu-id="7ea31-113">Példák</span><span class="sxs-lookup"><span data-stu-id="7ea31-113">EXAMPLES</span></span>

### <span data-ttu-id="7ea31-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7ea31-114">Example 1</span></span>
<span data-ttu-id="7ea31-115">Fürt frissítése az egyes paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="7ea31-115">Update a cluster using individual parameters.</span></span>

```
PS C:\> Set-AzMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster -AgentCount 5
```

### <span data-ttu-id="7ea31-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="7ea31-116">Example 2</span></span>
<span data-ttu-id="7ea31-117">Fürt frissítése beviteli objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="7ea31-117">Update a cluster using an input object.</span></span>

```
PS C:\> $cluster = Get-AzMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster
PS C:\> $cluster.ContainerService.AgentCount = 5
PS C:\> Set-AzMlOpCluster -InputObject $cluster
```

## <span data-ttu-id="7ea31-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7ea31-118">PARAMETERS</span></span>

### <span data-ttu-id="7ea31-119">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="7ea31-119">-AgentCount</span></span>
<span data-ttu-id="7ea31-120">Az ügynök csomópontjainak száma az ACS-fürtben.</span><span class="sxs-lookup"><span data-stu-id="7ea31-120">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ea31-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ea31-121">-DefaultProfile</span></span>
<span data-ttu-id="7ea31-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7ea31-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ea31-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ea31-123">-InputObject</span></span>
<span data-ttu-id="7ea31-124">A operationalization-fürt tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="7ea31-124">The operationalization cluster properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: SetByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ea31-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7ea31-125">-Name</span></span>
<span data-ttu-id="7ea31-126">A operationalization-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="7ea31-126">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea31-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ea31-127">-ResourceGroupName</span></span>
<span data-ttu-id="7ea31-128">A operationalization-fürt erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7ea31-128">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea31-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ea31-129">-ResourceId</span></span>
<span data-ttu-id="7ea31-130">Az Azure Resource id a operationalization-fürthöz.</span><span class="sxs-lookup"><span data-stu-id="7ea31-130">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ea31-131">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="7ea31-131">-SslCertificate</span></span>
<span data-ttu-id="7ea31-132">Az SSL-tanúsítványok PEM formátumban jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="7ea31-132">The SSL certificate data in PEM format.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ea31-133">-SslCName</span><span class="sxs-lookup"><span data-stu-id="7ea31-133">-SslCName</span></span>
<span data-ttu-id="7ea31-134">Az SSL-tanúsítvány CName rekordja.</span><span class="sxs-lookup"><span data-stu-id="7ea31-134">The CName for the SSL certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ea31-135">-SslKey</span><span class="sxs-lookup"><span data-stu-id="7ea31-135">-SslKey</span></span>
<span data-ttu-id="7ea31-136">Az SSL-kulcs adatainak PEM formátumban való megjelenítése.</span><span class="sxs-lookup"><span data-stu-id="7ea31-136">The SSL key data in PEM format.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ea31-137">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="7ea31-137">-SslStatus</span></span>
<span data-ttu-id="7ea31-138">SSL-állapot</span><span class="sxs-lookup"><span data-stu-id="7ea31-138">SSL status.</span></span>
<span data-ttu-id="7ea31-139">A lehetséges értékek "engedélyezve" és "Letiltva".</span><span class="sxs-lookup"><span data-stu-id="7ea31-139">Possible values are 'Enabled' and 'Disabled'.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ea31-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7ea31-140">-Confirm</span></span>
<span data-ttu-id="7ea31-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7ea31-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea31-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ea31-142">-WhatIf</span></span>
<span data-ttu-id="7ea31-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7ea31-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ea31-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7ea31-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea31-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ea31-145">CommonParameters</span></span>
<span data-ttu-id="7ea31-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7ea31-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ea31-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ea31-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ea31-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ea31-148">INPUTS</span></span>

### <span data-ttu-id="7ea31-149">Microsoft. Azure. Command. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="7ea31-149">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="7ea31-150">System. String</span><span class="sxs-lookup"><span data-stu-id="7ea31-150">System.String</span></span>

### <span data-ttu-id="7ea31-151">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7ea31-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="7ea31-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ea31-152">OUTPUTS</span></span>

### <span data-ttu-id="7ea31-153">Microsoft. Azure. Command. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="7ea31-153">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="7ea31-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7ea31-154">NOTES</span></span>

## <span data-ttu-id="7ea31-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7ea31-155">RELATED LINKS</span></span>
