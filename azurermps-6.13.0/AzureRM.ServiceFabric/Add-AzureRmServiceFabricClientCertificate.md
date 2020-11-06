---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClientCertificate.md
ms.openlocfilehash: d1bd4dc4a3fd47d19d76568e9c60a51f09d739c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495644"
---
# <span data-ttu-id="91254-101">Add-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="91254-101">Add-AzureRmServiceFabricClientCertificate</span></span>

## <span data-ttu-id="91254-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="91254-102">SYNOPSIS</span></span>
<span data-ttu-id="91254-103">Az ügyfél-hitelesítéshez adjon meg köznapi nevet vagy ujjlenyomatot a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="91254-103">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91254-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="91254-104">SYNTAX</span></span>

### <span data-ttu-id="91254-105">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="91254-105">SingleUpdateWithThumbprint</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91254-106">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="91254-106">SingleUpdateWithCommonName</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91254-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="91254-107">MultipleUpdatesWithCommonName</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91254-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="91254-108">MultipleUpdatesWithThumbprint</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91254-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="91254-109">DESCRIPTION</span></span>
<span data-ttu-id="91254-110">A **Add-AzureRmServiceFabricClientCertificate** használatával felvehet egy köznapi nevet és egy kiállított ujjlenyomatot vagy egy tanúsítvány ujjlenyomatát a fürthöz, így az ügyfél használhatja azt hitelesítésre.</span><span class="sxs-lookup"><span data-stu-id="91254-110">Use **Add-AzureRmServiceFabricClientCertificate** to add a common name and issuer thumbprint or certificate thumbprint to the cluster, so the client can use it for authentication.</span></span>

## <span data-ttu-id="91254-111">Példák</span><span class="sxs-lookup"><span data-stu-id="91254-111">EXAMPLES</span></span>

