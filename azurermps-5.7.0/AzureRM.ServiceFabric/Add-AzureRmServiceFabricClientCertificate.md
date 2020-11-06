---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClientCertificate.md
ms.openlocfilehash: c7b6e00ccbe368267fd6b110490df4f70b2229a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500395"
---
# <span data-ttu-id="47279-101">Add-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="47279-101">Add-AzureRmServiceFabricClientCertificate</span></span>

## <span data-ttu-id="47279-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="47279-102">SYNOPSIS</span></span>
<span data-ttu-id="47279-103">Az ügyfél-hitelesítéshez adjon meg köznapi nevet vagy ujjlenyomatot a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="47279-103">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47279-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="47279-104">SYNTAX</span></span>

### <span data-ttu-id="47279-105">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="47279-105">SingleUpdateWithThumbprint</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47279-106">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="47279-106">SingleUpdateWithCommonName</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47279-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="47279-107">MultipleUpdatesWithCommonName</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47279-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="47279-108">MultipleUpdatesWithThumbprint</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47279-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="47279-109">DESCRIPTION</span></span>
<span data-ttu-id="47279-110">A **Add-AzureRmServiceFabricClientCertificate** használatával felvehet egy köznapi nevet és egy kiállított ujjlenyomatot vagy egy tanúsítvány ujjlenyomatát a fürthöz, így az ügyfél használhatja azt hitelesítésre.</span><span class="sxs-lookup"><span data-stu-id="47279-110">Use **Add-AzureRmServiceFabricClientCertificate** to add a common name and issuer thumbprint or certificate thumbprint to the cluster, so the client can use it for authentication.</span></span>

## <span data-ttu-id="47279-111">Példák</span><span class="sxs-lookup"><span data-stu-id="47279-111">EXAMPLES</span></span>

### <span data-ttu-id="47279-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="47279-112">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="47279-113">Ez a parancs hozzáadja a "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" ujjlenyomatot a fürthöz, így az ügyfél a tanúsítványt rendszergazdaként használhatja a fürttel való kommunikációhoz.</span><span class="sxs-lookup"><span data-stu-id="47279-113">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="47279-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="47279-114">Example 2</span></span>
```
PS c:> Add-AzureRmServiceFabricClientCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="47279-115">Ezzel a paranccsal a "Contoso.com" és a "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" a fürthöz a "" nevű írásvédett ügyféltanúsítványt fogja hozzáadni.</span><span class="sxs-lookup"><span data-stu-id="47279-115">This command will add a read only client certificate that's common name is 'Contoso.com' and issuer thumbprint is '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster.</span></span>

## <span data-ttu-id="47279-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="47279-116">PARAMETERS</span></span>

### <span data-ttu-id="47279-117">-Rendszergazda</span><span class="sxs-lookup"><span data-stu-id="47279-117">-Admin</span></span>
<span data-ttu-id="47279-118">Ügyfél-hitelesítés típusa</span><span class="sxs-lookup"><span data-stu-id="47279-118">Client authentication type.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SingleUpdateWithThumbprint, SingleUpdateWithCommonName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47279-119">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="47279-119">-AdminClientThumbprint</span></span>
<span data-ttu-id="47279-120">Adjon meg olyan ügyféltanúsítvány-ujjlenyomatot, amely csak rendszergazdai engedélyekkel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="47279-120">Specify client certificate thumbprint that only has admin permission.</span></span>

```yaml
Type: String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47279-121">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="47279-121">-ClientCertificateCommonName</span></span>
<span data-ttu-id="47279-122">Adja meg az ügyfél köznapi nevét, a kibocsátás-ujjlenyomatot és a hitelesítés típusát.</span><span class="sxs-lookup"><span data-stu-id="47279-122">Specify client common name, issuer thumbprint, and authentication type.</span></span>

```yaml
Type: PSClientCertificateCommonName[]
Parameter Sets: MultipleUpdatesWithCommonName
Aliases: CertCommonName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47279-123">-CommonName</span><span class="sxs-lookup"><span data-stu-id="47279-123">-CommonName</span></span>
<span data-ttu-id="47279-124">Adja meg az ügyfél tanúsítványának köznapi nevét.</span><span class="sxs-lookup"><span data-stu-id="47279-124">Specify client certificate common name.</span></span>

```yaml
Type: String
Parameter Sets: SingleUpdateWithCommonName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47279-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47279-125">-DefaultProfile</span></span>
<span data-ttu-id="47279-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="47279-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47279-127">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="47279-127">-IssuerThumbprint</span></span>
<span data-ttu-id="47279-128">Adja meg az ügyfél tanúsítvány-kibocsátási ujjlenyomatát.</span><span class="sxs-lookup"><span data-stu-id="47279-128">Specify client certificate issuer thumbprint.</span></span>

```yaml
Type: String
Parameter Sets: SingleUpdateWithCommonName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47279-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="47279-129">-Name</span></span>
<span data-ttu-id="47279-130">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="47279-130">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47279-131">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="47279-131">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="47279-132">Adja meg a csak olvasható engedélyt tartalmazó ügyféltanúsítvány-ujjlenyomatot.</span><span class="sxs-lookup"><span data-stu-id="47279-132">Specify client certificate thumbprint that has read only permission.</span></span>

```yaml
Type: String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47279-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47279-133">-ResourceGroupName</span></span>
<span data-ttu-id="47279-134">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="47279-134">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47279-135">-Ujjlenyomat</span><span class="sxs-lookup"><span data-stu-id="47279-135">-Thumbprint</span></span>
<span data-ttu-id="47279-136">Ügyféltanúsítvány-ujjlenyomat megadása</span><span class="sxs-lookup"><span data-stu-id="47279-136">Specify client certificate thumbprint.</span></span>

```yaml
Type: String
Parameter Sets: SingleUpdateWithThumbprint
Aliases: ClientCertificateThumbprint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47279-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="47279-137">-Confirm</span></span>
<span data-ttu-id="47279-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="47279-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47279-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47279-139">-WhatIf</span></span>
<span data-ttu-id="47279-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="47279-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="47279-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="47279-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47279-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47279-142">CommonParameters</span></span>
<span data-ttu-id="47279-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="47279-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47279-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47279-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47279-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="47279-145">INPUTS</span></span>

### <span data-ttu-id="47279-146">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="47279-146">System.Collections.Hashtable</span></span>
<span data-ttu-id="47279-147">System. String</span><span class="sxs-lookup"><span data-stu-id="47279-147">System.String</span></span>

<span data-ttu-id="47279-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="47279-148">System.Boolean</span></span>

## <span data-ttu-id="47279-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="47279-149">OUTPUTS</span></span>

### <span data-ttu-id="47279-150">Microsoft. Azure. Command. ServiceFabric. models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="47279-150">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="47279-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="47279-151">NOTES</span></span>

## <span data-ttu-id="47279-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="47279-152">RELATED LINKS</span></span>

[<span data-ttu-id="47279-153">Remove-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="47279-153">Remove-AzureRmServiceFabricClientCertificate</span></span>](./Remove-AzureRmServiceFabricClientCertificate.md)
