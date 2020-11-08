---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedCluster.md
ms.openlocfilehash: 9dd54f0f1ca56a8bedf3550e238a4308b519925d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186539"
---
# <span data-ttu-id="95745-101">New-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="95745-101">New-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="95745-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="95745-102">SYNOPSIS</span></span>
<span data-ttu-id="95745-103">Új felügyelt fürt létrehozása</span><span class="sxs-lookup"><span data-stu-id="95745-103">Create new managed cluster.</span></span>

## <span data-ttu-id="95745-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="95745-104">SYNTAX</span></span>

### <span data-ttu-id="95745-105">ClientCertByTp (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="95745-105">ClientCertByTp (Default)</span></span>
```
New-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-ClientCertIsAdmin]
 -ClientCertThumbprint <String> -AdminPassword <SecureString> [-AdminUserName <String>]
 [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>] [-DnsName <String>]
 [-ReverseProxyEndpointPort <Int32>] [-Sku <ManagedClusterSku>] [-UseTestExtension] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95745-106">ClientCertByCn</span><span class="sxs-lookup"><span data-stu-id="95745-106">ClientCertByCn</span></span>
```
New-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-ClientCertIsAdmin]
 -ClientCertCommonName <String> [-ClientCertIssuerThumbprint <String[]>] -AdminPassword <SecureString>
 [-AdminUserName <String>] [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>]
 [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-Sku <ManagedClusterSku>] [-UseTestExtension]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95745-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="95745-107">DESCRIPTION</span></span>
<span data-ttu-id="95745-108">Ez a parancsmag csomópont-típus nélkül hozza létre a felügyelt fürterőforrás-erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="95745-108">This cmdlet will create a managed cluster resource without node types.</span></span> <span data-ttu-id="95745-109">A fürt betöltéséhez elsődleges csomópontot kell hozzáadnia az [új AzServiceFabricManagedNodeType](./New-AzServiceFabricManagedNodeType.md).</span><span class="sxs-lookup"><span data-stu-id="95745-109">To bootstrap the cluster A primary node type needs to be added use [New-AzServiceFabricManagedNodeType](./New-AzServiceFabricManagedNodeType.md).</span></span>

## <span data-ttu-id="95745-110">Példák</span><span class="sxs-lookup"><span data-stu-id="95745-110">EXAMPLES</span></span>

### <span data-ttu-id="95745-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="95745-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$password = ConvertTo-SecureString -AsPlainText -Force "testpass1234!@#$"
New-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Location centraluseuap -ClusterName $clusterName -AdminPassword $password -Verbose
```

<span data-ttu-id="95745-112">Ez a parancs létrehoz egy cluster-erőforrást alapértelmezett alapsku-val.</span><span class="sxs-lookup"><span data-stu-id="95745-112">This command creates a cluster resource with default basic sku.</span></span>

### <span data-ttu-id="95745-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="95745-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$password = ConvertTo-SecureString -AsPlainText -Force "testpass1234!@#$"
New-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Location centraluseuap -ClusterName $clusterName -ClientCertThumbprint XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX -ClientCertIsAdmin -AdminPassword $password -Sku Standard -Verbose
```

<span data-ttu-id="95745-114">A parancs létrehoz egy centraluseuap az első rendszergazdai ügyféltanúsítvány és a normál SKU beállítással.</span><span class="sxs-lookup"><span data-stu-id="95745-114">This command creates a cluster resource in centraluseuap with an initial admin client certificate and standard sku.</span></span>

## <span data-ttu-id="95745-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="95745-115">PARAMETERS</span></span>

### <span data-ttu-id="95745-116">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="95745-116">-AdminPassword</span></span>
<span data-ttu-id="95745-117">A virtuális gépekhez használt rendszergazdai jelszó.</span><span class="sxs-lookup"><span data-stu-id="95745-117">Admin password used for the virtual machines.</span></span>

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

