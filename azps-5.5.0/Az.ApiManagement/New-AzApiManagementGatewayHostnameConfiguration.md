---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: 6aadf94ff379df322907be66c73052196de803c5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149610"
---
# <span data-ttu-id="3dbd5-101">New-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="3dbd5-101">New-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="3dbd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3dbd5-102">SYNOPSIS</span></span>
<span data-ttu-id="3dbd5-103">Létrehoz egy állomásnevet konfiguráló kiszolgálót a meglévő átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="3dbd5-103">Creates a hostname configuratin for the existing Gateway.</span></span>

## <span data-ttu-id="3dbd5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3dbd5-104">SYNTAX</span></span>

```
New-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 [-GatewayHostnameConfigurationId <String>] -Hostname <String> -CertificateResourceId <String>
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3dbd5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3dbd5-105">DESCRIPTION</span></span>
<span data-ttu-id="3dbd5-106">A **New-AzApiManagementGatewayHostnameConfiguration parancsmag** létrehoz egy állomásnevet configuratin a meglévő átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="3dbd5-106">The **New-AzApiManagementGatewayHostnameConfiguration** cmdlet creates a hostname configuratin for the existing Gateway.</span></span>

## <span data-ttu-id="3dbd5-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3dbd5-107">EXAMPLES</span></span>

### <span data-ttu-id="3dbd5-108">1. példa: Állomásnév-konfiguráció létrehozása a meglévő átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="3dbd5-108">Example 1: Create a hostname configuration for the existing gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$cert = Get-AzApiManagementCertificate -Context $apimContext -CertificateId "333"
PS C:\>New-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "g01" -GatewayHostnameConfigurationId "h01" -Hostname "www.contoso.com" -CertificateResourceId $cert.Id
```

<span data-ttu-id="3dbd5-109">Ez a parancs egy "h01" állomásnév-konfigurációt hoz létre egy "g01" átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="3dbd5-109">This command creates a "h01" hostname configuration for a "g01" gateway.</span></span>

## <span data-ttu-id="3dbd5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3dbd5-110">PARAMETERS</span></span>

### <span data-ttu-id="3dbd5-111">-CertificateResourceId</span><span class="sxs-lookup"><span data-stu-id="3dbd5-111">-CertificateResourceId</span></span>
<span data-ttu-id="3dbd5-112">A meglévő tanúsítványazonosító erőforrás-azonosítója. Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="3dbd5-112">A resource identifier for the existing certificate id. This parameter is required.</span></span>

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

### <span data-ttu-id="3dbd5-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="3dbd5-113">-Context</span></span>
<span data-ttu-id="3dbd5-114">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="3dbd5-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3dbd5-115">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="3dbd5-115">This parameter is required.</span></span>

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

### <span data-ttu-id="3dbd5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dbd5-116">-DefaultProfile</span></span>
<span data-ttu-id="3dbd5-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3dbd5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3dbd5-118">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="3dbd5-118">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="3dbd5-119">Az új átjáró állomásnevének konkuration azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3dbd5-119">Identifier of new gateway hostname confiuration.</span></span>
<span data-ttu-id="3dbd5-120">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="3dbd5-120">This parameter is optional.</span></span>
<span data-ttu-id="3dbd5-121">Ha nincs megadva, akkor a program létrehoz egy újat.</span><span class="sxs-lookup"><span data-stu-id="3dbd5-121">If not specified will be generated.</span></span>

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

### <span data-ttu-id="3dbd5-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="3dbd5-122">-GatewayId</span></span>
<span data-ttu-id="3dbd5-123">A meglévő átjáró azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3dbd5-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="3dbd5-124">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="3dbd5-124">This parameter is required.</span></span>

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

### <span data-ttu-id="3dbd5-125">-Hostname</span><span class="sxs-lookup"><span data-stu-id="3dbd5-125">-Hostname</span></span>
<span data-ttu-id="3dbd5-126">Állomásnév.</span><span class="sxs-lookup"><span data-stu-id="3dbd5-126">Hostname.</span></span>
<span data-ttu-id="3dbd5-127">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="3dbd5-127">This parameter is required.</span></span>

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

### <span data-ttu-id="3dbd5-128">-NegotiateClientCertificate</span><span class="sxs-lookup"><span data-stu-id="3dbd5-128">-NegotiateClientCertificate</span></span>
<span data-ttu-id="3dbd5-129">Flag to enforce NegotiateClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="3dbd5-129">Flag to enforce NegotiateClientCertificate.</span></span>
<span data-ttu-id="3dbd5-130">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="3dbd5-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="3dbd5-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3dbd5-131">-Confirm</span></span>
<span data-ttu-id="3dbd5-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3dbd5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dbd5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dbd5-133">-WhatIf</span></span>
<span data-ttu-id="3dbd5-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3dbd5-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3dbd5-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3dbd5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dbd5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dbd5-136">CommonParameters</span></span>
<span data-ttu-id="3dbd5-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dbd5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dbd5-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3dbd5-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dbd5-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3dbd5-139">INPUTS</span></span>

### <span data-ttu-id="3dbd5-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3dbd5-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3dbd5-141">System.String</span><span class="sxs-lookup"><span data-stu-id="3dbd5-141">System.String</span></span>

### <span data-ttu-id="3dbd5-142">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3dbd5-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3dbd5-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3dbd5-143">OUTPUTS</span></span>

### <span data-ttu-id="3dbd5-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="3dbd5-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="3dbd5-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3dbd5-145">NOTES</span></span>

## <span data-ttu-id="3dbd5-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3dbd5-146">RELATED LINKS</span></span>