### <span data-ttu-id="91254-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="91254-112">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="91254-113">Ez a parancs hozzáadja a "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" ujjlenyomatot a fürthöz, így az ügyfél a tanúsítványt rendszergazdaként használhatja a fürttel való kommunikációhoz.</span><span class="sxs-lookup"><span data-stu-id="91254-113">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="91254-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="91254-114">Example 2</span></span>
```
PS c:> Add-AzureRmServiceFabricClientCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="91254-115">Ezzel a paranccsal a "Contoso.com" és a "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" a fürthöz a "" nevű írásvédett ügyféltanúsítványt fogja hozzáadni.</span><span class="sxs-lookup"><span data-stu-id="91254-115">This command will add a read only client certificate that's common name is 'Contoso.com' and issuer thumbprint is '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster.</span></span>

## <span data-ttu-id="91254-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="91254-116">PARAMETERS</span></span>

### <span data-ttu-id="91254-117">-Rendszergazda</span><span class="sxs-lookup"><span data-stu-id="91254-117">-Admin</span></span>
<span data-ttu-id="91254-118">Ügyfél-hitelesítés típusa</span><span class="sxs-lookup"><span data-stu-id="91254-118">Client authentication type.</span></span>

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

### <span data-ttu-id="91254-119">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="91254-119">-AdminClientThumbprint</span></span>
<span data-ttu-id="91254-120">Adjon meg olyan ügyféltanúsítvány-ujjlenyomatot, amely csak rendszergazdai engedélyekkel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="91254-120">Specify client certificate thumbprint that only has admin permission.</span></span>

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

### <span data-ttu-id="91254-121">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="91254-121">-ClientCertificateCommonName</span></span>
<span data-ttu-id="91254-122">Adja meg az ügyfél köznapi nevét, a kibocsátás-ujjlenyomatot és a hitelesítés típusát.</span><span class="sxs-lookup"><span data-stu-id="91254-122">Specify client common name, issuer thumbprint, and authentication type.</span></span>

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

### <span data-ttu-id="91254-123">-CommonName</span><span class="sxs-lookup"><span data-stu-id="91254-123">-CommonName</span></span>
<span data-ttu-id="91254-124">Adja meg az ügyfél tanúsítványának köznapi nevét.</span><span class="sxs-lookup"><span data-stu-id="91254-124">Specify client certificate common name.</span></span>

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

### <span data-ttu-id="91254-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91254-125">-DefaultProfile</span></span>
<span data-ttu-id="91254-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="91254-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91254-127">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="91254-127">-IssuerThumbprint</span></span>
<span data-ttu-id="91254-128">Adja meg az ügyfél tanúsítvány-kibocsátási ujjlenyomatát.</span><span class="sxs-lookup"><span data-stu-id="91254-128">Specify client certificate issuer thumbprint.</span></span>

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

### <span data-ttu-id="91254-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="91254-129">-Name</span></span>
<span data-ttu-id="91254-130">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="91254-130">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="91254-131">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="91254-131">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="91254-132">Adja meg a csak olvasható engedélyt tartalmazó ügyféltanúsítvány-ujjlenyomatot.</span><span class="sxs-lookup"><span data-stu-id="91254-132">Specify client certificate thumbprint that has read only permission.</span></span>

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

### <span data-ttu-id="91254-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91254-133">-ResourceGroupName</span></span>
<span data-ttu-id="91254-134">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="91254-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="91254-135">-Ujjlenyomat</span><span class="sxs-lookup"><span data-stu-id="91254-135">-Thumbprint</span></span>
<span data-ttu-id="91254-136">Ügyféltanúsítvány-ujjlenyomat megadása</span><span class="sxs-lookup"><span data-stu-id="91254-136">Specify client certificate thumbprint.</span></span>

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

### <span data-ttu-id="91254-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="91254-137">-Confirm</span></span>
<span data-ttu-id="91254-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="91254-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91254-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91254-139">-WhatIf</span></span>
<span data-ttu-id="91254-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="91254-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91254-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="91254-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91254-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91254-142">CommonParameters</span></span>
<span data-ttu-id="91254-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="91254-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91254-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91254-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91254-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="91254-145">INPUTS</span></span>

### <span data-ttu-id="91254-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="91254-146">System.Management.Automation.SwitchParameter</span></span>
<span data-ttu-id="91254-147">Paraméterek: rendszergazda (ByValue)</span><span class="sxs-lookup"><span data-stu-id="91254-147">Parameters: Admin (ByValue)</span></span>

### <span data-ttu-id="91254-148">System. String</span><span class="sxs-lookup"><span data-stu-id="91254-148">System.String</span></span>
<span data-ttu-id="91254-149">Paraméterek: CommonName (ByValue), IssuerThumbprint (ByValue), ujjlenyomat (ByValue)</span><span class="sxs-lookup"><span data-stu-id="91254-149">Parameters: CommonName (ByValue), IssuerThumbprint (ByValue), Thumbprint (ByValue)</span></span>

### <span data-ttu-id="91254-150">System. string []</span><span class="sxs-lookup"><span data-stu-id="91254-150">System.String[]</span></span>
<span data-ttu-id="91254-151">Paraméterek: AdminClientThumbprint (ByValue), ReadonlyClientThumbprint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="91254-151">Parameters: AdminClientThumbprint (ByValue), ReadonlyClientThumbprint (ByValue)</span></span>

### <span data-ttu-id="91254-152">Microsoft. Azure. Command. ServiceFabric. models. PSClientCertificateCommonName []</span><span class="sxs-lookup"><span data-stu-id="91254-152">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>
<span data-ttu-id="91254-153">Paraméterek: ClientCertificateCommonName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="91254-153">Parameters: ClientCertificateCommonName (ByValue)</span></span>

## <span data-ttu-id="91254-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="91254-154">OUTPUTS</span></span>

### <span data-ttu-id="91254-155">Microsoft. Azure. Command. ServiceFabric. models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="91254-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="91254-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="91254-156">NOTES</span></span>

## <span data-ttu-id="91254-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="91254-157">RELATED LINKS</span></span>

[<span data-ttu-id="91254-158">Remove-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="91254-158">Remove-AzureRmServiceFabricClientCertificate</span></span>](./Remove-AzureRmServiceFabricClientCertificate.md)
