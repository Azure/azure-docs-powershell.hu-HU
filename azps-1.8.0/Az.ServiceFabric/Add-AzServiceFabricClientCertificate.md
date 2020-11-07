---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
ms.openlocfilehash: bb6280eb623f52256eda5324e3d7980894fc91e3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669128"
---
# <span data-ttu-id="c5485-101">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="c5485-101">Add-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="c5485-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c5485-102">SYNOPSIS</span></span>
<span data-ttu-id="c5485-103">Az ügyfél-hitelesítéshez adjon meg köznapi nevet vagy ujjlenyomatot a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="c5485-103">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="c5485-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c5485-104">SYNTAX</span></span>

### <span data-ttu-id="c5485-105">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="c5485-105">SingleUpdateWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5485-106">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="c5485-106">SingleUpdateWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5485-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="c5485-107">MultipleUpdatesWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5485-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="c5485-108">MultipleUpdatesWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5485-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="c5485-109">DESCRIPTION</span></span>
<span data-ttu-id="c5485-110">A **Add-AzServiceFabricClientCertificate** használatával felvehet egy köznapi nevet és egy kiállított ujjlenyomatot vagy egy tanúsítvány ujjlenyomatát a fürthöz, így az ügyfél használhatja azt hitelesítésre.</span><span class="sxs-lookup"><span data-stu-id="c5485-110">Use **Add-AzServiceFabricClientCertificate** to add a common name and issuer thumbprint or certificate thumbprint to the cluster, so the client can use it for authentication.</span></span>

## <span data-ttu-id="c5485-111">Példák</span><span class="sxs-lookup"><span data-stu-id="c5485-111">EXAMPLES</span></span>

### <span data-ttu-id="c5485-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c5485-112">Example 1</span></span>
```
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="c5485-113">Ez a parancs hozzáadja a "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" ujjlenyomatot a fürthöz, így az ügyfél a tanúsítványt rendszergazdaként használhatja a fürttel való kommunikációhoz.</span><span class="sxs-lookup"><span data-stu-id="c5485-113">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="c5485-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="c5485-114">Example 2</span></span>
```
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="c5485-115">Ezzel a paranccsal a "Contoso.com" és a "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" a fürthöz a "" nevű írásvédett ügyféltanúsítványt fogja hozzáadni.</span><span class="sxs-lookup"><span data-stu-id="c5485-115">This command will add a read only client certificate that's common name is 'Contoso.com' and issuer thumbprint is '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster.</span></span>

## <span data-ttu-id="c5485-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c5485-116">PARAMETERS</span></span>

### <span data-ttu-id="c5485-117">-Rendszergazda</span><span class="sxs-lookup"><span data-stu-id="c5485-117">-Admin</span></span>
<span data-ttu-id="c5485-118">Ügyfél-hitelesítés típusa</span><span class="sxs-lookup"><span data-stu-id="c5485-118">Client authentication type.</span></span>

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

### <span data-ttu-id="c5485-119">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="c5485-119">-AdminClientThumbprint</span></span>
<span data-ttu-id="c5485-120">Adjon meg olyan ügyféltanúsítvány-ujjlenyomatot, amely csak rendszergazdai engedélyekkel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="c5485-120">Specify client certificate thumbprint that only has admin permission.</span></span>

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

### <span data-ttu-id="c5485-121">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="c5485-121">-ClientCertificateCommonName</span></span>
<span data-ttu-id="c5485-122">Adja meg az ügyfél köznapi nevét, a kibocsátás-ujjlenyomatot és a hitelesítés típusát.</span><span class="sxs-lookup"><span data-stu-id="c5485-122">Specify client common name, issuer thumbprint, and authentication type.</span></span>

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

### <span data-ttu-id="c5485-123">-CommonName</span><span class="sxs-lookup"><span data-stu-id="c5485-123">-CommonName</span></span>
<span data-ttu-id="c5485-124">Adja meg az ügyfél tanúsítványának köznapi nevét.</span><span class="sxs-lookup"><span data-stu-id="c5485-124">Specify client certificate common name.</span></span>

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

### <span data-ttu-id="c5485-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5485-125">-DefaultProfile</span></span>
<span data-ttu-id="c5485-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c5485-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5485-127">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="c5485-127">-IssuerThumbprint</span></span>
<span data-ttu-id="c5485-128">Adja meg az ügyfél tanúsítvány-kibocsátási ujjlenyomatát.</span><span class="sxs-lookup"><span data-stu-id="c5485-128">Specify client certificate issuer thumbprint.</span></span>

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

### <span data-ttu-id="c5485-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c5485-129">-Name</span></span>
<span data-ttu-id="c5485-130">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="c5485-130">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="c5485-131">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="c5485-131">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="c5485-132">Adja meg a csak olvasható engedélyt tartalmazó ügyféltanúsítvány-ujjlenyomatot.</span><span class="sxs-lookup"><span data-stu-id="c5485-132">Specify client certificate thumbprint that has read only permission.</span></span>

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

### <span data-ttu-id="c5485-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5485-133">-ResourceGroupName</span></span>
<span data-ttu-id="c5485-134">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c5485-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c5485-135">-Ujjlenyomat</span><span class="sxs-lookup"><span data-stu-id="c5485-135">-Thumbprint</span></span>
<span data-ttu-id="c5485-136">Ügyféltanúsítvány-ujjlenyomat megadása</span><span class="sxs-lookup"><span data-stu-id="c5485-136">Specify client certificate thumbprint.</span></span>

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

### <span data-ttu-id="c5485-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c5485-137">-Confirm</span></span>
<span data-ttu-id="c5485-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c5485-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5485-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5485-139">-WhatIf</span></span>
<span data-ttu-id="c5485-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c5485-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c5485-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c5485-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5485-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5485-142">CommonParameters</span></span>
<span data-ttu-id="c5485-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c5485-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5485-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5485-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5485-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5485-145">INPUTS</span></span>

### <span data-ttu-id="c5485-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c5485-146">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="c5485-147">System. String</span><span class="sxs-lookup"><span data-stu-id="c5485-147">System.String</span></span>

### <span data-ttu-id="c5485-148">System. string []</span><span class="sxs-lookup"><span data-stu-id="c5485-148">System.String[]</span></span>

### <span data-ttu-id="c5485-149">Microsoft. Azure. Command. ServiceFabric. models. PSClientCertificateCommonName []</span><span class="sxs-lookup"><span data-stu-id="c5485-149">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="c5485-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5485-150">OUTPUTS</span></span>

### <span data-ttu-id="c5485-151">Microsoft. Azure. Command. ServiceFabric. models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="c5485-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="c5485-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c5485-152">NOTES</span></span>

## <span data-ttu-id="c5485-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c5485-153">RELATED LINKS</span></span>

[<span data-ttu-id="c5485-154">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="c5485-154">Remove-AzServiceFabricClientCertificate</span></span>](./Remove-AzServiceFabricClientCertificate.md)
