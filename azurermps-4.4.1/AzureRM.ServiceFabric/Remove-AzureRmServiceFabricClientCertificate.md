---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClientCertificate.md
ms.openlocfilehash: d0ba19efaf0cf3dc1f997d06231e056fb20b02f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494671"
---
# <span data-ttu-id="c79d8-101">Remove-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="c79d8-101">Remove-AzureRmServiceFabricClientCertificate</span></span>

## <span data-ttu-id="c79d8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c79d8-102">SYNOPSIS</span></span>
<span data-ttu-id="c79d8-103">Ügyféltanúsítvány (ok) vagy tanúsítvány tárgya (i) eltávolítása a fürt ügyfél-hitelesítéséhez használatos.</span><span class="sxs-lookup"><span data-stu-id="c79d8-103">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c79d8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c79d8-104">SYNTAX</span></span>

### <span data-ttu-id="c79d8-105">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="c79d8-105">SingleUpdateWithCommonName</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c79d8-106">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="c79d8-106">SingleUpdateWithThumbprint</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c79d8-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="c79d8-107">MultipleUpdatesWithCommonName</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c79d8-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="c79d8-108">MultipleUpdatesWithThumbprint</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c79d8-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="c79d8-109">DESCRIPTION</span></span>
<span data-ttu-id="c79d8-110">A **Remove-AzureRmServiceFabricClientCertificate** eltávolíthatja az ügyfél tanúsítványát vagy a tanúsítvány tárgyát (ka) t az ügyfél-hitelesítéshez a fürtben való használat céljából.</span><span class="sxs-lookup"><span data-stu-id="c79d8-110">Use **Remove-AzureRmServiceFabricClientCertificate** to remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="c79d8-111">Példák</span><span class="sxs-lookup"><span data-stu-id="c79d8-111">EXAMPLES</span></span>

### <span data-ttu-id="c79d8-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c79d8-112">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="c79d8-113">Ez a parancs eltávolítja az ügyféltanúsítványt a fürtök "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" ujjlenyomatával.</span><span class="sxs-lookup"><span data-stu-id="c79d8-113">This command will remove client certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' from the cluster.</span></span>

## <span data-ttu-id="c79d8-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c79d8-114">PARAMETERS</span></span>

### <span data-ttu-id="c79d8-115">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="c79d8-115">-AdminClientThumbprint</span></span>
<span data-ttu-id="c79d8-116">Adjon meg olyan ügyféltanúsítvány-ujjlenyomatot, amely csak rendszergazdai engedélyekkel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="c79d8-116">Specify client certificate thumbprint that only has admin permission.</span></span>

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

### <span data-ttu-id="c79d8-117">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="c79d8-117">-ClientCertificateCommonName</span></span>
<span data-ttu-id="c79d8-118">Adja meg az ügyfél köznapi nevét, a kibocsátás-ujjlenyomatot és a hitelesítés típusát.</span><span class="sxs-lookup"><span data-stu-id="c79d8-118">Specify client common name, issuer thumbprint, and authentication type.</span></span>

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

### <span data-ttu-id="c79d8-119">-CommonName</span><span class="sxs-lookup"><span data-stu-id="c79d8-119">-CommonName</span></span>
<span data-ttu-id="c79d8-120">Adja meg az ügyfél tanúsítványának köznapi nevét.</span><span class="sxs-lookup"><span data-stu-id="c79d8-120">Specify client certificate common name.</span></span>

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

### <span data-ttu-id="c79d8-121">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="c79d8-121">-IssuerThumbprint</span></span>
<span data-ttu-id="c79d8-122">Adja meg az ügyfél tanúsítvány-kibocsátási ujjlenyomatát.</span><span class="sxs-lookup"><span data-stu-id="c79d8-122">Specify client certificate issuer thumbprint.</span></span>

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

### <span data-ttu-id="c79d8-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c79d8-123">-Name</span></span>
<span data-ttu-id="c79d8-124">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="c79d8-124">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="c79d8-125">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="c79d8-125">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="c79d8-126">Adja meg a csak olvasható engedélyt tartalmazó ügyféltanúsítvány-ujjlenyomatot.</span><span class="sxs-lookup"><span data-stu-id="c79d8-126">Specify client certificate thumbprint that has read only permission.</span></span>

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

### <span data-ttu-id="c79d8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c79d8-127">-ResourceGroupName</span></span>
<span data-ttu-id="c79d8-128">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c79d8-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c79d8-129">-Ujjlenyomat</span><span class="sxs-lookup"><span data-stu-id="c79d8-129">-Thumbprint</span></span>
<span data-ttu-id="c79d8-130">Ügyféltanúsítvány-ujjlenyomat megadása</span><span class="sxs-lookup"><span data-stu-id="c79d8-130">Specify client certificate thumbprint.</span></span>

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

### <span data-ttu-id="c79d8-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c79d8-131">-Confirm</span></span>
<span data-ttu-id="c79d8-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c79d8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c79d8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c79d8-133">-WhatIf</span></span>
<span data-ttu-id="c79d8-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c79d8-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c79d8-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c79d8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c79d8-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c79d8-136">-DefaultProfile</span></span>
<span data-ttu-id="c79d8-137">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c79d8-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c79d8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c79d8-138">CommonParameters</span></span>
<span data-ttu-id="c79d8-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c79d8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c79d8-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c79d8-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c79d8-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c79d8-141">INPUTS</span></span>

### <span data-ttu-id="c79d8-142">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c79d8-142">System.Collections.Hashtable</span></span>
<span data-ttu-id="c79d8-143">System. String</span><span class="sxs-lookup"><span data-stu-id="c79d8-143">System.String</span></span>

<span data-ttu-id="c79d8-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c79d8-144">System.Boolean</span></span>

## <span data-ttu-id="c79d8-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c79d8-145">OUTPUTS</span></span>

### <span data-ttu-id="c79d8-146">Microsoft. Azure. Command. ServiceFabric. models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="c79d8-146">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="c79d8-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c79d8-147">NOTES</span></span>

## <span data-ttu-id="c79d8-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c79d8-148">RELATED LINKS</span></span>

[<span data-ttu-id="c79d8-149">Add-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="c79d8-149">Add-AzureRmServiceFabricClientCertificate</span></span>](./Add-AzureRmServiceFabricClientCertificate.md)
