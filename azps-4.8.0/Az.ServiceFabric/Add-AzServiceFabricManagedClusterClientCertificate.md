---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: e948acb179a0ae6a338fa02f01d1cb7d6efbd4fe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017588"
---
# <span data-ttu-id="d72c0-101">Add-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="d72c0-101">Add-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="d72c0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d72c0-102">SYNOPSIS</span></span>
<span data-ttu-id="d72c0-103">Adjon meg tanúsítvány-köznapi nevet vagy ujjlenyomatot a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="d72c0-103">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="d72c0-104">Ez a funkció regisztrálja a tanúsítványt a fürt ügyfél-hitelesítés céljából.</span><span class="sxs-lookup"><span data-stu-id="d72c0-104">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="d72c0-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d72c0-105">SYNTAX</span></span>

### <span data-ttu-id="d72c0-106">ClientCertByTpByObj (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d72c0-106">ClientCertByTpByObj (Default)</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d72c0-107">ClientCertByTpByName</span><span class="sxs-lookup"><span data-stu-id="d72c0-107">ClientCertByTpByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d72c0-108">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="d72c0-108">ClientCertByCnByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d72c0-109">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="d72c0-109">ClientCertByCnByObj</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d72c0-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="d72c0-110">DESCRIPTION</span></span>
<span data-ttu-id="d72c0-111">Adjon meg tanúsítvány-köznapi nevet vagy ujjlenyomatot a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="d72c0-111">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="d72c0-112">Ez a funkció regisztrálja a tanúsítványt a fürt ügyfél-hitelesítés céljából.</span><span class="sxs-lookup"><span data-stu-id="d72c0-112">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="d72c0-113">Példák</span><span class="sxs-lookup"><span data-stu-id="d72c0-113">EXAMPLES</span></span>

### <span data-ttu-id="d72c0-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d72c0-114">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="d72c0-115">Ez a parancs hozzáadja a "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" ujjlenyomatot a fürthöz, így az ügyfél a tanúsítványt rendszergazdaként használhatja a fürttel való kommunikációhoz.</span><span class="sxs-lookup"><span data-stu-id="d72c0-115">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="d72c0-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="d72c0-116">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="d72c0-117">Ezzel a paranccsal a "Contoso.com" és a "két kibocsátó" köznapi névvel rendelkező írásvédett ügyféltanúsítványt kell hozzáadni.</span><span class="sxs-lookup"><span data-stu-id="d72c0-117">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers.</span></span>

### <span data-ttu-id="d72c0-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="d72c0-118">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
$cluster | Add-AzServiceFabricManagedClusterClientCertificate -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="d72c0-119">Ezzel a paranccsal a "Contoso.com" és a "2 kibocsátó" nevű "csak olvasható" ügyféltanúsítványt fogja hozzáadni a csövekkel.</span><span class="sxs-lookup"><span data-stu-id="d72c0-119">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers, with piping.</span></span>

## <span data-ttu-id="d72c0-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d72c0-120">PARAMETERS</span></span>

### <span data-ttu-id="d72c0-121">-Rendszergazda</span><span class="sxs-lookup"><span data-stu-id="d72c0-121">-Admin</span></span>
<span data-ttu-id="d72c0-122">Segítségével megadhatja, hogy az ügyféltanúsítvány rendelkezik-e rendszergazdai szintű engedélyekkel.</span><span class="sxs-lookup"><span data-stu-id="d72c0-122">Use to specify if the client certificate has administrator level.</span></span>

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

### <span data-ttu-id="d72c0-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d72c0-123">-AsJob</span></span>
<span data-ttu-id="d72c0-124">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="d72c0-124">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d72c0-125">-CommonName</span><span class="sxs-lookup"><span data-stu-id="d72c0-125">-CommonName</span></span>
<span data-ttu-id="d72c0-126">Ügyfél-tanúsítvány – köznapi név.</span><span class="sxs-lookup"><span data-stu-id="d72c0-126">Client certificate common name.</span></span>

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

### <span data-ttu-id="d72c0-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d72c0-127">-DefaultProfile</span></span>
<span data-ttu-id="d72c0-128">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d72c0-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d72c0-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d72c0-129">-InputObject</span></span>
<span data-ttu-id="d72c0-130">Felügyelt cluster resource</span><span class="sxs-lookup"><span data-stu-id="d72c0-130">Managed cluster resource</span></span>

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

### <span data-ttu-id="d72c0-131">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="d72c0-131">-IssuerThumbprint</span></span>
<span data-ttu-id="d72c0-132">Az ügyfél tanúsítványához tartozó thumbprints listája.</span><span class="sxs-lookup"><span data-stu-id="d72c0-132">List of Issuer thumbprints for the client certificate.</span></span>
<span data-ttu-id="d72c0-133">Csak a CommonName együtt használható.</span><span class="sxs-lookup"><span data-stu-id="d72c0-133">Only use in combination with CommonName.</span></span>

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

### <span data-ttu-id="d72c0-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d72c0-134">-Name</span></span>
<span data-ttu-id="d72c0-135">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="d72c0-135">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="d72c0-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d72c0-136">-ResourceGroupName</span></span>
<span data-ttu-id="d72c0-137">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="d72c0-137">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="d72c0-138">-Ujjlenyomat</span><span class="sxs-lookup"><span data-stu-id="d72c0-138">-Thumbprint</span></span>
<span data-ttu-id="d72c0-139">Ügyféltanúsítvány ujjlenyomata.</span><span class="sxs-lookup"><span data-stu-id="d72c0-139">Client certificate thumbprint.</span></span>

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

### <span data-ttu-id="d72c0-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d72c0-140">-Confirm</span></span>
<span data-ttu-id="d72c0-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d72c0-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d72c0-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d72c0-142">-WhatIf</span></span>
<span data-ttu-id="d72c0-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d72c0-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d72c0-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d72c0-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d72c0-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d72c0-145">CommonParameters</span></span>
<span data-ttu-id="d72c0-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d72c0-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d72c0-147">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d72c0-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d72c0-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d72c0-148">INPUTS</span></span>

### <span data-ttu-id="d72c0-149">System. String</span><span class="sxs-lookup"><span data-stu-id="d72c0-149">System.String</span></span>

## <span data-ttu-id="d72c0-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d72c0-150">OUTPUTS</span></span>

### <span data-ttu-id="d72c0-151">Microsoft. Azure. Command. ServiceFabric. models. PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="d72c0-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="d72c0-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d72c0-152">NOTES</span></span>

## <span data-ttu-id="d72c0-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d72c0-153">RELATED LINKS</span></span>
