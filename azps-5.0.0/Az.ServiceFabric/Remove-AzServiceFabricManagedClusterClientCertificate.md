---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: d9a3e5488fe55a1d5090fb21ffb211e6fcec53c2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185861"
---
# <span data-ttu-id="2d776-101">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="2d776-101">Remove-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="2d776-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2d776-102">SYNOPSIS</span></span>
<span data-ttu-id="2d776-103">Remvoe-ügyféltanúsítvány ujjlenyomat vagy köznapi név szerint.</span><span class="sxs-lookup"><span data-stu-id="2d776-103">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="2d776-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2d776-104">SYNTAX</span></span>

### <span data-ttu-id="2d776-105">ClientCertByTpByObj (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2d776-105">ClientCertByTpByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -Thumbprint <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d776-106">ClientCertByCnTpName</span><span class="sxs-lookup"><span data-stu-id="2d776-106">ClientCertByCnTpName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d776-107">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="2d776-107">ClientCertByCnByName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d776-108">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="2d776-108">ClientCertByCnByObj</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -CommonName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d776-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="2d776-109">DESCRIPTION</span></span>
<span data-ttu-id="2d776-110">Remvoe-ügyféltanúsítvány ujjlenyomat vagy köznapi név szerint.</span><span class="sxs-lookup"><span data-stu-id="2d776-110">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="2d776-111">Példák</span><span class="sxs-lookup"><span data-stu-id="2d776-111">EXAMPLES</span></span>

### <span data-ttu-id="2d776-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2d776-112">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -CommonName 'Contoso.com'
```

<span data-ttu-id="2d776-113">Ügyféltanúsítvány eltávolítása köznapi névvel</span><span class="sxs-lookup"><span data-stu-id="2d776-113">Remove client certificate by common name.</span></span>

### <span data-ttu-id="2d776-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="2d776-114">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="2d776-115">Ügyféltanúsítvány eltávolítása ujjlenyomat alapján.</span><span class="sxs-lookup"><span data-stu-id="2d776-115">Remove client certificate by thumbprint.</span></span>

### <span data-ttu-id="2d776-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="2d776-116">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster | Remove-AzServiceFabricManagedClusterClientCertificate -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="2d776-117">Ügyféltanúsítványok eltávolítása ujjlenyomatról a csővezetékekkel.</span><span class="sxs-lookup"><span data-stu-id="2d776-117">Remove client certificate by thumbprint, with piping.</span></span>

## <span data-ttu-id="2d776-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2d776-118">PARAMETERS</span></span>

### <span data-ttu-id="2d776-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d776-119">-AsJob</span></span>
<span data-ttu-id="2d776-120">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="2d776-120">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="2d776-121">-CommonName</span><span class="sxs-lookup"><span data-stu-id="2d776-121">-CommonName</span></span>
<span data-ttu-id="2d776-122">Ügyfél-tanúsítvány – köznapi név.</span><span class="sxs-lookup"><span data-stu-id="2d776-122">Client certificate common name.</span></span>

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

### <span data-ttu-id="2d776-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d776-123">-DefaultProfile</span></span>
<span data-ttu-id="2d776-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2d776-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d776-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2d776-125">-InputObject</span></span>
<span data-ttu-id="2d776-126">Felügyelt cluster resource</span><span class="sxs-lookup"><span data-stu-id="2d776-126">Managed cluster resource</span></span>

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

### <span data-ttu-id="2d776-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2d776-127">-Name</span></span>
<span data-ttu-id="2d776-128">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="2d776-128">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="2d776-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d776-129">-PassThru</span></span>
<span data-ttu-id="2d776-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="2d776-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="2d776-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d776-131">-ResourceGroupName</span></span>
<span data-ttu-id="2d776-132">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="2d776-132">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="2d776-133">-Ujjlenyomat</span><span class="sxs-lookup"><span data-stu-id="2d776-133">-Thumbprint</span></span>
<span data-ttu-id="2d776-134">Ügyféltanúsítvány ujjlenyomata.</span><span class="sxs-lookup"><span data-stu-id="2d776-134">Client certificate thumbprint.</span></span>

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

### <span data-ttu-id="2d776-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2d776-135">-Confirm</span></span>
<span data-ttu-id="2d776-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2d776-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d776-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d776-137">-WhatIf</span></span>
<span data-ttu-id="2d776-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2d776-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d776-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2d776-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d776-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d776-140">CommonParameters</span></span>
<span data-ttu-id="2d776-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2d776-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d776-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2d776-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d776-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d776-143">INPUTS</span></span>

### <span data-ttu-id="2d776-144">System. String</span><span class="sxs-lookup"><span data-stu-id="2d776-144">System.String</span></span>

## <span data-ttu-id="2d776-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d776-145">OUTPUTS</span></span>

### <span data-ttu-id="2d776-146">Microsoft. Azure. Command. ServiceFabric. models. PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="2d776-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="2d776-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2d776-147">NOTES</span></span>

## <span data-ttu-id="2d776-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2d776-148">RELATED LINKS</span></span>
