---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightgatewaycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
ms.openlocfilehash: f3997247c9a32fa9066e17dff3a09f2bd65a80d5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296303"
---
# <span data-ttu-id="1f334-101">Set-AzHDInsightGatewayCredential</span><span class="sxs-lookup"><span data-stu-id="1f334-101">Set-AzHDInsightGatewayCredential</span></span>

## <span data-ttu-id="1f334-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1f334-102">SYNOPSIS</span></span>
<span data-ttu-id="1f334-103">Az Azure HDInsight-fürtök átjárójának HTTP-hitelesítő adatait állítja be.</span><span class="sxs-lookup"><span data-stu-id="1f334-103">Sets the gateway HTTP credentials of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="1f334-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1f334-104">SYNTAX</span></span>

### <span data-ttu-id="1f334-105">SetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1f334-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightGatewayCredential [-Name] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f334-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f334-106">SetByInputObjectParameterSet</span></span>
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -InputObject <AzureHDInsightCluster> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f334-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f334-107">SetByResourceIdParameterSet</span></span>
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f334-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1f334-108">DESCRIPTION</span></span>
<span data-ttu-id="1f334-109">A **set-AzHDInsightGatewayCredential** parancsmag az Azure HDInsight-fürtök átjárójának hitelesítő adatait állítja be.</span><span class="sxs-lookup"><span data-stu-id="1f334-109">The **Set-AzHDInsightGatewayCredential** cmdlet sets gateway credential of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="1f334-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1f334-110">EXAMPLES</span></span>

### <span data-ttu-id="1f334-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1f334-111">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Set-AzHDInsightGatewayCredential `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="1f334-112">Ez a parancs az átjáró hitelesítő adatait a-Hadoop-001 nevű név paraméteres beállítással állítja be.</span><span class="sxs-lookup"><span data-stu-id="1f334-112">This command sets gateway credential of the cluster named your-hadoop-001 by name parameter set.</span></span>

### <span data-ttu-id="1f334-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="1f334-113">Example 2</span></span>
```powershell
PS C:\> Set-AzHDInsightGatewayCredential `
            -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.HDInsight/clusters/your-hadoop-001" `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="1f334-114">Ez a parancs az átjáró hitelesítő adatait a-Hadoop-001 nevű ResourceId paraméterrel állítja be.</span><span class="sxs-lookup"><span data-stu-id="1f334-114">This command sets gateway credential of the cluster named your-hadoop-001 by ResourceId parameter set.</span></span>

### <span data-ttu-id="1f334-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="1f334-115">Example 3</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Get-AzHDInsightCluster -ClusterName $clusterName | Set-AzHDInsightGatewayCredential `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="1f334-116">Ez a parancs az átjáró hitelesítő adatait a-Hadoop-001 nevű InputObject paraméterrel állítja be.</span><span class="sxs-lookup"><span data-stu-id="1f334-116">This command sets gateway credential of the cluster named your-hadoop-001 by InputObject parameter set.</span></span>

## <span data-ttu-id="1f334-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1f334-117">PARAMETERS</span></span>

### <span data-ttu-id="1f334-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f334-118">-AsJob</span></span>
<span data-ttu-id="1f334-119">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="1f334-119">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="1f334-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f334-120">-DefaultProfile</span></span>
<span data-ttu-id="1f334-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1f334-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f334-122">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="1f334-122">-HttpCredential</span></span>
<span data-ttu-id="1f334-123">Beadja vagy beállítja a fürt felhasználójának felhasználónevét.</span><span class="sxs-lookup"><span data-stu-id="1f334-123">Gets or sets the login for the cluster's user.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f334-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f334-124">-InputObject</span></span>
<span data-ttu-id="1f334-125">A beviteli objektum beolvasása vagy megadása</span><span class="sxs-lookup"><span data-stu-id="1f334-125">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f334-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1f334-126">-Name</span></span>
<span data-ttu-id="1f334-127">A fürt nevének beolvasása vagy megadására szolgáló beállítás.</span><span class="sxs-lookup"><span data-stu-id="1f334-127">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f334-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f334-128">-ResourceGroupName</span></span>
<span data-ttu-id="1f334-129">Az erőforráscsoport nevének beolvasása vagy megadására szolgáló parancs.</span><span class="sxs-lookup"><span data-stu-id="1f334-129">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f334-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f334-130">-ResourceId</span></span>
<span data-ttu-id="1f334-131">Az erőforrás azonosítóját kapja vagy állítja be.</span><span class="sxs-lookup"><span data-stu-id="1f334-131">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f334-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1f334-132">-Confirm</span></span>
<span data-ttu-id="1f334-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1f334-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f334-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f334-134">-WhatIf</span></span>
<span data-ttu-id="1f334-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1f334-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f334-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1f334-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f334-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f334-137">CommonParameters</span></span>
<span data-ttu-id="1f334-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1f334-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f334-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1f334-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f334-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f334-140">INPUTS</span></span>

### <span data-ttu-id="1f334-141">Nincs</span><span class="sxs-lookup"><span data-stu-id="1f334-141">None</span></span>

## <span data-ttu-id="1f334-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f334-142">OUTPUTS</span></span>

### <span data-ttu-id="1f334-143">Microsoft. Azure. Command. HDInsight. models. Management. AzureHDInsightGatewaySettings</span><span class="sxs-lookup"><span data-stu-id="1f334-143">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightGatewaySettings</span></span>

## <span data-ttu-id="1f334-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1f334-144">NOTES</span></span>

## <span data-ttu-id="1f334-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1f334-145">RELATED LINKS</span></span>
