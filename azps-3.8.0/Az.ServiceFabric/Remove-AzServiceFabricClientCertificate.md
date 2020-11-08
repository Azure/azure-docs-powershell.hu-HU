---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
ms.openlocfilehash: dc9f7dfa26b350a5dadea4bfa3afb9ad832fa063
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011679"
---
# <span data-ttu-id="a0448-101">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="a0448-101">Remove-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="a0448-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a0448-102">SYNOPSIS</span></span>
<span data-ttu-id="a0448-103">Ügyféltanúsítvány (ok) vagy tanúsítvány tárgya (i) eltávolítása a fürt ügyfél-hitelesítéséhez használatos.</span><span class="sxs-lookup"><span data-stu-id="a0448-103">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="a0448-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a0448-104">SYNTAX</span></span>

### <span data-ttu-id="a0448-105">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="a0448-105">SingleUpdateWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -CommonName <String>
 -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a0448-106">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="a0448-106">SingleUpdateWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0448-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="a0448-107">MultipleUpdatesWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0448-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="a0448-108">MultipleUpdatesWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0448-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="a0448-109">DESCRIPTION</span></span>
<span data-ttu-id="a0448-110">A **Remove-AzServiceFabricClientCertificate** eltávolíthatja az ügyfél tanúsítványát vagy a tanúsítvány tárgyát (ka) t az ügyfél-hitelesítéshez a fürtben való használat céljából.</span><span class="sxs-lookup"><span data-stu-id="a0448-110">Use **Remove-AzServiceFabricClientCertificate** to remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="a0448-111">Példák</span><span class="sxs-lookup"><span data-stu-id="a0448-111">EXAMPLES</span></span>

### <span data-ttu-id="a0448-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a0448-112">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="a0448-113">Ez a parancs eltávolítja az ügyféltanúsítványt a fürtök "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" ujjlenyomatával.</span><span class="sxs-lookup"><span data-stu-id="a0448-113">This command will remove client certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' from the cluster.</span></span>

## <span data-ttu-id="a0448-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a0448-114">PARAMETERS</span></span>

### <span data-ttu-id="a0448-115">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="a0448-115">-AdminClientThumbprint</span></span>
<span data-ttu-id="a0448-116">A csak rendszergazdai engedélyekkel rendelkező ügyféltanúsítvány-ujjlenyomat megadása</span><span class="sxs-lookup"><span data-stu-id="a0448-116">Specify client certificate thumbprint which only has admin permission</span></span>

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

### <span data-ttu-id="a0448-117">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="a0448-117">-ClientCertificateCommonName</span></span>
<span data-ttu-id="a0448-118">Az ügyfél köznapi nevének, a kibocsátások ujjlenyomatának és a hitelesítés típusának megadása</span><span class="sxs-lookup"><span data-stu-id="a0448-118">Specify client common name , issuer thumbprint and authentication type</span></span>

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

### <span data-ttu-id="a0448-119">-CommonName</span><span class="sxs-lookup"><span data-stu-id="a0448-119">-CommonName</span></span>
<span data-ttu-id="a0448-120">Ügyféltanúsítvány-köznapi név megadása</span><span class="sxs-lookup"><span data-stu-id="a0448-120">Specify client certificate common name</span></span>

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

### <span data-ttu-id="a0448-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0448-121">-DefaultProfile</span></span>
<span data-ttu-id="a0448-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a0448-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0448-123">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="a0448-123">-IssuerThumbprint</span></span>
<span data-ttu-id="a0448-124">Adja meg az ügyfél tanúsítványának ujjlenyomatát</span><span class="sxs-lookup"><span data-stu-id="a0448-124">Specify thumbprint of client certificate's issuer</span></span>

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

### <span data-ttu-id="a0448-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a0448-125">-Name</span></span>
<span data-ttu-id="a0448-126">A fürt nevének megadása</span><span class="sxs-lookup"><span data-stu-id="a0448-126">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="a0448-127">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="a0448-127">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="a0448-128">Adja meg az ügyféltanúsítvány-ujjlenyomatot, amely csak írásvédett engedélyt tartalmaz</span><span class="sxs-lookup"><span data-stu-id="a0448-128">Specify client certificate thumbprint which only has read only permission</span></span>

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

### <span data-ttu-id="a0448-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0448-129">-ResourceGroupName</span></span>
<span data-ttu-id="a0448-130">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="a0448-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="a0448-131">-Ujjlenyomat</span><span class="sxs-lookup"><span data-stu-id="a0448-131">-Thumbprint</span></span>
<span data-ttu-id="a0448-132">Ügyféltanúsítvány ujjlenyomatának megadása</span><span class="sxs-lookup"><span data-stu-id="a0448-132">Specify client certificate thumbprint</span></span>

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

### <span data-ttu-id="a0448-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a0448-133">-Confirm</span></span>
<span data-ttu-id="a0448-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a0448-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0448-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0448-135">-WhatIf</span></span>
<span data-ttu-id="a0448-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a0448-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0448-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a0448-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0448-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0448-138">CommonParameters</span></span>
<span data-ttu-id="a0448-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a0448-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0448-140">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0448-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0448-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0448-141">INPUTS</span></span>

### <span data-ttu-id="a0448-142">System. String</span><span class="sxs-lookup"><span data-stu-id="a0448-142">System.String</span></span>

### <span data-ttu-id="a0448-143">System. string []</span><span class="sxs-lookup"><span data-stu-id="a0448-143">System.String[]</span></span>

### <span data-ttu-id="a0448-144">Microsoft. Azure. Command. ServiceFabric. models. PSClientCertificateCommonName []</span><span class="sxs-lookup"><span data-stu-id="a0448-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="a0448-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0448-145">OUTPUTS</span></span>

### <span data-ttu-id="a0448-146">Microsoft. Azure. Command. ServiceFabric. models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="a0448-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="a0448-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a0448-147">NOTES</span></span>

## <span data-ttu-id="a0448-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a0448-148">RELATED LINKS</span></span>

[<span data-ttu-id="a0448-149">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="a0448-149">Add-AzServiceFabricClientCertificate</span></span>](./Add-AzServiceFabricClientCertificate.md)
