---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
ms.openlocfilehash: d2488792b5893e3972aa27ce98f87a23cec23073
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837999"
---
# <span data-ttu-id="db15e-101">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="db15e-101">Remove-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="db15e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="db15e-102">SYNOPSIS</span></span>
<span data-ttu-id="db15e-103">Ügyféltanúsítvány (ok) vagy tanúsítvány tárgya (i) eltávolítása a fürt ügyfél-hitelesítéséhez használatos.</span><span class="sxs-lookup"><span data-stu-id="db15e-103">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="db15e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="db15e-104">SYNTAX</span></span>

### <span data-ttu-id="db15e-105">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="db15e-105">SingleUpdateWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -CommonName <String>
 -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="db15e-106">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="db15e-106">SingleUpdateWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db15e-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="db15e-107">MultipleUpdatesWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db15e-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="db15e-108">MultipleUpdatesWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db15e-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="db15e-109">DESCRIPTION</span></span>
<span data-ttu-id="db15e-110">A **Remove-AzServiceFabricClientCertificate** eltávolíthatja az ügyfél tanúsítványát vagy a tanúsítvány tárgyát (ka) t az ügyfél-hitelesítéshez a fürtben való használat céljából.</span><span class="sxs-lookup"><span data-stu-id="db15e-110">Use **Remove-AzServiceFabricClientCertificate** to remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="db15e-111">Példák</span><span class="sxs-lookup"><span data-stu-id="db15e-111">EXAMPLES</span></span>

### <span data-ttu-id="db15e-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="db15e-112">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="db15e-113">Ez a parancs eltávolítja az ügyféltanúsítványt a fürtök "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" ujjlenyomatával.</span><span class="sxs-lookup"><span data-stu-id="db15e-113">This command will remove client certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' from the cluster.</span></span>

## <span data-ttu-id="db15e-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="db15e-114">PARAMETERS</span></span>

### <span data-ttu-id="db15e-115">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="db15e-115">-AdminClientThumbprint</span></span>
<span data-ttu-id="db15e-116">A csak rendszergazdai engedélyekkel rendelkező ügyféltanúsítvány-ujjlenyomat megadása</span><span class="sxs-lookup"><span data-stu-id="db15e-116">Specify client certificate thumbprint which only has admin permission</span></span>

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

### <span data-ttu-id="db15e-117">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="db15e-117">-ClientCertificateCommonName</span></span>
<span data-ttu-id="db15e-118">Az ügyfél köznapi nevének, a kibocsátások ujjlenyomatának és a hitelesítés típusának megadása</span><span class="sxs-lookup"><span data-stu-id="db15e-118">Specify client common name , issuer thumbprint and authentication type</span></span>

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

### <span data-ttu-id="db15e-119">-CommonName</span><span class="sxs-lookup"><span data-stu-id="db15e-119">-CommonName</span></span>
<span data-ttu-id="db15e-120">Ügyféltanúsítvány-köznapi név megadása</span><span class="sxs-lookup"><span data-stu-id="db15e-120">Specify client certificate common name</span></span>

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

### <span data-ttu-id="db15e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db15e-121">-DefaultProfile</span></span>
<span data-ttu-id="db15e-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="db15e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db15e-123">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="db15e-123">-IssuerThumbprint</span></span>
<span data-ttu-id="db15e-124">Adja meg az ügyfél tanúsítványának ujjlenyomatát</span><span class="sxs-lookup"><span data-stu-id="db15e-124">Specify thumbprint of client certificate's issuer</span></span>

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

### <span data-ttu-id="db15e-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="db15e-125">-Name</span></span>
<span data-ttu-id="db15e-126">A fürt nevének megadása</span><span class="sxs-lookup"><span data-stu-id="db15e-126">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="db15e-127">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="db15e-127">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="db15e-128">Adja meg az ügyféltanúsítvány-ujjlenyomatot, amely csak írásvédett engedélyt tartalmaz</span><span class="sxs-lookup"><span data-stu-id="db15e-128">Specify client certificate thumbprint which only has read only permission</span></span>

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

### <span data-ttu-id="db15e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db15e-129">-ResourceGroupName</span></span>
<span data-ttu-id="db15e-130">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="db15e-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="db15e-131">-Ujjlenyomat</span><span class="sxs-lookup"><span data-stu-id="db15e-131">-Thumbprint</span></span>
<span data-ttu-id="db15e-132">Ügyféltanúsítvány ujjlenyomatának megadása</span><span class="sxs-lookup"><span data-stu-id="db15e-132">Specify client certificate thumbprint</span></span>

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

### <span data-ttu-id="db15e-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="db15e-133">-Confirm</span></span>
<span data-ttu-id="db15e-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="db15e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db15e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db15e-135">-WhatIf</span></span>
<span data-ttu-id="db15e-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="db15e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db15e-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="db15e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db15e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db15e-138">CommonParameters</span></span>
<span data-ttu-id="db15e-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="db15e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db15e-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db15e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db15e-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="db15e-141">INPUTS</span></span>

### <span data-ttu-id="db15e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="db15e-142">System.String</span></span>

### <span data-ttu-id="db15e-143">System. string []</span><span class="sxs-lookup"><span data-stu-id="db15e-143">System.String[]</span></span>

### <span data-ttu-id="db15e-144">Microsoft. Azure. Command. ServiceFabric. models. PSClientCertificateCommonName []</span><span class="sxs-lookup"><span data-stu-id="db15e-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="db15e-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db15e-145">OUTPUTS</span></span>

### <span data-ttu-id="db15e-146">Microsoft. Azure. Command. ServiceFabric. models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="db15e-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="db15e-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="db15e-147">NOTES</span></span>

## <span data-ttu-id="db15e-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db15e-148">RELATED LINKS</span></span>

[<span data-ttu-id="db15e-149">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="db15e-149">Add-AzServiceFabricClientCertificate</span></span>](./Add-AzServiceFabricClientCertificate.md)
