---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedCluster.md
ms.openlocfilehash: 9dd54f0f1ca56a8bedf3550e238a4308b519925d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371781"
---
# <span data-ttu-id="0a2ae-101">New-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="0a2ae-101">New-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="0a2ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a2ae-102">SYNOPSIS</span></span>
<span data-ttu-id="0a2ae-103">Hozzon létre új felügyelt fürtöt.</span><span class="sxs-lookup"><span data-stu-id="0a2ae-103">Create new managed cluster.</span></span>

## <span data-ttu-id="0a2ae-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0a2ae-104">SYNTAX</span></span>

### <span data-ttu-id="0a2ae-105">ClientCertByTp (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0a2ae-105">ClientCertByTp (Default)</span></span>
```
New-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-ClientCertIsAdmin]
 -ClientCertThumbprint <String> -AdminPassword <SecureString> [-AdminUserName <String>]
 [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>] [-DnsName <String>]
 [-ReverseProxyEndpointPort <Int32>] [-Sku <ManagedClusterSku>] [-UseTestExtension] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a2ae-106">ClientCertByCn</span><span class="sxs-lookup"><span data-stu-id="0a2ae-106">ClientCertByCn</span></span>
```
New-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-ClientCertIsAdmin]
 -ClientCertCommonName <String> [-ClientCertIssuerThumbprint <String[]>] -AdminPassword <SecureString>
 [-AdminUserName <String>] [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>]
 [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-Sku <ManagedClusterSku>] [-UseTestExtension]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a2ae-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0a2ae-107">DESCRIPTION</span></span>
<span data-ttu-id="0a2ae-108">Ez a parancsmag csomóponttípusok nélküli felügyelt fürterőforrást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0a2ae-108">This cmdlet will create a managed cluster resource without node types.</span></span> <span data-ttu-id="0a2ae-109">A fürt indításához az elsődleges csomóponttípust a [New-AzServiceFabricManagedNodeType](./New-AzServiceFabricManagedNodeType.md)használatával kell hozzáadni.</span><span class="sxs-lookup"><span data-stu-id="0a2ae-109">To bootstrap the cluster A primary node type needs to be added use [New-AzServiceFabricManagedNodeType](./New-AzServiceFabricManagedNodeType.md).</span></span>

## <span data-ttu-id="0a2ae-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0a2ae-110">EXAMPLES</span></span>

### <span data-ttu-id="0a2ae-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="0a2ae-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$password = ConvertTo-SecureString -AsPlainText -Force "testpass1234!@#$"
New-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Location centraluseuap -ClusterName $clusterName -AdminPassword $password -Verbose
```

<span data-ttu-id="0a2ae-112">Ez a parancs létrehoz egy alapértelmezett egyszerű termékváltozatot a fürterőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="0a2ae-112">This command creates a cluster resource with default basic sku.</span></span>

### <span data-ttu-id="0a2ae-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="0a2ae-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$password = ConvertTo-SecureString -AsPlainText -Force "testpass1234!@#$"
New-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Location centraluseuap -ClusterName $clusterName -ClientCertThumbprint XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX -ClientCertIsAdmin -AdminPassword $password -Sku Standard -Verbose
```

<span data-ttu-id="0a2ae-114">Ez a parancs egy kezdeti rendszergazdai ügyfél tanúsítvánnyal és szokásos termékváltozattal létrehozott fürterőforrást hoz létre központi használatra.</span><span class="sxs-lookup"><span data-stu-id="0a2ae-114">This command creates a cluster resource in centraluseuap with an initial admin client certificate and standard sku.</span></span>

## <span data-ttu-id="0a2ae-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a2ae-115">PARAMETERS</span></span>

### <span data-ttu-id="0a2ae-116">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="0a2ae-116">-AdminPassword</span></span>
<span data-ttu-id="0a2ae-117">A virtuális gépekhez használt rendszergazdai jelszó.</span><span class="sxs-lookup"><span data-stu-id="0a2ae-117">Admin password used for the virtual machines.</span></span>

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

