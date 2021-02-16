---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
ms.openlocfilehash: c7a88cad933781b00e720c273be467966991cebf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165882"
---
# <span data-ttu-id="03292-101">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="03292-101">Remove-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="03292-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03292-102">SYNOPSIS</span></span>
<span data-ttu-id="03292-103">Távolítsa el az ügyfél-tanúsítvány(ok) vagy a tanúsítvány tulajdonosának(ok) nevét az ügyfél-hitelesítéshez a fürtre való ügyfélalkalmazás-hitelesítéshez.</span><span class="sxs-lookup"><span data-stu-id="03292-103">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="03292-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="03292-104">SYNTAX</span></span>

### <span data-ttu-id="03292-105">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="03292-105">SingleUpdateWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -CommonName <String>
 -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="03292-106">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="03292-106">SingleUpdateWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03292-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="03292-107">MultipleUpdatesWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03292-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="03292-108">MultipleUpdatesWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03292-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="03292-109">DESCRIPTION</span></span>
<span data-ttu-id="03292-110">A **Remove-AzServiceFabricClientCertificate** segítségével eltávolíthatja az ügyféltanúsítvány(ok) vagy a tanúsítvány tulajdonosának(ok) nevét a fürtre való ügyfél-hitelesítéshez.</span><span class="sxs-lookup"><span data-stu-id="03292-110">Use **Remove-AzServiceFabricClientCertificate** to remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="03292-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="03292-111">EXAMPLES</span></span>

### <span data-ttu-id="03292-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="03292-112">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="03292-113">Ez a parancs eltávolítja az "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" nyomatot a fürtből.</span><span class="sxs-lookup"><span data-stu-id="03292-113">This command will remove client certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' from the cluster.</span></span>

## <span data-ttu-id="03292-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03292-114">PARAMETERS</span></span>

### <span data-ttu-id="03292-115">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="03292-115">-AdminClientThumbprint</span></span>
<span data-ttu-id="03292-116">Az ügyfél tanúsítványának thumbprint megadása, amely csak rendszergazdai engedéllyel rendelkezik</span><span class="sxs-lookup"><span data-stu-id="03292-116">Specify client certificate thumbprint which only has admin permission</span></span>

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

### <span data-ttu-id="03292-117">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="03292-117">-ClientCertificateCommonName</span></span>
<span data-ttu-id="03292-118">Az ügyfél általános nevének, a kibocsátó hüvelykujjának és a hitelesítés típusának megadása</span><span class="sxs-lookup"><span data-stu-id="03292-118">Specify client common name , issuer thumbprint and authentication type</span></span>

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

### <span data-ttu-id="03292-119">-CommonName</span><span class="sxs-lookup"><span data-stu-id="03292-119">-CommonName</span></span>
<span data-ttu-id="03292-120">Az ügyfél tanúsítványának általános nevének megadása</span><span class="sxs-lookup"><span data-stu-id="03292-120">Specify client certificate common name</span></span>

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

### <span data-ttu-id="03292-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03292-121">-DefaultProfile</span></span>
<span data-ttu-id="03292-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="03292-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03292-123">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="03292-123">-IssuerThumbprint</span></span>
<span data-ttu-id="03292-124">Az ügyfél-tanúsítvány kibocsátójának thumbprintjának megadása</span><span class="sxs-lookup"><span data-stu-id="03292-124">Specify thumbprint of client certificate's issuer</span></span>

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

### <span data-ttu-id="03292-125">-Name</span><span class="sxs-lookup"><span data-stu-id="03292-125">-Name</span></span>
<span data-ttu-id="03292-126">A fürt nevének megadása</span><span class="sxs-lookup"><span data-stu-id="03292-126">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="03292-127">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="03292-127">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="03292-128">Az ügyfél tanúsítványának thumbprint megadása, amely csak olvasási engedéllyel rendelkezik</span><span class="sxs-lookup"><span data-stu-id="03292-128">Specify client certificate thumbprint which only has read only permission</span></span>

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

### <span data-ttu-id="03292-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03292-129">-ResourceGroupName</span></span>
<span data-ttu-id="03292-130">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="03292-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="03292-131">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="03292-131">-Thumbprint</span></span>
<span data-ttu-id="03292-132">Ügyfél tanúsítványának thumbprint megadása</span><span class="sxs-lookup"><span data-stu-id="03292-132">Specify client certificate thumbprint</span></span>

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

### <span data-ttu-id="03292-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03292-133">-Confirm</span></span>
<span data-ttu-id="03292-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="03292-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03292-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03292-135">-WhatIf</span></span>
<span data-ttu-id="03292-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="03292-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03292-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="03292-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03292-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03292-138">CommonParameters</span></span>
<span data-ttu-id="03292-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03292-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03292-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="03292-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03292-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="03292-141">INPUTS</span></span>

### <span data-ttu-id="03292-142">System.String</span><span class="sxs-lookup"><span data-stu-id="03292-142">System.String</span></span>

### <span data-ttu-id="03292-143">System.String[]</span><span class="sxs-lookup"><span data-stu-id="03292-143">System.String[]</span></span>

### <span data-ttu-id="03292-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span><span class="sxs-lookup"><span data-stu-id="03292-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="03292-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="03292-145">OUTPUTS</span></span>

### <span data-ttu-id="03292-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="03292-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="03292-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="03292-147">NOTES</span></span>

## <span data-ttu-id="03292-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="03292-148">RELATED LINKS</span></span>

[<span data-ttu-id="03292-149">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="03292-149">Add-AzServiceFabricClientCertificate</span></span>](./Add-AzServiceFabricClientCertificate.md)
