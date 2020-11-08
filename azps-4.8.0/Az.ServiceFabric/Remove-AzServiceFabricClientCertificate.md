---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
ms.openlocfilehash: c7a88cad933781b00e720c273be467966991cebf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180852"
---
# <span data-ttu-id="a4914-101">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="a4914-101">Remove-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="a4914-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a4914-102">SYNOPSIS</span></span>
<span data-ttu-id="a4914-103">Ügyféltanúsítvány (ok) vagy tanúsítvány tárgya (i) eltávolítása a fürt ügyfél-hitelesítéséhez használatos.</span><span class="sxs-lookup"><span data-stu-id="a4914-103">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="a4914-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a4914-104">SYNTAX</span></span>

### <span data-ttu-id="a4914-105">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="a4914-105">SingleUpdateWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -CommonName <String>
 -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a4914-106">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="a4914-106">SingleUpdateWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4914-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="a4914-107">MultipleUpdatesWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4914-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="a4914-108">MultipleUpdatesWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4914-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="a4914-109">DESCRIPTION</span></span>
<span data-ttu-id="a4914-110">A **Remove-AzServiceFabricClientCertificate** eltávolíthatja az ügyfél tanúsítványát vagy a tanúsítvány tárgyát (ka) t az ügyfél-hitelesítéshez a fürtben való használat céljából.</span><span class="sxs-lookup"><span data-stu-id="a4914-110">Use **Remove-AzServiceFabricClientCertificate** to remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="a4914-111">Példák</span><span class="sxs-lookup"><span data-stu-id="a4914-111">EXAMPLES</span></span>

### <span data-ttu-id="a4914-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a4914-112">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="a4914-113">Ez a parancs eltávolítja az ügyféltanúsítványt a fürtök "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" ujjlenyomatával.</span><span class="sxs-lookup"><span data-stu-id="a4914-113">This command will remove client certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' from the cluster.</span></span>

## <span data-ttu-id="a4914-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a4914-114">PARAMETERS</span></span>

### <span data-ttu-id="a4914-115">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="a4914-115">-AdminClientThumbprint</span></span>
<span data-ttu-id="a4914-116">A csak rendszergazdai engedélyekkel rendelkező ügyféltanúsítvány-ujjlenyomat megadása</span><span class="sxs-lookup"><span data-stu-id="a4914-116">Specify client certificate thumbprint which only has admin permission</span></span>

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

### <span data-ttu-id="a4914-117">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="a4914-117">-ClientCertificateCommonName</span></span>
<span data-ttu-id="a4914-118">Az ügyfél köznapi nevének, a kibocsátások ujjlenyomatának és a hitelesítés típusának megadása</span><span class="sxs-lookup"><span data-stu-id="a4914-118">Specify client common name , issuer thumbprint and authentication type</span></span>

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

### <span data-ttu-id="a4914-119">-CommonName</span><span class="sxs-lookup"><span data-stu-id="a4914-119">-CommonName</span></span>
<span data-ttu-id="a4914-120">Ügyféltanúsítvány-köznapi név megadása</span><span class="sxs-lookup"><span data-stu-id="a4914-120">Specify client certificate common name</span></span>

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

### <span data-ttu-id="a4914-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4914-121">-DefaultProfile</span></span>
<span data-ttu-id="a4914-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a4914-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4914-123">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="a4914-123">-IssuerThumbprint</span></span>
<span data-ttu-id="a4914-124">Adja meg az ügyfél tanúsítványának ujjlenyomatát</span><span class="sxs-lookup"><span data-stu-id="a4914-124">Specify thumbprint of client certificate's issuer</span></span>

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

### <span data-ttu-id="a4914-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a4914-125">-Name</span></span>
<span data-ttu-id="a4914-126">A fürt nevének megadása</span><span class="sxs-lookup"><span data-stu-id="a4914-126">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="a4914-127">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="a4914-127">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="a4914-128">Adja meg az ügyféltanúsítvány-ujjlenyomatot, amely csak írásvédett engedélyt tartalmaz</span><span class="sxs-lookup"><span data-stu-id="a4914-128">Specify client certificate thumbprint which only has read only permission</span></span>

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

### <span data-ttu-id="a4914-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4914-129">-ResourceGroupName</span></span>
<span data-ttu-id="a4914-130">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="a4914-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="a4914-131">-Ujjlenyomat</span><span class="sxs-lookup"><span data-stu-id="a4914-131">-Thumbprint</span></span>
<span data-ttu-id="a4914-132">Ügyféltanúsítvány ujjlenyomatának megadása</span><span class="sxs-lookup"><span data-stu-id="a4914-132">Specify client certificate thumbprint</span></span>

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

### <span data-ttu-id="a4914-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a4914-133">-Confirm</span></span>
<span data-ttu-id="a4914-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a4914-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4914-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4914-135">-WhatIf</span></span>
<span data-ttu-id="a4914-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a4914-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4914-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a4914-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4914-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4914-138">CommonParameters</span></span>
<span data-ttu-id="a4914-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a4914-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4914-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a4914-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4914-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4914-141">INPUTS</span></span>

### <span data-ttu-id="a4914-142">System. String</span><span class="sxs-lookup"><span data-stu-id="a4914-142">System.String</span></span>

### <span data-ttu-id="a4914-143">System. string []</span><span class="sxs-lookup"><span data-stu-id="a4914-143">System.String[]</span></span>

### <span data-ttu-id="a4914-144">Microsoft. Azure. Command. ServiceFabric. models. PSClientCertificateCommonName []</span><span class="sxs-lookup"><span data-stu-id="a4914-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="a4914-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4914-145">OUTPUTS</span></span>

### <span data-ttu-id="a4914-146">Microsoft. Azure. Command. ServiceFabric. models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="a4914-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="a4914-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a4914-147">NOTES</span></span>

## <span data-ttu-id="a4914-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a4914-148">RELATED LINKS</span></span>

[<span data-ttu-id="a4914-149">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="a4914-149">Add-AzServiceFabricClientCertificate</span></span>](./Add-AzServiceFabricClientCertificate.md)
