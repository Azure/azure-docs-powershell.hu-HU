---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
ms.openlocfilehash: ca9dbbba29e6f770b727e1f96717c2626f112839
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479591"
---
# <span data-ttu-id="6328d-101">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="6328d-101">Add-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="6328d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6328d-102">SYNOPSIS</span></span>
<span data-ttu-id="6328d-103">Az ügyfélhitelesítési célokból adjon hozzá általános nevet vagy thumbprint-et a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="6328d-103">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="6328d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6328d-104">SYNTAX</span></span>

### <span data-ttu-id="6328d-105">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="6328d-105">SingleUpdateWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6328d-106">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="6328d-106">SingleUpdateWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6328d-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="6328d-107">MultipleUpdatesWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6328d-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="6328d-108">MultipleUpdatesWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6328d-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6328d-109">DESCRIPTION</span></span>
<span data-ttu-id="6328d-110">Az **Add-AzServiceFabricClientCertificate** segítségével adjon hozzá egy általános nevet és egy kibocsátó thumbprint-ját vagy tanúsítvány-thumbprint-ját a fürthöz, hogy az ügyfél fel tudja használni hitelesítésre.</span><span class="sxs-lookup"><span data-stu-id="6328d-110">Use **Add-AzServiceFabricClientCertificate** to add a common name and issuer thumbprint or certificate thumbprint to the cluster, so the client can use it for authentication.</span></span>

## <span data-ttu-id="6328d-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6328d-111">EXAMPLES</span></span>

### <span data-ttu-id="6328d-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="6328d-112">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="6328d-113">Ez a parancs hozzáadja a "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" hüvelykujjú tanúsítványt a fürthöz, hogy az ügyfél rendszergazdaként használva kommunikáljon a fürtbel.</span><span class="sxs-lookup"><span data-stu-id="6328d-113">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="6328d-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="6328d-114">Example 2</span></span>
```
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="6328d-115">Ez a parancs a "Contoso.com" nevű írásos ügyfélalkalmazási tanúsítványt, a kibocsátó pedig az "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" nyomatot adja a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="6328d-115">This command will add a read only client certificate that's common name is 'Contoso.com' and issuer thumbprint is '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster.</span></span>

## <span data-ttu-id="6328d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6328d-116">PARAMETERS</span></span>

### <span data-ttu-id="6328d-117">-Admin</span><span class="sxs-lookup"><span data-stu-id="6328d-117">-Admin</span></span>
<span data-ttu-id="6328d-118">Ügyfél-hitelesítés típusa</span><span class="sxs-lookup"><span data-stu-id="6328d-118">Client authentication type</span></span>

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

### <span data-ttu-id="6328d-119">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="6328d-119">-AdminClientThumbprint</span></span>
<span data-ttu-id="6328d-120">Az ügyfél tanúsítványának thumbprint megadása, amely csak rendszergazdai engedéllyel rendelkezik</span><span class="sxs-lookup"><span data-stu-id="6328d-120">Specify client certificate thumbprint which only has admin permission</span></span>

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

### <span data-ttu-id="6328d-121">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="6328d-121">-ClientCertificateCommonName</span></span>
<span data-ttu-id="6328d-122">Az ügyfél általános nevének, a kibocsátó hüvelykujjának és a hitelesítés típusának megadása</span><span class="sxs-lookup"><span data-stu-id="6328d-122">Specify client common name , issuer thumbprint and authentication type</span></span>

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

### <span data-ttu-id="6328d-123">-CommonName</span><span class="sxs-lookup"><span data-stu-id="6328d-123">-CommonName</span></span>
<span data-ttu-id="6328d-124">Az ügyfél tanúsítványának általános nevének megadása</span><span class="sxs-lookup"><span data-stu-id="6328d-124">Specify client certificate common name</span></span>

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

### <span data-ttu-id="6328d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6328d-125">-DefaultProfile</span></span>
<span data-ttu-id="6328d-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6328d-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6328d-127">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="6328d-127">-IssuerThumbprint</span></span>
<span data-ttu-id="6328d-128">Az ügyfél-tanúsítvány kibocsátójának thumbprintjának megadása</span><span class="sxs-lookup"><span data-stu-id="6328d-128">Specify thumbprint of client certificate's issuer</span></span>

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

### <span data-ttu-id="6328d-129">-Name</span><span class="sxs-lookup"><span data-stu-id="6328d-129">-Name</span></span>
<span data-ttu-id="6328d-130">A fürt nevének megadása</span><span class="sxs-lookup"><span data-stu-id="6328d-130">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="6328d-131">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="6328d-131">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="6328d-132">Az ügyfél tanúsítványának thumbprint megadása, amely csak olvasási engedéllyel rendelkezik</span><span class="sxs-lookup"><span data-stu-id="6328d-132">Specify client certificate thumbprint which only has read only permission</span></span>

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

### <span data-ttu-id="6328d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6328d-133">-ResourceGroupName</span></span>
<span data-ttu-id="6328d-134">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="6328d-134">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="6328d-135">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="6328d-135">-Thumbprint</span></span>
<span data-ttu-id="6328d-136">Ügyfél tanúsítványának thumbprint megadása</span><span class="sxs-lookup"><span data-stu-id="6328d-136">Specify client certificate thumbprint</span></span>

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

### <span data-ttu-id="6328d-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6328d-137">-Confirm</span></span>
<span data-ttu-id="6328d-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6328d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6328d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6328d-139">-WhatIf</span></span>
<span data-ttu-id="6328d-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6328d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6328d-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6328d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6328d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6328d-142">CommonParameters</span></span>
<span data-ttu-id="6328d-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6328d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6328d-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6328d-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6328d-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6328d-145">INPUTS</span></span>

### <span data-ttu-id="6328d-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6328d-146">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="6328d-147">System.String</span><span class="sxs-lookup"><span data-stu-id="6328d-147">System.String</span></span>

### <span data-ttu-id="6328d-148">System.String[]</span><span class="sxs-lookup"><span data-stu-id="6328d-148">System.String[]</span></span>

### <span data-ttu-id="6328d-149">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span><span class="sxs-lookup"><span data-stu-id="6328d-149">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="6328d-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6328d-150">OUTPUTS</span></span>

### <span data-ttu-id="6328d-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="6328d-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="6328d-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6328d-152">NOTES</span></span>

## <span data-ttu-id="6328d-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6328d-153">RELATED LINKS</span></span>

[<span data-ttu-id="6328d-154">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="6328d-154">Remove-AzServiceFabricClientCertificate</span></span>](./Remove-AzServiceFabricClientCertificate.md)
