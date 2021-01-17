---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedCluster.md
ms.openlocfilehash: 4636dc8f8c8efdf9dae5f7d2094fd3432528f043
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339845"
---
# <span data-ttu-id="27890-101">Set-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="27890-101">Set-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="27890-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27890-102">SYNOPSIS</span></span>
<span data-ttu-id="27890-103">A fürterőforrás tulajdonságainak beállítása</span><span class="sxs-lookup"><span data-stu-id="27890-103">Set cluster resource properties.</span></span>

## <span data-ttu-id="27890-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="27890-104">SYNTAX</span></span>

### <span data-ttu-id="27890-105">ByObj (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="27890-105">ByObj (Default)</span></span>
```
Set-AzServiceFabricManagedCluster [-InputObject] <PSManagedCluster> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27890-106">WithPramsByName</span><span class="sxs-lookup"><span data-stu-id="27890-106">WithPramsByName</span></span>
```
Set-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-HttpGatewayConnectionPort <Int32>]
 [-ClientConnectionPort <Int32>] [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27890-107">ByNameById</span><span class="sxs-lookup"><span data-stu-id="27890-107">ByNameById</span></span>
```
Set-AzServiceFabricManagedCluster [-ResourceId] <String> [-UpgradeMode <ClusterUpgradeMode>]
 [-CodeVersion <String>] [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>]
 [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27890-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="27890-108">DESCRIPTION</span></span>
<span data-ttu-id="27890-109">A fürterőforrás tulajdonságainak beállítása</span><span class="sxs-lookup"><span data-stu-id="27890-109">Set cluster resource properties.</span></span>

## <span data-ttu-id="27890-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="27890-110">EXAMPLES</span></span>

### <span data-ttu-id="27890-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="27890-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Update-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName -DnsName testnewdns -ClientConnectionPort 50000 -Verbose
```

<span data-ttu-id="27890-112">Frissítse a fürt DNS-nevét és ügyfélkapcsolati portját.</span><span class="sxs-lookup"><span data-stu-id="27890-112">Update dns name and client connection port for the cluster.</span></span>

### <span data-ttu-id="27890-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="27890-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster.DnsName = "testnewdns"
$cluster.ClientConnectionPort = 50000
$cluster | Set-AzServiceFabricManagedCluster
```

<span data-ttu-id="27890-114">Frissítse a dns nevét és az ügyfélkapcsolat portját a fürthöz pipázással.</span><span class="sxs-lookup"><span data-stu-id="27890-114">Update dns name and client connection port for the cluster, with piping.</span></span>

## <span data-ttu-id="27890-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27890-115">PARAMETERS</span></span>

### <span data-ttu-id="27890-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27890-116">-AsJob</span></span>
<span data-ttu-id="27890-117">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="27890-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="27890-118">-ClientConnectionPort</span><span class="sxs-lookup"><span data-stu-id="27890-118">-ClientConnectionPort</span></span>
<span data-ttu-id="27890-119">A fürthöz való ügyfélkapcsolatok portja.</span><span class="sxs-lookup"><span data-stu-id="27890-119">Port used for client connections to the cluster.</span></span> <span data-ttu-id="27890-120">Alapértelmezett érték: 19000.</span><span class="sxs-lookup"><span data-stu-id="27890-120">Default: 19000.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27890-121">-CodeVersion</span><span class="sxs-lookup"><span data-stu-id="27890-121">-CodeVersion</span></span>
<span data-ttu-id="27890-122">Fürtkód verziója.</span><span class="sxs-lookup"><span data-stu-id="27890-122">Cluster code version.</span></span> <span data-ttu-id="27890-123">Csak akkor használja, ha a frissítési mód manuális.</span><span class="sxs-lookup"><span data-stu-id="27890-123">Only use if upgrade mode is Manual.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27890-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27890-124">-DefaultProfile</span></span>
<span data-ttu-id="27890-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="27890-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27890-126">-DnsName</span><span class="sxs-lookup"><span data-stu-id="27890-126">-DnsName</span></span>
<span data-ttu-id="27890-127">A fürt DNS-neve.</span><span class="sxs-lookup"><span data-stu-id="27890-127">Cluster's dns name.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27890-128">-HttpGatewayConnectionPort</span><span class="sxs-lookup"><span data-stu-id="27890-128">-HttpGatewayConnectionPort</span></span>
<span data-ttu-id="27890-129">A fürt http-kapcsolataihoz használt port.</span><span class="sxs-lookup"><span data-stu-id="27890-129">Port used for http connections to the cluster.</span></span> <span data-ttu-id="27890-130">Alapértelmezett érték: 19080.</span><span class="sxs-lookup"><span data-stu-id="27890-130">Default: 19080.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27890-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27890-131">-InputObject</span></span>
<span data-ttu-id="27890-132">Felügyelt fürterőforrás</span><span class="sxs-lookup"><span data-stu-id="27890-132">Managed Cluster resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27890-133">-Name</span><span class="sxs-lookup"><span data-stu-id="27890-133">-Name</span></span>
<span data-ttu-id="27890-134">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="27890-134">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27890-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27890-135">-ResourceGroupName</span></span>
<span data-ttu-id="27890-136">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="27890-136">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27890-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27890-137">-ResourceId</span></span>
<span data-ttu-id="27890-138">Felügyelt fürt erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="27890-138">Managed Cluster resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27890-139">-ReverseProxyEndpointPort</span><span class="sxs-lookup"><span data-stu-id="27890-139">-ReverseProxyEndpointPort</span></span>
<span data-ttu-id="27890-140">A fordított proxy által használt végpont.</span><span class="sxs-lookup"><span data-stu-id="27890-140">Endpoint used by reverse proxy.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27890-141">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="27890-141">-UpgradeMode</span></span>
<span data-ttu-id="27890-142">Fürtkód verziófrissítési módja.</span><span class="sxs-lookup"><span data-stu-id="27890-142">Cluster code version upgrade mode.</span></span> <span data-ttu-id="27890-143">Automatikus vagy manuális.</span><span class="sxs-lookup"><span data-stu-id="27890-143">Automatic or Manual.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode]
Parameter Sets: WithPramsByName, ByNameById
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27890-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27890-144">-Confirm</span></span>
<span data-ttu-id="27890-145">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="27890-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27890-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27890-146">-WhatIf</span></span>
<span data-ttu-id="27890-147">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="27890-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="27890-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="27890-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27890-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27890-149">CommonParameters</span></span>
<span data-ttu-id="27890-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27890-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27890-151">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27890-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27890-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="27890-152">INPUTS</span></span>

### <span data-ttu-id="27890-153">System.String</span><span class="sxs-lookup"><span data-stu-id="27890-153">System.String</span></span>

## <span data-ttu-id="27890-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="27890-154">OUTPUTS</span></span>

### <span data-ttu-id="27890-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="27890-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="27890-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="27890-156">NOTES</span></span>

## <span data-ttu-id="27890-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="27890-157">RELATED LINKS</span></span>
