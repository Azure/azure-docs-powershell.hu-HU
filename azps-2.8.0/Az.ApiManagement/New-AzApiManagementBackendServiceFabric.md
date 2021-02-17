---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendservicefabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendServiceFabric.md
ms.openlocfilehash: 744889e022301951bbc9ba2895eb5750f85925d0
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401657"
---
# <span data-ttu-id="48386-101">New-AzApiManagementBackendServiceFabric</span><span class="sxs-lookup"><span data-stu-id="48386-101">New-AzApiManagementBackendServiceFabric</span></span>

## <span data-ttu-id="48386-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48386-102">SYNOPSIS</span></span>
<span data-ttu-id="48386-103">Objektum létrehozása: `PsApiManagementServiceFabric`</span><span class="sxs-lookup"><span data-stu-id="48386-103">Creates an object of `PsApiManagementServiceFabric`</span></span>

## <span data-ttu-id="48386-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="48386-104">SYNTAX</span></span>

```
New-AzApiManagementBackendServiceFabric -ManagementEndpoint <String[]> -ClientCertificateThumbprint <String>
 [-MaxPartitionResolutionRetry <Int32>] [-ServerX509Name <Hashtable>] [-ServerCertificateThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48386-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="48386-105">DESCRIPTION</span></span>

<span data-ttu-id="48386-106">A **New-AzApiManagementBackendServiceFabric** parancsmag létrehoz egy objektumot, amely a `PsApiManagementServiceFabric` **New-AzApiManagementBackend** és a **Set-AzApiManagementBackend** parancsmagban használható.</span><span class="sxs-lookup"><span data-stu-id="48386-106">The **New-AzApiManagementBackendServiceFabric** cmdlet creates an object of `PsApiManagementServiceFabric` to be used in cmdlet **New-AzApiManagementBackend** and **Set-AzApiManagementBackend**.</span></span>

## <span data-ttu-id="48386-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="48386-107">EXAMPLES</span></span>

### <span data-ttu-id="48386-108">1. példa: Backend Service Fabric In-Memory objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="48386-108">Example 1: Create a Backend Service Fabric In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$ManagementEndpoints = 'https://sfbackend-01.net:443', 'https://sfbackend-02.net:443'
PS C:\>$ServerCertificateThumbprints = '33CC47C6FCA848DC9B14A6F071C1EF7C'
PS C:\>$serviceFabric = New-AzApiManagementBackendServiceFabric -ManagementEndpoint  $ManagementEndpoints -ClientCertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C" -ServerX509Name @{"CN=foobar.net" = @('33CC47C6FCA848DC9B14A6F071C1EF7C'); } -ServerCertificateThumbprint $ServerCertificateThumbprints

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -ServiceFabricCluster $serviceFabric -Description "service fabric backend" -PassThru
```

<span data-ttu-id="48386-109">Backend Service Fabric Contract (Backend Service Fabric Contract) hoz létre</span><span class="sxs-lookup"><span data-stu-id="48386-109">Creates a Backend Service Fabric Contract</span></span>

## <span data-ttu-id="48386-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48386-110">PARAMETERS</span></span>

### <span data-ttu-id="48386-111">-ClientCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="48386-111">-ClientCertificateThumbprint</span></span>
<span data-ttu-id="48386-112">Client Certificate Thumbprint for the management endpoint.</span><span class="sxs-lookup"><span data-stu-id="48386-112">Client Certificate Thumbprint for the management endpoint.</span></span>
<span data-ttu-id="48386-113">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="48386-113">This parameter is required.</span></span>

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

### <span data-ttu-id="48386-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48386-114">-DefaultProfile</span></span>
<span data-ttu-id="48386-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="48386-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48386-116">-ManagementEndpoint</span><span class="sxs-lookup"><span data-stu-id="48386-116">-ManagementEndpoint</span></span>
<span data-ttu-id="48386-117">Service Fabric Cluster management Endpoints.</span><span class="sxs-lookup"><span data-stu-id="48386-117">Service Fabric Cluster management Endpoints.</span></span>
<span data-ttu-id="48386-118">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="48386-118">This parameter is required.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48386-119">-MaxPartitionResolutionRetry</span><span class="sxs-lookup"><span data-stu-id="48386-119">-MaxPartitionResolutionRetry</span></span>
<span data-ttu-id="48386-120">A Service Fabric partíciók feloldásakor a retries maximális száma.</span><span class="sxs-lookup"><span data-stu-id="48386-120">Maximum number of retries when resolving a Service Fabric partition.</span></span>
<span data-ttu-id="48386-121">Ez a paraméter nem kötelező, az alapértelmezett érték pedig 5.</span><span class="sxs-lookup"><span data-stu-id="48386-121">This parameter is optional and default value is 5.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48386-122">-ServerCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="48386-122">-ServerCertificateThumbprint</span></span>
<span data-ttu-id="48386-123">A tanúsítványok fürtkezelési szolgáltatásának thumbprint of certificates cluster management service uses for tls communication. Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="48386-123">Thumbprint of certificates cluster management service uses for tls communication.This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48386-124">-ServerX509Name</span><span class="sxs-lookup"><span data-stu-id="48386-124">-ServerX509Name</span></span>
<span data-ttu-id="48386-125">Server X509 Certificate Names Collection.</span><span class="sxs-lookup"><span data-stu-id="48386-125">Server X509 Certificate Names Collection.</span></span>
<span data-ttu-id="48386-126">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="48386-126">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48386-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48386-127">CommonParameters</span></span>
<span data-ttu-id="48386-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48386-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48386-129">További információt a [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48386-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48386-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="48386-130">INPUTS</span></span>

### <span data-ttu-id="48386-131">System.String</span><span class="sxs-lookup"><span data-stu-id="48386-131">System.String</span></span>

## <span data-ttu-id="48386-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="48386-132">OUTPUTS</span></span>

### <span data-ttu-id="48386-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="48386-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="48386-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="48386-134">NOTES</span></span>

## <span data-ttu-id="48386-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="48386-135">RELATED LINKS</span></span>

[<span data-ttu-id="48386-136">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="48386-136">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="48386-137">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="48386-137">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="48386-138">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="48386-138">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="48386-139">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="48386-139">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="48386-140">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="48386-140">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