### <span data-ttu-id="0a2ae-118">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="0a2ae-118">-AdminUserName</span></span>
<span data-ttu-id="0a2ae-119">A virtuális gépekhez használt rendszergazdai jelszó.</span><span class="sxs-lookup"><span data-stu-id="0a2ae-119">Admin password used for the virtual machines.</span></span>
<span data-ttu-id="0a2ae-120">Alapértelmezett: vmadmin.</span><span class="sxs-lookup"><span data-stu-id="0a2ae-120">Default: vmadmin.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "vmadmin"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a2ae-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a2ae-121">-AsJob</span></span>
<span data-ttu-id="0a2ae-122">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="0a2ae-122">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="0a2ae-123">-ClientCertCommonName</span><span class="sxs-lookup"><span data-stu-id="0a2ae-123">-ClientCertCommonName</span></span>
<span data-ttu-id="0a2ae-124">Ügyfél tanúsítványának általános neve.</span><span class="sxs-lookup"><span data-stu-id="0a2ae-124">Client certificate common name.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByCn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a2ae-125">-ClientCertIsAdmin</span><span class="sxs-lookup"><span data-stu-id="0a2ae-125">-ClientCertIsAdmin</span></span>
<span data-ttu-id="0a2ae-126">Itt adhatja meg, hogy az ügyfél tanúsítványának van-e rendszergazdai szintje.</span><span class="sxs-lookup"><span data-stu-id="0a2ae-126">Use to specify if the client certificate has administrator level.</span></span>

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

