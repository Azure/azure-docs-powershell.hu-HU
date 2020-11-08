---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: 6aadf94ff379df322907be66c73052196de803c5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180662"
---
# <span data-ttu-id="89478-101">New-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="89478-101">New-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="89478-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="89478-102">SYNOPSIS</span></span>
<span data-ttu-id="89478-103">A meglévő átjáróhoz tartozó hostname configuratin hoz létre.</span><span class="sxs-lookup"><span data-stu-id="89478-103">Creates a hostname configuratin for the existing Gateway.</span></span>

## <span data-ttu-id="89478-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="89478-104">SYNTAX</span></span>

```
New-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 [-GatewayHostnameConfigurationId <String>] -Hostname <String> -CertificateResourceId <String>
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="89478-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="89478-105">DESCRIPTION</span></span>
<span data-ttu-id="89478-106">A **New-AzApiManagementGatewayHostnameConfiguration** parancsmag létrehoz egy gépnév configuratin a meglévő átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="89478-106">The **New-AzApiManagementGatewayHostnameConfiguration** cmdlet creates a hostname configuratin for the existing Gateway.</span></span>

## <span data-ttu-id="89478-107">Példák</span><span class="sxs-lookup"><span data-stu-id="89478-107">EXAMPLES</span></span>

### <span data-ttu-id="89478-108">Példa 1: a meglévő átjáró gépnév-konfigurációjának létrehozása</span><span class="sxs-lookup"><span data-stu-id="89478-108">Example 1: Create a hostname configuration for the existing gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$cert = Get-AzApiManagementCertificate -Context $apimContext -CertificateId "333"
PS C:\>New-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "g01" -GatewayHostnameConfigurationId "h01" -Hostname "www.contoso.com" -CertificateResourceId $cert.Id
```

<span data-ttu-id="89478-109">Ez a parancs létrehoz egy "h01" gépnév-konfigurációt egy "G01" átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="89478-109">This command creates a "h01" hostname configuration for a "g01" gateway.</span></span>

## <span data-ttu-id="89478-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="89478-110">PARAMETERS</span></span>

### <span data-ttu-id="89478-111">-CertificateResourceId</span><span class="sxs-lookup"><span data-stu-id="89478-111">-CertificateResourceId</span></span>
<span data-ttu-id="89478-112">A meglévő tanúsítvány erőforrás-azonosítója. Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="89478-112">A resource identifier for the existing certificate id. This parameter is required.</span></span>

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

### <span data-ttu-id="89478-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="89478-113">-Context</span></span>
<span data-ttu-id="89478-114">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="89478-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="89478-115">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="89478-115">This parameter is required.</span></span>

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

### <span data-ttu-id="89478-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89478-116">-DefaultProfile</span></span>
<span data-ttu-id="89478-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="89478-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89478-118">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="89478-118">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="89478-119">A hostname Confiuration új átjárójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="89478-119">Identifier of new gateway hostname confiuration.</span></span>
<span data-ttu-id="89478-120">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="89478-120">This parameter is optional.</span></span>
<span data-ttu-id="89478-121">Ha a program nem adja meg a megadott értéket.</span><span class="sxs-lookup"><span data-stu-id="89478-121">If not specified will be generated.</span></span>

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

### <span data-ttu-id="89478-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="89478-122">-GatewayId</span></span>
<span data-ttu-id="89478-123">A meglévő átjáró azonosítója</span><span class="sxs-lookup"><span data-stu-id="89478-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="89478-124">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="89478-124">This parameter is required.</span></span>

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

### <span data-ttu-id="89478-125">-Hostname (állomásnév)</span><span class="sxs-lookup"><span data-stu-id="89478-125">-Hostname</span></span>
<span data-ttu-id="89478-126">Hostname.</span><span class="sxs-lookup"><span data-stu-id="89478-126">Hostname.</span></span>
<span data-ttu-id="89478-127">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="89478-127">This parameter is required.</span></span>

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

### <span data-ttu-id="89478-128">-NegotiateClientCertificate</span><span class="sxs-lookup"><span data-stu-id="89478-128">-NegotiateClientCertificate</span></span>
<span data-ttu-id="89478-129">Jelölő a NegotiateClientCertificate érvényesítéséhez.</span><span class="sxs-lookup"><span data-stu-id="89478-129">Flag to enforce NegotiateClientCertificate.</span></span>
<span data-ttu-id="89478-130">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="89478-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="89478-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="89478-131">-Confirm</span></span>
<span data-ttu-id="89478-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="89478-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89478-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89478-133">-WhatIf</span></span>
<span data-ttu-id="89478-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="89478-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="89478-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="89478-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89478-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89478-136">CommonParameters</span></span>
<span data-ttu-id="89478-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="89478-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89478-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="89478-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89478-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="89478-139">INPUTS</span></span>

### <span data-ttu-id="89478-140">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="89478-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="89478-141">System. String</span><span class="sxs-lookup"><span data-stu-id="89478-141">System.String</span></span>

### <span data-ttu-id="89478-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="89478-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="89478-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="89478-143">OUTPUTS</span></span>

### <span data-ttu-id="89478-144">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="89478-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="89478-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="89478-145">NOTES</span></span>

## <span data-ttu-id="89478-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="89478-146">RELATED LINKS</span></span>
