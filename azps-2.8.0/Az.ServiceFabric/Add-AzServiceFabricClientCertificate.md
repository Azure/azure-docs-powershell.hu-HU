---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
ms.openlocfilehash: de43485cc4504d8819e16e121bb94a29ae6b650a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838015"
---
# <span data-ttu-id="4d77a-101">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="4d77a-101">Add-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="4d77a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4d77a-102">SYNOPSIS</span></span>
<span data-ttu-id="4d77a-103">Az ügyfél-hitelesítéshez adjon meg köznapi nevet vagy ujjlenyomatot a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="4d77a-103">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="4d77a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4d77a-104">SYNTAX</span></span>

### <span data-ttu-id="4d77a-105">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="4d77a-105">SingleUpdateWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d77a-106">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="4d77a-106">SingleUpdateWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d77a-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="4d77a-107">MultipleUpdatesWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d77a-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="4d77a-108">MultipleUpdatesWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d77a-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="4d77a-109">DESCRIPTION</span></span>
<span data-ttu-id="4d77a-110">A **Add-AzServiceFabricClientCertificate** használatával felvehet egy köznapi nevet és egy kiállított ujjlenyomatot vagy egy tanúsítvány ujjlenyomatát a fürthöz, így az ügyfél használhatja azt hitelesítésre.</span><span class="sxs-lookup"><span data-stu-id="4d77a-110">Use **Add-AzServiceFabricClientCertificate** to add a common name and issuer thumbprint or certificate thumbprint to the cluster, so the client can use it for authentication.</span></span>

## <span data-ttu-id="4d77a-111">Példák</span><span class="sxs-lookup"><span data-stu-id="4d77a-111">EXAMPLES</span></span>

### <span data-ttu-id="4d77a-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4d77a-112">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="4d77a-113">Ez a parancs hozzáadja a "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" ujjlenyomatot a fürthöz, így az ügyfél a tanúsítványt rendszergazdaként használhatja a fürttel való kommunikációhoz.</span><span class="sxs-lookup"><span data-stu-id="4d77a-113">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="4d77a-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="4d77a-114">Example 2</span></span>
```
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="4d77a-115">Ezzel a paranccsal a "Contoso.com" és a "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" a fürthöz a "" nevű írásvédett ügyféltanúsítványt fogja hozzáadni.</span><span class="sxs-lookup"><span data-stu-id="4d77a-115">This command will add a read only client certificate that's common name is 'Contoso.com' and issuer thumbprint is '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster.</span></span>

## <span data-ttu-id="4d77a-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4d77a-116">PARAMETERS</span></span>

### <span data-ttu-id="4d77a-117">-Rendszergazda</span><span class="sxs-lookup"><span data-stu-id="4d77a-117">-Admin</span></span>
<span data-ttu-id="4d77a-118">Ügyfél-hitelesítés típusa</span><span class="sxs-lookup"><span data-stu-id="4d77a-118">Client authentication type</span></span>

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

### <span data-ttu-id="4d77a-119">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="4d77a-119">-AdminClientThumbprint</span></span>
<span data-ttu-id="4d77a-120">A csak rendszergazdai engedélyekkel rendelkező ügyféltanúsítvány-ujjlenyomat megadása</span><span class="sxs-lookup"><span data-stu-id="4d77a-120">Specify client certificate thumbprint which only has admin permission</span></span>

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

### <span data-ttu-id="4d77a-121">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="4d77a-121">-ClientCertificateCommonName</span></span>
<span data-ttu-id="4d77a-122">Az ügyfél köznapi nevének, a kibocsátások ujjlenyomatának és a hitelesítés típusának megadása</span><span class="sxs-lookup"><span data-stu-id="4d77a-122">Specify client common name , issuer thumbprint and authentication type</span></span>

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

### <span data-ttu-id="4d77a-123">-CommonName</span><span class="sxs-lookup"><span data-stu-id="4d77a-123">-CommonName</span></span>
<span data-ttu-id="4d77a-124">Ügyféltanúsítvány-köznapi név megadása</span><span class="sxs-lookup"><span data-stu-id="4d77a-124">Specify client certificate common name</span></span>

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

### <span data-ttu-id="4d77a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d77a-125">-DefaultProfile</span></span>
<span data-ttu-id="4d77a-126">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4d77a-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d77a-127">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="4d77a-127">-IssuerThumbprint</span></span>
<span data-ttu-id="4d77a-128">Adja meg az ügyfél tanúsítványának ujjlenyomatát</span><span class="sxs-lookup"><span data-stu-id="4d77a-128">Specify thumbprint of client certificate's issuer</span></span>

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

### <span data-ttu-id="4d77a-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4d77a-129">-Name</span></span>
<span data-ttu-id="4d77a-130">A fürt nevének megadása</span><span class="sxs-lookup"><span data-stu-id="4d77a-130">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="4d77a-131">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="4d77a-131">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="4d77a-132">Adja meg az ügyféltanúsítvány-ujjlenyomatot, amely csak írásvédett engedélyt tartalmaz</span><span class="sxs-lookup"><span data-stu-id="4d77a-132">Specify client certificate thumbprint which only has read only permission</span></span>

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

### <span data-ttu-id="4d77a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d77a-133">-ResourceGroupName</span></span>
<span data-ttu-id="4d77a-134">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="4d77a-134">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="4d77a-135">-Ujjlenyomat</span><span class="sxs-lookup"><span data-stu-id="4d77a-135">-Thumbprint</span></span>
<span data-ttu-id="4d77a-136">Ügyféltanúsítvány ujjlenyomatának megadása</span><span class="sxs-lookup"><span data-stu-id="4d77a-136">Specify client certificate thumbprint</span></span>

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

### <span data-ttu-id="4d77a-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4d77a-137">-Confirm</span></span>
<span data-ttu-id="4d77a-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4d77a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d77a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d77a-139">-WhatIf</span></span>
<span data-ttu-id="4d77a-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4d77a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d77a-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4d77a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d77a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d77a-142">CommonParameters</span></span>
<span data-ttu-id="4d77a-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4d77a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d77a-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d77a-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d77a-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d77a-145">INPUTS</span></span>

### <span data-ttu-id="4d77a-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4d77a-146">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="4d77a-147">System. String</span><span class="sxs-lookup"><span data-stu-id="4d77a-147">System.String</span></span>

### <span data-ttu-id="4d77a-148">System. string []</span><span class="sxs-lookup"><span data-stu-id="4d77a-148">System.String[]</span></span>

### <span data-ttu-id="4d77a-149">Microsoft. Azure. Command. ServiceFabric. models. PSClientCertificateCommonName []</span><span class="sxs-lookup"><span data-stu-id="4d77a-149">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="4d77a-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d77a-150">OUTPUTS</span></span>

### <span data-ttu-id="4d77a-151">Microsoft. Azure. Command. ServiceFabric. models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="4d77a-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="4d77a-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4d77a-152">NOTES</span></span>

## <span data-ttu-id="4d77a-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4d77a-153">RELATED LINKS</span></span>

[<span data-ttu-id="4d77a-154">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="4d77a-154">Remove-AzServiceFabricClientCertificate</span></span>](./Remove-AzServiceFabricClientCertificate.md)