### <span data-ttu-id="95745-118">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="95745-118">-AdminUserName</span></span>
<span data-ttu-id="95745-119">A virtuális gépekhez használt rendszergazdai jelszó.</span><span class="sxs-lookup"><span data-stu-id="95745-119">Admin password used for the virtual machines.</span></span>
<span data-ttu-id="95745-120">Alapértelmezett: vmadmin.</span><span class="sxs-lookup"><span data-stu-id="95745-120">Default: vmadmin.</span></span>

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

### <span data-ttu-id="95745-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95745-121">-AsJob</span></span>
<span data-ttu-id="95745-122">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="95745-122">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="95745-123">-ClientCertCommonName</span><span class="sxs-lookup"><span data-stu-id="95745-123">-ClientCertCommonName</span></span>
<span data-ttu-id="95745-124">Ügyfél-tanúsítvány – köznapi név.</span><span class="sxs-lookup"><span data-stu-id="95745-124">Client certificate common name.</span></span>

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

### <span data-ttu-id="95745-125">-ClientCertIsAdmin</span><span class="sxs-lookup"><span data-stu-id="95745-125">-ClientCertIsAdmin</span></span>
<span data-ttu-id="95745-126">Segítségével megadhatja, hogy az ügyféltanúsítvány rendelkezik-e rendszergazdai szintű engedélyekkel.</span><span class="sxs-lookup"><span data-stu-id="95745-126">Use to specify if the client certificate has administrator level.</span></span>

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

### <span data-ttu-id="95745-127">-ClientCertIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="95745-127">-ClientCertIssuerThumbprint</span></span>
<span data-ttu-id="95745-128">Az ügyfél tanúsítványához tartozó thumbprints listája.</span><span class="sxs-lookup"><span data-stu-id="95745-128">List of Issuer thumbprints for the client certificate.</span></span>
<span data-ttu-id="95745-129">Csak a ClientCertCommonName együtt használható.</span><span class="sxs-lookup"><span data-stu-id="95745-129">Only use in combination with ClientCertCommonName.</span></span>

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

### <span data-ttu-id="95745-130">-ClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="95745-130">-ClientCertThumbprint</span></span>
<span data-ttu-id="95745-131">Ügyféltanúsítvány ujjlenyomata.</span><span class="sxs-lookup"><span data-stu-id="95745-131">Client certificate thumbprint.</span></span>

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

### <span data-ttu-id="95745-132">-ClientConnectionPort</span><span class="sxs-lookup"><span data-stu-id="95745-132">-ClientConnectionPort</span></span>
<span data-ttu-id="95745-133">A fürthöz való ügyfél-kapcsolatokhoz használt port.</span><span class="sxs-lookup"><span data-stu-id="95745-133">Port used for client connections to the cluster.</span></span>
<span data-ttu-id="95745-134">Alapértelmezett: 19000.</span><span class="sxs-lookup"><span data-stu-id="95745-134">Default: 19000.</span></span>

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

### <span data-ttu-id="95745-135">-CodeVersion</span><span class="sxs-lookup"><span data-stu-id="95745-135">-CodeVersion</span></span>
<span data-ttu-id="95745-136">Fürtszolgáltatási szövet kód verziója.</span><span class="sxs-lookup"><span data-stu-id="95745-136">Cluster service fabric code version.</span></span>
<span data-ttu-id="95745-137">Csak akkor használja, ha a frissítési mód kézi.</span><span class="sxs-lookup"><span data-stu-id="95745-137">Only use if upgrade mode is Manual.</span></span>

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

### <span data-ttu-id="95745-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95745-138">-DefaultProfile</span></span>
<span data-ttu-id="95745-139">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="95745-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95745-140">-DnsName</span><span class="sxs-lookup"><span data-stu-id="95745-140">-DnsName</span></span>
<span data-ttu-id="95745-141">A fürt DNS-neve.</span><span class="sxs-lookup"><span data-stu-id="95745-141">Cluster's dns name.</span></span>

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

