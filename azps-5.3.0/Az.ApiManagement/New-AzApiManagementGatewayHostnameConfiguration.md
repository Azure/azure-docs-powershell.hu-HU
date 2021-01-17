---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: 6aadf94ff379df322907be66c73052196de803c5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478813"
---
# <span data-ttu-id="8406d-101">New-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="8406d-101">New-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="8406d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8406d-102">SYNOPSIS</span></span>
<span data-ttu-id="8406d-103">Létrehoz egy állomásnevet konfiguráló kiszolgálót a meglévő átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="8406d-103">Creates a hostname configuratin for the existing Gateway.</span></span>

## <span data-ttu-id="8406d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8406d-104">SYNTAX</span></span>

```
New-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 [-GatewayHostnameConfigurationId <String>] -Hostname <String> -CertificateResourceId <String>
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8406d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8406d-105">DESCRIPTION</span></span>
<span data-ttu-id="8406d-106">A **New-AzApiManagementGatewayHostnameConfiguration parancsmag** létrehoz egy állomásnevet configuratin a meglévő átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="8406d-106">The **New-AzApiManagementGatewayHostnameConfiguration** cmdlet creates a hostname configuratin for the existing Gateway.</span></span>

## <span data-ttu-id="8406d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8406d-107">EXAMPLES</span></span>

### <span data-ttu-id="8406d-108">1. példa: Állomásnév-konfiguráció létrehozása a meglévő átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="8406d-108">Example 1: Create a hostname configuration for the existing gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$cert = Get-AzApiManagementCertificate -Context $apimContext -CertificateId "333"
PS C:\>New-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "g01" -GatewayHostnameConfigurationId "h01" -Hostname "www.contoso.com" -CertificateResourceId $cert.Id
```

<span data-ttu-id="8406d-109">Ez a parancs egy "h01" állomásnév-konfigurációt hoz létre egy "g01" átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="8406d-109">This command creates a "h01" hostname configuration for a "g01" gateway.</span></span>

## <span data-ttu-id="8406d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8406d-110">PARAMETERS</span></span>

### <span data-ttu-id="8406d-111">-CertificateResourceId</span><span class="sxs-lookup"><span data-stu-id="8406d-111">-CertificateResourceId</span></span>
<span data-ttu-id="8406d-112">A meglévő tanúsítványazonosító erőforrás-azonosítója. Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="8406d-112">A resource identifier for the existing certificate id. This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8406d-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="8406d-113">-Context</span></span>
<span data-ttu-id="8406d-114">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="8406d-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="8406d-115">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="8406d-115">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8406d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8406d-116">-DefaultProfile</span></span>
<span data-ttu-id="8406d-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8406d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8406d-118">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="8406d-118">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="8406d-119">Az új átjáró állomásnevének konkuration azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8406d-119">Identifier of new gateway hostname confiuration.</span></span>
<span data-ttu-id="8406d-120">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="8406d-120">This parameter is optional.</span></span>
<span data-ttu-id="8406d-121">Ha nincs megadva, akkor a program létrehoz egy újat.</span><span class="sxs-lookup"><span data-stu-id="8406d-121">If not specified will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8406d-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="8406d-122">-GatewayId</span></span>
<span data-ttu-id="8406d-123">A meglévő átjáró azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8406d-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="8406d-124">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="8406d-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8406d-125">-Hostname</span><span class="sxs-lookup"><span data-stu-id="8406d-125">-Hostname</span></span>
<span data-ttu-id="8406d-126">Állomásnév.</span><span class="sxs-lookup"><span data-stu-id="8406d-126">Hostname.</span></span>
<span data-ttu-id="8406d-127">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="8406d-127">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8406d-128">-NegotiateClientCertificate</span><span class="sxs-lookup"><span data-stu-id="8406d-128">-NegotiateClientCertificate</span></span>
<span data-ttu-id="8406d-129">Flag to enforce NegotiateClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="8406d-129">Flag to enforce NegotiateClientCertificate.</span></span>
<span data-ttu-id="8406d-130">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="8406d-130">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8406d-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8406d-131">-Confirm</span></span>
<span data-ttu-id="8406d-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8406d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8406d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8406d-133">-WhatIf</span></span>
<span data-ttu-id="8406d-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8406d-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8406d-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8406d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8406d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8406d-136">CommonParameters</span></span>
<span data-ttu-id="8406d-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8406d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8406d-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8406d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8406d-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8406d-139">INPUTS</span></span>

### <span data-ttu-id="8406d-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8406d-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8406d-141">System.String</span><span class="sxs-lookup"><span data-stu-id="8406d-141">System.String</span></span>

### <span data-ttu-id="8406d-142">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8406d-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8406d-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8406d-143">OUTPUTS</span></span>

### <span data-ttu-id="8406d-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="8406d-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="8406d-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8406d-145">NOTES</span></span>

## <span data-ttu-id="8406d-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8406d-146">RELATED LINKS</span></span>
