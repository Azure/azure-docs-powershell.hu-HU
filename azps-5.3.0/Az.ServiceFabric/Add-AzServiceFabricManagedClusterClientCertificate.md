---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: e948acb179a0ae6a338fa02f01d1cb7d6efbd4fe
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479588"
---
# <span data-ttu-id="79dbd-101">Add-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="79dbd-101">Add-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="79dbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79dbd-102">SYNOPSIS</span></span>
<span data-ttu-id="79dbd-103">Adja hozzá a tanúsítvány általános nevét vagy thumbprint-ját a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="79dbd-103">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="79dbd-104">Ez a módszer ismét regisztrálja a tanúsítványt, ügyfél-hitelesítési célokra.</span><span class="sxs-lookup"><span data-stu-id="79dbd-104">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="79dbd-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="79dbd-105">SYNTAX</span></span>

### <span data-ttu-id="79dbd-106">ClientCertByTpByObj (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="79dbd-106">ClientCertByTpByObj (Default)</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="79dbd-107">ClientCertByTpByName</span><span class="sxs-lookup"><span data-stu-id="79dbd-107">ClientCertByTpByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="79dbd-108">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="79dbd-108">ClientCertByCnByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79dbd-109">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="79dbd-109">ClientCertByCnByObj</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79dbd-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="79dbd-110">DESCRIPTION</span></span>
<span data-ttu-id="79dbd-111">Adja hozzá a tanúsítvány általános nevét vagy thumbprint-ját a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="79dbd-111">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="79dbd-112">Ez a módszer ismét regisztrálja a tanúsítványt, ügyfél-hitelesítési célokra.</span><span class="sxs-lookup"><span data-stu-id="79dbd-112">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="79dbd-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="79dbd-113">EXAMPLES</span></span>

### <span data-ttu-id="79dbd-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="79dbd-114">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="79dbd-115">Ez a parancs hozzáadja a "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" hüvelykujjú tanúsítványt a fürthöz, hogy az ügyfél rendszergazdaként használva kommunikáljon a fürtbel.</span><span class="sxs-lookup"><span data-stu-id="79dbd-115">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="79dbd-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="79dbd-116">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="79dbd-117">Ez a parancs egy "csak olvasható" ügyfél tanúsítványt ad hozzá, amely közös neve "Contoso.com" és 2 kibocsátó.</span><span class="sxs-lookup"><span data-stu-id="79dbd-117">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers.</span></span>

### <span data-ttu-id="79dbd-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="79dbd-118">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
$cluster | Add-AzServiceFabricManagedClusterClientCertificate -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="79dbd-119">Ez a parancs egy "Contoso.com" és 2 kibocsátót is hozzáad egy írásjeles ügyfél tanúsítványhoz, pipával.</span><span class="sxs-lookup"><span data-stu-id="79dbd-119">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers, with piping.</span></span>

## <span data-ttu-id="79dbd-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79dbd-120">PARAMETERS</span></span>

### <span data-ttu-id="79dbd-121">-Admin</span><span class="sxs-lookup"><span data-stu-id="79dbd-121">-Admin</span></span>
<span data-ttu-id="79dbd-122">Itt adhatja meg, hogy az ügyfél tanúsítványának van-e rendszergazdai szintje.</span><span class="sxs-lookup"><span data-stu-id="79dbd-122">Use to specify if the client certificate has administrator level.</span></span>

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

### <span data-ttu-id="79dbd-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79dbd-123">-AsJob</span></span>
<span data-ttu-id="79dbd-124">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="79dbd-124">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="79dbd-125">-CommonName</span><span class="sxs-lookup"><span data-stu-id="79dbd-125">-CommonName</span></span>
<span data-ttu-id="79dbd-126">Ügyfél tanúsítványának általános neve.</span><span class="sxs-lookup"><span data-stu-id="79dbd-126">Client certificate common name.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByCnByName, ClientCertByCnByObj
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79dbd-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79dbd-127">-DefaultProfile</span></span>
<span data-ttu-id="79dbd-128">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="79dbd-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79dbd-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79dbd-129">-InputObject</span></span>
<span data-ttu-id="79dbd-130">Felügyelt fürterőforrás</span><span class="sxs-lookup"><span data-stu-id="79dbd-130">Managed cluster resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster
Parameter Sets: ClientCertByTpByObj, ClientCertByCnByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79dbd-131">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="79dbd-131">-IssuerThumbprint</span></span>
<span data-ttu-id="79dbd-132">Az ügyfél-tanúsítvány kibocsátójának thumbprints listája.</span><span class="sxs-lookup"><span data-stu-id="79dbd-132">List of Issuer thumbprints for the client certificate.</span></span>
<span data-ttu-id="79dbd-133">Csak a CommonName névvel együtt használható.</span><span class="sxs-lookup"><span data-stu-id="79dbd-133">Only use in combination with CommonName.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ClientCertByCnByName, ClientCertByCnByObj
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79dbd-134">-Name</span><span class="sxs-lookup"><span data-stu-id="79dbd-134">-Name</span></span>
<span data-ttu-id="79dbd-135">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="79dbd-135">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByName, ClientCertByCnByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79dbd-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79dbd-136">-ResourceGroupName</span></span>
<span data-ttu-id="79dbd-137">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="79dbd-137">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByName, ClientCertByCnByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79dbd-138">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="79dbd-138">-Thumbprint</span></span>
<span data-ttu-id="79dbd-139">Ügyfél tanúsítványának thumbprint.</span><span class="sxs-lookup"><span data-stu-id="79dbd-139">Client certificate thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByObj, ClientCertByTpByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79dbd-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79dbd-140">-Confirm</span></span>
<span data-ttu-id="79dbd-141">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="79dbd-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79dbd-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79dbd-142">-WhatIf</span></span>
<span data-ttu-id="79dbd-143">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="79dbd-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79dbd-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="79dbd-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79dbd-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79dbd-145">CommonParameters</span></span>
<span data-ttu-id="79dbd-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79dbd-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79dbd-147">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="79dbd-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79dbd-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="79dbd-148">INPUTS</span></span>

### <span data-ttu-id="79dbd-149">System.String</span><span class="sxs-lookup"><span data-stu-id="79dbd-149">System.String</span></span>

## <span data-ttu-id="79dbd-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="79dbd-150">OUTPUTS</span></span>

### <span data-ttu-id="79dbd-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="79dbd-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="79dbd-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="79dbd-152">NOTES</span></span>

## <span data-ttu-id="79dbd-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="79dbd-153">RELATED LINKS</span></span>
