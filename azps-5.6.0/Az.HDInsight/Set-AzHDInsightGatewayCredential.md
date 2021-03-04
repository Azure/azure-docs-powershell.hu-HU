---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/set-azhdinsightgatewaycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
ms.openlocfilehash: e864e963e91df9599642c763a151325dd68d65a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935754"
---
# <span data-ttu-id="87919-101">Set-AzHDInsightGatewayCredential</span><span class="sxs-lookup"><span data-stu-id="87919-101">Set-AzHDInsightGatewayCredential</span></span>

## <span data-ttu-id="87919-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87919-102">SYNOPSIS</span></span>
<span data-ttu-id="87919-103">Beállítja egy Azure HDInsight-fürt átjáró HTTP-hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="87919-103">Sets the gateway HTTP credentials of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="87919-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="87919-104">SYNTAX</span></span>

### <span data-ttu-id="87919-105">SetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="87919-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightGatewayCredential [-Name] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="87919-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="87919-106">SetByInputObjectParameterSet</span></span>
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -InputObject <AzureHDInsightCluster> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="87919-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="87919-107">SetByResourceIdParameterSet</span></span>
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87919-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="87919-108">DESCRIPTION</span></span>
<span data-ttu-id="87919-109">A **Set-AzHDInsightGatewayCredential** parancsmag beállítja egy Azure HDInsight-fürt átjáró hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="87919-109">The **Set-AzHDInsightGatewayCredential** cmdlet sets gateway credential of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="87919-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="87919-110">EXAMPLES</span></span>

### <span data-ttu-id="87919-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="87919-111">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Set-AzHDInsightGatewayCredential `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="87919-112">Ez a parancs beállítja az átjáró hitelesítő adatait a "-hadoop-001" nevű fürthöz név paraméterkészlet szerint.</span><span class="sxs-lookup"><span data-stu-id="87919-112">This command sets gateway credential of the cluster named your-hadoop-001 by name parameter set.</span></span>

### <span data-ttu-id="87919-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="87919-113">Example 2</span></span>
```powershell
PS C:\> Set-AzHDInsightGatewayCredential `
            -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.HDInsight/clusters/your-hadoop-001" `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="87919-114">Ez a parancs a ResourceId paraméterkészlet által megadott" nevű fürt átjárói hitelesítő adatait állítja be.</span><span class="sxs-lookup"><span data-stu-id="87919-114">This command sets gateway credential of the cluster named your-hadoop-001 by ResourceId parameter set.</span></span>

### <span data-ttu-id="87919-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="87919-115">Example 3</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Get-AzHDInsightCluster -ClusterName $clusterName | Set-AzHDInsightGatewayCredential `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="87919-116">Ez a parancs az InputObject paraméterkészlettel beállítja a saját-hadoop-001 nevű fürt átjárói hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="87919-116">This command sets gateway credential of the cluster named your-hadoop-001 by InputObject parameter set.</span></span>

## <span data-ttu-id="87919-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87919-117">PARAMETERS</span></span>

### <span data-ttu-id="87919-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="87919-118">-AsJob</span></span>
<span data-ttu-id="87919-119">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="87919-119">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="87919-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87919-120">-DefaultProfile</span></span>
<span data-ttu-id="87919-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="87919-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87919-122">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="87919-122">-HttpCredential</span></span>
<span data-ttu-id="87919-123">Beállítja vagy beállítja a bejelentkezést a fürt felhasználója számára.</span><span class="sxs-lookup"><span data-stu-id="87919-123">Gets or sets the login for the cluster's user.</span></span>

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

### <span data-ttu-id="87919-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87919-124">-InputObject</span></span>
<span data-ttu-id="87919-125">Beállítja vagy beállítja a bemeneti objektumot.</span><span class="sxs-lookup"><span data-stu-id="87919-125">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="87919-126">-Name</span><span class="sxs-lookup"><span data-stu-id="87919-126">-Name</span></span>
<span data-ttu-id="87919-127">Beállítja vagy beállítja a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="87919-127">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="87919-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87919-128">-ResourceGroupName</span></span>
<span data-ttu-id="87919-129">Beállítja vagy beállítja az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="87919-129">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="87919-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87919-130">-ResourceId</span></span>
<span data-ttu-id="87919-131">Beállítja vagy beállítja az erőforrás-azonosítót.</span><span class="sxs-lookup"><span data-stu-id="87919-131">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="87919-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="87919-132">-Confirm</span></span>
<span data-ttu-id="87919-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="87919-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87919-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87919-134">-WhatIf</span></span>
<span data-ttu-id="87919-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="87919-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="87919-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="87919-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87919-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87919-137">CommonParameters</span></span>
<span data-ttu-id="87919-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87919-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87919-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="87919-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87919-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="87919-140">INPUTS</span></span>

### <span data-ttu-id="87919-141">Nincs</span><span class="sxs-lookup"><span data-stu-id="87919-141">None</span></span>

## <span data-ttu-id="87919-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="87919-142">OUTPUTS</span></span>

### <span data-ttu-id="87919-143">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightGatewaySettings</span><span class="sxs-lookup"><span data-stu-id="87919-143">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightGatewaySettings</span></span>

## <span data-ttu-id="87919-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="87919-144">NOTES</span></span>

## <span data-ttu-id="87919-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="87919-145">RELATED LINKS</span></span>