### <span data-ttu-id="0a2ae-127">-ClientCertIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="0a2ae-127">-ClientCertIssuerThumbprint</span></span>
<span data-ttu-id="0a2ae-128">Az ügyfél-tanúsítvány kibocsátójának thumbprints listája.</span><span class="sxs-lookup"><span data-stu-id="0a2ae-128">List of Issuer thumbprints for the client certificate.</span></span>
<span data-ttu-id="0a2ae-129">Csak a ClientCertCommonName billentyűkombinációval együtt használható.</span><span class="sxs-lookup"><span data-stu-id="0a2ae-129">Only use in combination with ClientCertCommonName.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ClientCertByCn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a2ae-130">-ClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="0a2ae-130">-ClientCertThumbprint</span></span>
<span data-ttu-id="0a2ae-131">Ügyfél tanúsítványának thumbprint.</span><span class="sxs-lookup"><span data-stu-id="0a2ae-131">Client certificate thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a2ae-132">-ClientConnectionPort</span><span class="sxs-lookup"><span data-stu-id="0a2ae-132">-ClientConnectionPort</span></span>
<span data-ttu-id="0a2ae-133">A fürthöz való ügyfélkapcsolatok portja.</span><span class="sxs-lookup"><span data-stu-id="0a2ae-133">Port used for client connections to the cluster.</span></span>
<span data-ttu-id="0a2ae-134">Alapértelmezett érték: 19000.</span><span class="sxs-lookup"><span data-stu-id="0a2ae-134">Default: 19000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 19000
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a2ae-135">-CodeVersion</span><span class="sxs-lookup"><span data-stu-id="0a2ae-135">-CodeVersion</span></span>
<span data-ttu-id="0a2ae-136">Cluster service fabric code version.</span><span class="sxs-lookup"><span data-stu-id="0a2ae-136">Cluster service fabric code version.</span></span>
<span data-ttu-id="0a2ae-137">Csak akkor használja, ha a frissítési mód manuális.</span><span class="sxs-lookup"><span data-stu-id="0a2ae-137">Only use if upgrade mode is Manual.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a2ae-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a2ae-138">-DefaultProfile</span></span>
<span data-ttu-id="0a2ae-139">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0a2ae-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a2ae-140">-DnsName</span><span class="sxs-lookup"><span data-stu-id="0a2ae-140">-DnsName</span></span>
<span data-ttu-id="0a2ae-141">A fürt DNS-neve.</span><span class="sxs-lookup"><span data-stu-id="0a2ae-141">Cluster's dns name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a2ae-142">-HttpGatewayConnectionPort</span><span class="sxs-lookup"><span data-stu-id="0a2ae-142">-HttpGatewayConnectionPort</span></span>
<span data-ttu-id="0a2ae-143">A fürt http-kapcsolataihoz használt port.</span><span class="sxs-lookup"><span data-stu-id="0a2ae-143">Port used for http connections to the cluster.</span></span>
<span data-ttu-id="0a2ae-144">Alapértelmezett érték: 19080.</span><span class="sxs-lookup"><span data-stu-id="0a2ae-144">Default: 19080.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 19080
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a2ae-145">-Location</span><span class="sxs-lookup"><span data-stu-id="0a2ae-145">-Location</span></span>
<span data-ttu-id="0a2ae-146">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="0a2ae-146">The resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a2ae-147">-Name</span><span class="sxs-lookup"><span data-stu-id="0a2ae-147">-Name</span></span>
<span data-ttu-id="0a2ae-148">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="0a2ae-148">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a2ae-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a2ae-149">-ResourceGroupName</span></span>
<span data-ttu-id="0a2ae-150">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="0a2ae-150">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a2ae-151">-ReverseProxyEndpointPort</span><span class="sxs-lookup"><span data-stu-id="0a2ae-151">-ReverseProxyEndpointPort</span></span>
<span data-ttu-id="0a2ae-152">A fordított proxy által használt végpont.</span><span class="sxs-lookup"><span data-stu-id="0a2ae-152">Endpoint used by reverse proxy.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a2ae-153">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="0a2ae-153">-Sku</span></span>
<span data-ttu-id="0a2ae-154">Cluster's Sku, the options are Basic: it will have a minimum 3 seed nodes and only allows 1 node type and Standard: it will have a minimum 5 seed nodes and allows multiple node types.</span><span class="sxs-lookup"><span data-stu-id="0a2ae-154">Cluster's Sku, the options are Basic: it will have a minimum of 3 seed nodes and only allows 1 node type and Standard: it will have a minimum of 5 seed nodes and allows multiple node types.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ManagedClusterSku
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: Basic
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a2ae-155">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="0a2ae-155">-UpgradeMode</span></span>
<span data-ttu-id="0a2ae-156">Cluster service fabric code version upgrade mode.</span><span class="sxs-lookup"><span data-stu-id="0a2ae-156">Cluster service fabric code version upgrade mode.</span></span>
<span data-ttu-id="0a2ae-157">Automatikus vagy manuális.</span><span class="sxs-lookup"><span data-stu-id="0a2ae-157">Automatic or Manual.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a2ae-158">-UseTestExtension</span><span class="sxs-lookup"><span data-stu-id="0a2ae-158">-UseTestExtension</span></span>
<span data-ttu-id="0a2ae-159">Ha megadja a fürtöt, a rendszer a szolgáltatásteszt vmss kiterjesztéssel lesz csoportosítva.</span><span class="sxs-lookup"><span data-stu-id="0a2ae-159">If Specify The cluster will be crated with service test vmss extension.</span></span>

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

### <span data-ttu-id="0a2ae-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a2ae-160">-Confirm</span></span>
<span data-ttu-id="0a2ae-161">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0a2ae-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a2ae-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a2ae-162">-WhatIf</span></span>
<span data-ttu-id="0a2ae-163">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0a2ae-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a2ae-164">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0a2ae-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a2ae-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a2ae-165">CommonParameters</span></span>
<span data-ttu-id="0a2ae-166">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a2ae-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a2ae-167">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0a2ae-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a2ae-168">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0a2ae-168">INPUTS</span></span>

### <span data-ttu-id="0a2ae-169">System.String</span><span class="sxs-lookup"><span data-stu-id="0a2ae-169">System.String</span></span>

## <span data-ttu-id="0a2ae-170">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a2ae-170">OUTPUTS</span></span>

### <span data-ttu-id="0a2ae-171">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="0a2ae-171">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="0a2ae-172">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0a2ae-172">NOTES</span></span>

## <span data-ttu-id="0a2ae-173">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0a2ae-173">RELATED LINKS</span></span>

[<span data-ttu-id="0a2ae-174">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="0a2ae-174">New-AzServiceFabricManagedNodeType</span></span>](./New-AzServiceFabricManagedNodeType.md)