### <span data-ttu-id="95745-142">-HttpGatewayConnectionPort</span><span class="sxs-lookup"><span data-stu-id="95745-142">-HttpGatewayConnectionPort</span></span>
<span data-ttu-id="95745-143">A fürthöz való http-kapcsolatokhoz használt port.</span><span class="sxs-lookup"><span data-stu-id="95745-143">Port used for http connections to the cluster.</span></span>
<span data-ttu-id="95745-144">Alapértelmezett: 19080.</span><span class="sxs-lookup"><span data-stu-id="95745-144">Default: 19080.</span></span>

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

### <span data-ttu-id="95745-145">-Hely</span><span class="sxs-lookup"><span data-stu-id="95745-145">-Location</span></span>
<span data-ttu-id="95745-146">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="95745-146">The resource location</span></span>

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

### <span data-ttu-id="95745-147">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="95745-147">-Name</span></span>
<span data-ttu-id="95745-148">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="95745-148">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="95745-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95745-149">-ResourceGroupName</span></span>
<span data-ttu-id="95745-150">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="95745-150">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="95745-151">-ReverseProxyEndpointPort</span><span class="sxs-lookup"><span data-stu-id="95745-151">-ReverseProxyEndpointPort</span></span>
<span data-ttu-id="95745-152">A fordított proxy által használt végpont.</span><span class="sxs-lookup"><span data-stu-id="95745-152">Endpoint used by reverse proxy.</span></span>

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

### <span data-ttu-id="95745-153">-SKU</span><span class="sxs-lookup"><span data-stu-id="95745-153">-Sku</span></span>
<span data-ttu-id="95745-154">A fürt SKU-ban a beállítások Alapvetőak: legalább 3 vetőmag-csomópontot tartalmaz, és csak 1 csomópontot és szabványt ad meg: legalább 5 magot tartalmaz, és lehetővé teszi a több csomópont típusának használatát.</span><span class="sxs-lookup"><span data-stu-id="95745-154">Cluster's Sku, the options are Basic: it will have a minimum of 3 seed nodes and only allows 1 node type and Standard: it will have a minimum of 5 seed nodes and allows multiple node types.</span></span>

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

### <span data-ttu-id="95745-155">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="95745-155">-UpgradeMode</span></span>
<span data-ttu-id="95745-156">Fürtszolgáltatási szövet kód verziófrissítési módja.</span><span class="sxs-lookup"><span data-stu-id="95745-156">Cluster service fabric code version upgrade mode.</span></span>
<span data-ttu-id="95745-157">Automatikus vagy manuális.</span><span class="sxs-lookup"><span data-stu-id="95745-157">Automatic or Manual.</span></span>

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

### <span data-ttu-id="95745-158">-UseTestExtension</span><span class="sxs-lookup"><span data-stu-id="95745-158">-UseTestExtension</span></span>
<span data-ttu-id="95745-159">Ha adja meg, hogy a rendszer a fürtöt vmss-kiterjesztéssel becsomagolja.</span><span class="sxs-lookup"><span data-stu-id="95745-159">If Specify The cluster will be crated with service test vmss extension.</span></span>

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

### <span data-ttu-id="95745-160">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="95745-160">-Confirm</span></span>
<span data-ttu-id="95745-161">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="95745-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95745-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95745-162">-WhatIf</span></span>
<span data-ttu-id="95745-163">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="95745-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95745-164">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="95745-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95745-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95745-165">CommonParameters</span></span>
<span data-ttu-id="95745-166">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="95745-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95745-167">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="95745-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95745-168">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="95745-168">INPUTS</span></span>

### <span data-ttu-id="95745-169">System. String</span><span class="sxs-lookup"><span data-stu-id="95745-169">System.String</span></span>

## <span data-ttu-id="95745-170">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="95745-170">OUTPUTS</span></span>

### <span data-ttu-id="95745-171">Microsoft. Azure. Command. ServiceFabric. models. PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="95745-171">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="95745-172">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="95745-172">NOTES</span></span>

## <span data-ttu-id="95745-173">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="95745-173">RELATED LINKS</span></span>

[<span data-ttu-id="95745-174">Új – AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="95745-174">New-AzServiceFabricManagedNodeType</span></span>](./New-AzServiceFabricManagedNodeType.md)