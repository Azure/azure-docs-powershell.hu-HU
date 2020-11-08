---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedCluster.md
ms.openlocfilehash: 4636dc8f8c8efdf9dae5f7d2094fd3432528f043
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187021"
---
# <span data-ttu-id="b43c9-101">Set-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="b43c9-101">Set-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="b43c9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b43c9-102">SYNOPSIS</span></span>
<span data-ttu-id="b43c9-103">A cluster resource tulajdonság beállítása</span><span class="sxs-lookup"><span data-stu-id="b43c9-103">Set cluster resource properties.</span></span>

## <span data-ttu-id="b43c9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b43c9-104">SYNTAX</span></span>

### <span data-ttu-id="b43c9-105">ByObj (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b43c9-105">ByObj (Default)</span></span>
```
Set-AzServiceFabricManagedCluster [-InputObject] <PSManagedCluster> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b43c9-106">WithPramsByName</span><span class="sxs-lookup"><span data-stu-id="b43c9-106">WithPramsByName</span></span>
```
Set-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-HttpGatewayConnectionPort <Int32>]
 [-ClientConnectionPort <Int32>] [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b43c9-107">ByNameById</span><span class="sxs-lookup"><span data-stu-id="b43c9-107">ByNameById</span></span>
```
Set-AzServiceFabricManagedCluster [-ResourceId] <String> [-UpgradeMode <ClusterUpgradeMode>]
 [-CodeVersion <String>] [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>]
 [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b43c9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b43c9-108">DESCRIPTION</span></span>
<span data-ttu-id="b43c9-109">A cluster resource tulajdonság beállítása</span><span class="sxs-lookup"><span data-stu-id="b43c9-109">Set cluster resource properties.</span></span>

## <span data-ttu-id="b43c9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b43c9-110">EXAMPLES</span></span>

### <span data-ttu-id="b43c9-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b43c9-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Update-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName -DnsName testnewdns -ClientConnectionPort 50000 -Verbose
```

<span data-ttu-id="b43c9-112">Frissítse a fürt DNS-nevét és ügyfél-kapcsolati portját.</span><span class="sxs-lookup"><span data-stu-id="b43c9-112">Update dns name and client connection port for the cluster.</span></span>

### <span data-ttu-id="b43c9-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="b43c9-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster.DnsName = "testnewdns"
$cluster.ClientConnectionPort = 50000
$cluster | Set-AzServiceFabricManagedCluster
```

<span data-ttu-id="b43c9-114">Frissítse a fürt DNS-nevét és ügyfél-kapcsolati portját a csövekkel.</span><span class="sxs-lookup"><span data-stu-id="b43c9-114">Update dns name and client connection port for the cluster, with piping.</span></span>

## <span data-ttu-id="b43c9-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b43c9-115">PARAMETERS</span></span>

### <span data-ttu-id="b43c9-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b43c9-116">-AsJob</span></span>
<span data-ttu-id="b43c9-117">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="b43c9-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b43c9-118">-ClientConnectionPort</span><span class="sxs-lookup"><span data-stu-id="b43c9-118">-ClientConnectionPort</span></span>
<span data-ttu-id="b43c9-119">A fürthöz való ügyfél-kapcsolatokhoz használt port.</span><span class="sxs-lookup"><span data-stu-id="b43c9-119">Port used for client connections to the cluster.</span></span> <span data-ttu-id="b43c9-120">Alapértelmezett: 19000.</span><span class="sxs-lookup"><span data-stu-id="b43c9-120">Default: 19000.</span></span>

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

### <span data-ttu-id="b43c9-121">-CodeVersion</span><span class="sxs-lookup"><span data-stu-id="b43c9-121">-CodeVersion</span></span>
<span data-ttu-id="b43c9-122">Szektorcsoport-kód verziója.</span><span class="sxs-lookup"><span data-stu-id="b43c9-122">Cluster code version.</span></span> <span data-ttu-id="b43c9-123">Csak akkor használja, ha a frissítési mód kézi.</span><span class="sxs-lookup"><span data-stu-id="b43c9-123">Only use if upgrade mode is Manual.</span></span>

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

### <span data-ttu-id="b43c9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b43c9-124">-DefaultProfile</span></span>
<span data-ttu-id="b43c9-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b43c9-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b43c9-126">-DnsName</span><span class="sxs-lookup"><span data-stu-id="b43c9-126">-DnsName</span></span>
<span data-ttu-id="b43c9-127">A fürt DNS-neve.</span><span class="sxs-lookup"><span data-stu-id="b43c9-127">Cluster's dns name.</span></span>

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

### <span data-ttu-id="b43c9-128">-HttpGatewayConnectionPort</span><span class="sxs-lookup"><span data-stu-id="b43c9-128">-HttpGatewayConnectionPort</span></span>
<span data-ttu-id="b43c9-129">A fürthöz való http-kapcsolatokhoz használt port.</span><span class="sxs-lookup"><span data-stu-id="b43c9-129">Port used for http connections to the cluster.</span></span> <span data-ttu-id="b43c9-130">Alapértelmezett: 19080.</span><span class="sxs-lookup"><span data-stu-id="b43c9-130">Default: 19080.</span></span>

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

### <span data-ttu-id="b43c9-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b43c9-131">-InputObject</span></span>
<span data-ttu-id="b43c9-132">Felügyelt cluster resource</span><span class="sxs-lookup"><span data-stu-id="b43c9-132">Managed Cluster resource</span></span>

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

### <span data-ttu-id="b43c9-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b43c9-133">-Name</span></span>
<span data-ttu-id="b43c9-134">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="b43c9-134">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="b43c9-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b43c9-135">-ResourceGroupName</span></span>
<span data-ttu-id="b43c9-136">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="b43c9-136">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="b43c9-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b43c9-137">-ResourceId</span></span>
<span data-ttu-id="b43c9-138">Felügyelt cluster resource azonosító</span><span class="sxs-lookup"><span data-stu-id="b43c9-138">Managed Cluster resource id</span></span>

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

### <span data-ttu-id="b43c9-139">-ReverseProxyEndpointPort</span><span class="sxs-lookup"><span data-stu-id="b43c9-139">-ReverseProxyEndpointPort</span></span>
<span data-ttu-id="b43c9-140">A fordított proxy által használt végpont.</span><span class="sxs-lookup"><span data-stu-id="b43c9-140">Endpoint used by reverse proxy.</span></span>

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

### <span data-ttu-id="b43c9-141">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="b43c9-141">-UpgradeMode</span></span>
<span data-ttu-id="b43c9-142">A cluster Code verziófrissítési módja.</span><span class="sxs-lookup"><span data-stu-id="b43c9-142">Cluster code version upgrade mode.</span></span> <span data-ttu-id="b43c9-143">Automatikus vagy manuális.</span><span class="sxs-lookup"><span data-stu-id="b43c9-143">Automatic or Manual.</span></span>

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

### <span data-ttu-id="b43c9-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b43c9-144">-Confirm</span></span>
<span data-ttu-id="b43c9-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b43c9-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b43c9-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b43c9-146">-WhatIf</span></span>
<span data-ttu-id="b43c9-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b43c9-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b43c9-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b43c9-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b43c9-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b43c9-149">CommonParameters</span></span>
<span data-ttu-id="b43c9-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b43c9-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b43c9-151">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b43c9-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b43c9-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b43c9-152">INPUTS</span></span>

### <span data-ttu-id="b43c9-153">System. String</span><span class="sxs-lookup"><span data-stu-id="b43c9-153">System.String</span></span>

## <span data-ttu-id="b43c9-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b43c9-154">OUTPUTS</span></span>

### <span data-ttu-id="b43c9-155">Microsoft. Azure. Command. ServiceFabric. models. PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="b43c9-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="b43c9-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b43c9-156">NOTES</span></span>

## <span data-ttu-id="b43c9-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b43c9-157">RELATED LINKS</span></span>