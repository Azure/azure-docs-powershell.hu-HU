---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: f0ba5cb4d461bbc70ba742ae46ba4b9489923545
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005478"
---
# <span data-ttu-id="b7420-101">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="b7420-101">Remove-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="b7420-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7420-102">SYNOPSIS</span></span>
<span data-ttu-id="b7420-103">Ügyfél tanúsítványának visszaírása thumbprint vagy common name alapján.</span><span class="sxs-lookup"><span data-stu-id="b7420-103">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="b7420-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b7420-104">SYNTAX</span></span>

### <span data-ttu-id="b7420-105">ClientCertByTpByObj (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b7420-105">ClientCertByTpByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -Thumbprint <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7420-106">ClientCertByCnTpName</span><span class="sxs-lookup"><span data-stu-id="b7420-106">ClientCertByCnTpName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b7420-107">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="b7420-107">ClientCertByCnByName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b7420-108">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="b7420-108">ClientCertByCnByObj</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -CommonName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7420-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b7420-109">DESCRIPTION</span></span>
<span data-ttu-id="b7420-110">Ügyfél tanúsítványának visszaírása thumbprint vagy common name alapján.</span><span class="sxs-lookup"><span data-stu-id="b7420-110">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="b7420-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b7420-111">EXAMPLES</span></span>

### <span data-ttu-id="b7420-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="b7420-112">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -CommonName 'Contoso.com'
```

<span data-ttu-id="b7420-113">Távolítsa el az ügyfél tanúsítványát általános néven.</span><span class="sxs-lookup"><span data-stu-id="b7420-113">Remove client certificate by common name.</span></span>

### <span data-ttu-id="b7420-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="b7420-114">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="b7420-115">Távolítsa el az ügyfél tanúsítványát thumbprint.</span><span class="sxs-lookup"><span data-stu-id="b7420-115">Remove client certificate by thumbprint.</span></span>

### <span data-ttu-id="b7420-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="b7420-116">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster | Remove-AzServiceFabricManagedClusterClientCertificate -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="b7420-117">Távolítsa el az ügyfél tanúsítványát thumbprint,with piping.</span><span class="sxs-lookup"><span data-stu-id="b7420-117">Remove client certificate by thumbprint, with piping.</span></span>

## <span data-ttu-id="b7420-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7420-118">PARAMETERS</span></span>

### <span data-ttu-id="b7420-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b7420-119">-AsJob</span></span>
<span data-ttu-id="b7420-120">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="b7420-120">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b7420-121">-CommonName</span><span class="sxs-lookup"><span data-stu-id="b7420-121">-CommonName</span></span>
<span data-ttu-id="b7420-122">Ügyfél tanúsítványának általános neve.</span><span class="sxs-lookup"><span data-stu-id="b7420-122">Client certificate common name.</span></span>

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

### <span data-ttu-id="b7420-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7420-123">-DefaultProfile</span></span>
<span data-ttu-id="b7420-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b7420-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7420-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7420-125">-InputObject</span></span>
<span data-ttu-id="b7420-126">Felügyelt fürterőforrás</span><span class="sxs-lookup"><span data-stu-id="b7420-126">Managed cluster resource</span></span>

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

### <span data-ttu-id="b7420-127">-Name</span><span class="sxs-lookup"><span data-stu-id="b7420-127">-Name</span></span>
<span data-ttu-id="b7420-128">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="b7420-128">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="b7420-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7420-129">-PassThru</span></span>
<span data-ttu-id="b7420-130">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="b7420-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="b7420-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7420-131">-ResourceGroupName</span></span>
<span data-ttu-id="b7420-132">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="b7420-132">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="b7420-133">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="b7420-133">-Thumbprint</span></span>
<span data-ttu-id="b7420-134">Ügyfél tanúsítványának thumbprint.</span><span class="sxs-lookup"><span data-stu-id="b7420-134">Client certificate thumbprint.</span></span>

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

### <span data-ttu-id="b7420-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7420-135">-Confirm</span></span>
<span data-ttu-id="b7420-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b7420-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7420-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7420-137">-WhatIf</span></span>
<span data-ttu-id="b7420-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b7420-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7420-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b7420-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7420-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7420-140">CommonParameters</span></span>
<span data-ttu-id="b7420-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7420-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7420-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7420-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7420-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b7420-143">INPUTS</span></span>

### <span data-ttu-id="b7420-144">System.String</span><span class="sxs-lookup"><span data-stu-id="b7420-144">System.String</span></span>

## <span data-ttu-id="b7420-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7420-145">OUTPUTS</span></span>

### <span data-ttu-id="b7420-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="b7420-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="b7420-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b7420-147">NOTES</span></span>

## <span data-ttu-id="b7420-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b7420-148">RELATED LINKS</span></span>
