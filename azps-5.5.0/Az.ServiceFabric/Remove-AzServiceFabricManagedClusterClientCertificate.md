---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: d9a3e5488fe55a1d5090fb21ffb211e6fcec53c2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158378"
---
# <span data-ttu-id="44bf4-101">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="44bf4-101">Remove-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="44bf4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44bf4-102">SYNOPSIS</span></span>
<span data-ttu-id="44bf4-103">Ügyfél tanúsítványának visszaírása thumbprint vagy common name alapján.</span><span class="sxs-lookup"><span data-stu-id="44bf4-103">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="44bf4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="44bf4-104">SYNTAX</span></span>

### <span data-ttu-id="44bf4-105">ClientCertByTpByObj (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="44bf4-105">ClientCertByTpByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -Thumbprint <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44bf4-106">ClientCertByCnTpName</span><span class="sxs-lookup"><span data-stu-id="44bf4-106">ClientCertByCnTpName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="44bf4-107">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="44bf4-107">ClientCertByCnByName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="44bf4-108">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="44bf4-108">ClientCertByCnByObj</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -CommonName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44bf4-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="44bf4-109">DESCRIPTION</span></span>
<span data-ttu-id="44bf4-110">Ügyfél tanúsítványának visszaírása thumbprint vagy common name alapján.</span><span class="sxs-lookup"><span data-stu-id="44bf4-110">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="44bf4-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="44bf4-111">EXAMPLES</span></span>

### <span data-ttu-id="44bf4-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="44bf4-112">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -CommonName 'Contoso.com'
```

<span data-ttu-id="44bf4-113">Távolítsa el az ügyfél tanúsítványát általános néven.</span><span class="sxs-lookup"><span data-stu-id="44bf4-113">Remove client certificate by common name.</span></span>

### <span data-ttu-id="44bf4-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="44bf4-114">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="44bf4-115">Távolítsa el az ügyfél tanúsítványát thumbprint.</span><span class="sxs-lookup"><span data-stu-id="44bf4-115">Remove client certificate by thumbprint.</span></span>

### <span data-ttu-id="44bf4-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="44bf4-116">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster | Remove-AzServiceFabricManagedClusterClientCertificate -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="44bf4-117">Távolítsa el az ügyfél tanúsítványát thumbprint,with piping.</span><span class="sxs-lookup"><span data-stu-id="44bf4-117">Remove client certificate by thumbprint, with piping.</span></span>

## <span data-ttu-id="44bf4-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44bf4-118">PARAMETERS</span></span>

### <span data-ttu-id="44bf4-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44bf4-119">-AsJob</span></span>
<span data-ttu-id="44bf4-120">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="44bf4-120">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="44bf4-121">-CommonName</span><span class="sxs-lookup"><span data-stu-id="44bf4-121">-CommonName</span></span>
<span data-ttu-id="44bf4-122">Ügyfél tanúsítványának általános neve.</span><span class="sxs-lookup"><span data-stu-id="44bf4-122">Client certificate common name.</span></span>

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

### <span data-ttu-id="44bf4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44bf4-123">-DefaultProfile</span></span>
<span data-ttu-id="44bf4-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="44bf4-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44bf4-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44bf4-125">-InputObject</span></span>
<span data-ttu-id="44bf4-126">Felügyelt fürterőforrás</span><span class="sxs-lookup"><span data-stu-id="44bf4-126">Managed cluster resource</span></span>

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

### <span data-ttu-id="44bf4-127">-Name</span><span class="sxs-lookup"><span data-stu-id="44bf4-127">-Name</span></span>
<span data-ttu-id="44bf4-128">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="44bf4-128">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByCnTpName, ClientCertByCnByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44bf4-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="44bf4-129">-PassThru</span></span>
<span data-ttu-id="44bf4-130">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="44bf4-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="44bf4-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44bf4-131">-ResourceGroupName</span></span>
<span data-ttu-id="44bf4-132">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="44bf4-132">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByCnTpName, ClientCertByCnByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44bf4-133">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="44bf4-133">-Thumbprint</span></span>
<span data-ttu-id="44bf4-134">Ügyfél tanúsítványának thumbprint.</span><span class="sxs-lookup"><span data-stu-id="44bf4-134">Client certificate thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByObj, ClientCertByCnTpName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44bf4-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44bf4-135">-Confirm</span></span>
<span data-ttu-id="44bf4-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="44bf4-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44bf4-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44bf4-137">-WhatIf</span></span>
<span data-ttu-id="44bf4-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="44bf4-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44bf4-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="44bf4-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44bf4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44bf4-140">CommonParameters</span></span>
<span data-ttu-id="44bf4-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44bf4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44bf4-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="44bf4-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44bf4-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="44bf4-143">INPUTS</span></span>

### <span data-ttu-id="44bf4-144">System.String</span><span class="sxs-lookup"><span data-stu-id="44bf4-144">System.String</span></span>

## <span data-ttu-id="44bf4-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="44bf4-145">OUTPUTS</span></span>

### <span data-ttu-id="44bf4-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="44bf4-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="44bf4-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="44bf4-147">NOTES</span></span>

## <span data-ttu-id="44bf4-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="44bf4-148">RELATED LINKS</span></span>
