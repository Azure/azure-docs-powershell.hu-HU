---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
ms.openlocfilehash: 913b610bc1d79c7a1792c06b53947fd3bf51151a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010873"
---
# <span data-ttu-id="89132-101">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="89132-101">Add-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="89132-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="89132-102">SYNOPSIS</span></span>
<span data-ttu-id="89132-103">Az ügyfél-hitelesítéshez adjon meg köznapi nevet vagy ujjlenyomatot a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="89132-103">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="89132-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="89132-104">SYNTAX</span></span>

### <span data-ttu-id="89132-105">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="89132-105">SingleUpdateWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89132-106">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="89132-106">SingleUpdateWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89132-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="89132-107">MultipleUpdatesWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89132-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="89132-108">MultipleUpdatesWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89132-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="89132-109">DESCRIPTION</span></span>
<span data-ttu-id="89132-110">A **Add-AzServiceFabricClientCertificate** használatával felvehet egy köznapi nevet és egy kiállított ujjlenyomatot vagy egy tanúsítvány ujjlenyomatát a fürthöz, így az ügyfél használhatja azt hitelesítésre.</span><span class="sxs-lookup"><span data-stu-id="89132-110">Use **Add-AzServiceFabricClientCertificate** to add a common name and issuer thumbprint or certificate thumbprint to the cluster, so the client can use it for authentication.</span></span>

## <span data-ttu-id="89132-111">Példák</span><span class="sxs-lookup"><span data-stu-id="89132-111">EXAMPLES</span></span>

### <span data-ttu-id="89132-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="89132-112">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="89132-113">Ez a parancs hozzáadja a "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" ujjlenyomatot a fürthöz, így az ügyfél a tanúsítványt rendszergazdaként használhatja a fürttel való kommunikációhoz.</span><span class="sxs-lookup"><span data-stu-id="89132-113">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="89132-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="89132-114">Example 2</span></span>
```
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="89132-115">Ezzel a paranccsal a "Contoso.com" és a "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" a fürthöz a "" nevű írásvédett ügyféltanúsítványt fogja hozzáadni.</span><span class="sxs-lookup"><span data-stu-id="89132-115">This command will add a read only client certificate that's common name is 'Contoso.com' and issuer thumbprint is '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster.</span></span>

## <span data-ttu-id="89132-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="89132-116">PARAMETERS</span></span>

### <span data-ttu-id="89132-117">-Rendszergazda</span><span class="sxs-lookup"><span data-stu-id="89132-117">-Admin</span></span>
<span data-ttu-id="89132-118">Ügyfél-hitelesítés típusa</span><span class="sxs-lookup"><span data-stu-id="89132-118">Client authentication type</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SingleUpdateWithThumbprint, SingleUpdateWithCommonName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89132-119">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="89132-119">-AdminClientThumbprint</span></span>
<span data-ttu-id="89132-120">A csak rendszergazdai engedélyekkel rendelkező ügyféltanúsítvány-ujjlenyomat megadása</span><span class="sxs-lookup"><span data-stu-id="89132-120">Specify client certificate thumbprint which only has admin permission</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89132-121">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="89132-121">-ClientCertificateCommonName</span></span>
<span data-ttu-id="89132-122">Az ügyfél köznapi nevének, a kibocsátások ujjlenyomatának és a hitelesítés típusának megadása</span><span class="sxs-lookup"><span data-stu-id="89132-122">Specify client common name , issuer thumbprint and authentication type</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]
Parameter Sets: MultipleUpdatesWithCommonName
Aliases: CertCommonName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89132-123">-CommonName</span><span class="sxs-lookup"><span data-stu-id="89132-123">-CommonName</span></span>
<span data-ttu-id="89132-124">Ügyféltanúsítvány-köznapi név megadása</span><span class="sxs-lookup"><span data-stu-id="89132-124">Specify client certificate common name</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89132-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89132-125">-DefaultProfile</span></span>
<span data-ttu-id="89132-126">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="89132-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89132-127">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="89132-127">-IssuerThumbprint</span></span>
<span data-ttu-id="89132-128">Adja meg az ügyfél tanúsítványának ujjlenyomatát</span><span class="sxs-lookup"><span data-stu-id="89132-128">Specify thumbprint of client certificate's issuer</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89132-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="89132-129">-Name</span></span>
<span data-ttu-id="89132-130">A fürt nevének megadása</span><span class="sxs-lookup"><span data-stu-id="89132-130">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="89132-131">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="89132-131">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="89132-132">Adja meg az ügyféltanúsítvány-ujjlenyomatot, amely csak írásvédett engedélyt tartalmaz</span><span class="sxs-lookup"><span data-stu-id="89132-132">Specify client certificate thumbprint which only has read only permission</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89132-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89132-133">-ResourceGroupName</span></span>
<span data-ttu-id="89132-134">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="89132-134">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="89132-135">-Ujjlenyomat</span><span class="sxs-lookup"><span data-stu-id="89132-135">-Thumbprint</span></span>
<span data-ttu-id="89132-136">Ügyféltanúsítvány ujjlenyomatának megadása</span><span class="sxs-lookup"><span data-stu-id="89132-136">Specify client certificate thumbprint</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithThumbprint
Aliases: ClientCertificateThumbprint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89132-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="89132-137">-Confirm</span></span>
<span data-ttu-id="89132-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="89132-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89132-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89132-139">-WhatIf</span></span>
<span data-ttu-id="89132-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="89132-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89132-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="89132-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89132-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89132-142">CommonParameters</span></span>
<span data-ttu-id="89132-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="89132-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89132-144">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89132-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89132-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="89132-145">INPUTS</span></span>

### <span data-ttu-id="89132-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="89132-146">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="89132-147">System. String</span><span class="sxs-lookup"><span data-stu-id="89132-147">System.String</span></span>

### <span data-ttu-id="89132-148">System. string []</span><span class="sxs-lookup"><span data-stu-id="89132-148">System.String[]</span></span>

### <span data-ttu-id="89132-149">Microsoft. Azure. Command. ServiceFabric. models. PSClientCertificateCommonName []</span><span class="sxs-lookup"><span data-stu-id="89132-149">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="89132-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="89132-150">OUTPUTS</span></span>

### <span data-ttu-id="89132-151">Microsoft. Azure. Command. ServiceFabric. models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="89132-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="89132-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="89132-152">NOTES</span></span>

## <span data-ttu-id="89132-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="89132-153">RELATED LINKS</span></span>

[<span data-ttu-id="89132-154">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="89132-154">Remove-AzServiceFabricClientCertificate</span></span>](./Remove-AzServiceFabricClientCertificate.md)
