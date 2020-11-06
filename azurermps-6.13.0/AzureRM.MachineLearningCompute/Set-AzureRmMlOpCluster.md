---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/set-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Set-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Set-AzureRmMlOpCluster.md
ms.openlocfilehash: cbe72d14eac4864b784f31c4a800db09fc38b042
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495991"
---
# <span data-ttu-id="b088c-101">Set-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="b088c-101">Set-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="b088c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b088c-102">SYNOPSIS</span></span>
<span data-ttu-id="b088c-103">Beállítja egy operationalization-fürt tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="b088c-103">Sets the properties of an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b088c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b088c-104">SYNTAX</span></span>

### <span data-ttu-id="b088c-105">SetByIndividualParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b088c-105">SetByIndividualParameters (Default)</span></span>
```
Set-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b088c-106">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="b088c-106">SetByInputObject</span></span>
```
Set-AzureRmMlOpCluster -InputObject <PSOperationalizationCluster> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b088c-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b088c-107">SetByResourceId</span></span>
```
Set-AzureRmMlOpCluster -ResourceId <String> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b088c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b088c-108">DESCRIPTION</span></span>
<span data-ttu-id="b088c-109">Egy operationalization-fürt összes tulajdonságát beállítja.</span><span class="sxs-lookup"><span data-stu-id="b088c-109">Sets all the properties of an operationalization cluster.</span></span> <span data-ttu-id="b088c-110">Mivel a cluster objektum használatakor minden tulajdonságot beállítja, a teljes mértékben érvényes bemeneti objektumot át kell adni.</span><span class="sxs-lookup"><span data-stu-id="b088c-110">Since it sets all the properties when using a cluster object a fully valid input object must be passed.</span></span> <span data-ttu-id="b088c-111">A program figyelmen kívül hagyja a csak olvasható tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="b088c-111">Read-only properties will be ignored.</span></span> <span data-ttu-id="b088c-112">Csak néhány tulajdonság frissíthető, mint a paraméterek halmaza.</span><span class="sxs-lookup"><span data-stu-id="b088c-112">Only some properties are currently updatable, as shown in the parameter sets.</span></span>

## <span data-ttu-id="b088c-113">Példák</span><span class="sxs-lookup"><span data-stu-id="b088c-113">EXAMPLES</span></span>

### <span data-ttu-id="b088c-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b088c-114">Example 1</span></span>
<span data-ttu-id="b088c-115">Fürt frissítése az egyes paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="b088c-115">Update a cluster using individual parameters.</span></span>

```
PS C:\> Set-AzureRmMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster -AgentCount 5
```

### <span data-ttu-id="b088c-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="b088c-116">Example 2</span></span>
<span data-ttu-id="b088c-117">Fürt frissítése beviteli objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="b088c-117">Update a cluster using an input object.</span></span>

```
PS C:\> $cluster = Get-AzureRmMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster
PS C:\> $cluster.ContainerService.AgentCount = 5
PS C:\> Set-AzureRmMlOpCluster -InputObject $cluster
```

## <span data-ttu-id="b088c-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b088c-118">PARAMETERS</span></span>

### <span data-ttu-id="b088c-119">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="b088c-119">-AgentCount</span></span>
<span data-ttu-id="b088c-120">Az ügynök csomópontjainak száma az ACS-fürtben.</span><span class="sxs-lookup"><span data-stu-id="b088c-120">The number of agent nodes in the ACS cluster.</span></span>

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

### <span data-ttu-id="b088c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b088c-121">-DefaultProfile</span></span>
<span data-ttu-id="b088c-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b088c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b088c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b088c-123">-InputObject</span></span>
<span data-ttu-id="b088c-124">A operationalization-fürt tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="b088c-124">The operationalization cluster properties.</span></span>

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

### <span data-ttu-id="b088c-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b088c-125">-Name</span></span>
<span data-ttu-id="b088c-126">A operationalization-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="b088c-126">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="b088c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b088c-127">-ResourceGroupName</span></span>
<span data-ttu-id="b088c-128">A operationalization-fürt erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b088c-128">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="b088c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b088c-129">-ResourceId</span></span>
<span data-ttu-id="b088c-130">Az Azure Resource id a operationalization-fürthöz.</span><span class="sxs-lookup"><span data-stu-id="b088c-130">The Azure resource id for the operationalization cluster.</span></span>

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

### <span data-ttu-id="b088c-131">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="b088c-131">-SslCertificate</span></span>
<span data-ttu-id="b088c-132">Az SSL-tanúsítványok PEM formátumban jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="b088c-132">The SSL certificate data in PEM format.</span></span>

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

### <span data-ttu-id="b088c-133">-SslCName</span><span class="sxs-lookup"><span data-stu-id="b088c-133">-SslCName</span></span>
<span data-ttu-id="b088c-134">Az SSL-tanúsítvány CName rekordja.</span><span class="sxs-lookup"><span data-stu-id="b088c-134">The CName for the SSL certificate.</span></span>

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

### <span data-ttu-id="b088c-135">-SslKey</span><span class="sxs-lookup"><span data-stu-id="b088c-135">-SslKey</span></span>
<span data-ttu-id="b088c-136">Az SSL-kulcs adatainak PEM formátumban való megjelenítése.</span><span class="sxs-lookup"><span data-stu-id="b088c-136">The SSL key data in PEM format.</span></span>

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

### <span data-ttu-id="b088c-137">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="b088c-137">-SslStatus</span></span>
<span data-ttu-id="b088c-138">SSL-állapot</span><span class="sxs-lookup"><span data-stu-id="b088c-138">SSL status.</span></span>
<span data-ttu-id="b088c-139">A lehetséges értékek "engedélyezve" és "Letiltva".</span><span class="sxs-lookup"><span data-stu-id="b088c-139">Possible values are 'Enabled' and 'Disabled'.</span></span>

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

### <span data-ttu-id="b088c-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b088c-140">-Confirm</span></span>
<span data-ttu-id="b088c-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b088c-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b088c-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b088c-142">-WhatIf</span></span>
<span data-ttu-id="b088c-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b088c-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b088c-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b088c-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b088c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b088c-145">CommonParameters</span></span>
<span data-ttu-id="b088c-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b088c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b088c-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b088c-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b088c-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b088c-148">INPUTS</span></span>

### <span data-ttu-id="b088c-149">Microsoft. Azure. Command. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="b088c-149">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="b088c-150">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b088c-150">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="b088c-151">System. String</span><span class="sxs-lookup"><span data-stu-id="b088c-151">System.String</span></span>

### <span data-ttu-id="b088c-152">System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b088c-152">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="b088c-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b088c-153">OUTPUTS</span></span>

### <span data-ttu-id="b088c-154">Microsoft. Azure. Command. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="b088c-154">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="b088c-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b088c-155">NOTES</span></span>

## <span data-ttu-id="b088c-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b088c-156">RELATED LINKS</span></span>
