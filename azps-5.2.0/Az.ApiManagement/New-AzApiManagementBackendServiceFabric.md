---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendservicefabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendServiceFabric.md
ms.openlocfilehash: 352e40aa64adf5eea98950ac9271f0237e634ab6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331937"
---
# <span data-ttu-id="fdbfa-101">New-AzApiManagementBackendServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fdbfa-101">New-AzApiManagementBackendServiceFabric</span></span>

## <span data-ttu-id="fdbfa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdbfa-102">SYNOPSIS</span></span>
<span data-ttu-id="fdbfa-103">Objektum létrehozása: `PsApiManagementServiceFabric`</span><span class="sxs-lookup"><span data-stu-id="fdbfa-103">Creates an object of `PsApiManagementServiceFabric`</span></span>

## <span data-ttu-id="fdbfa-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fdbfa-104">SYNTAX</span></span>

```
New-AzApiManagementBackendServiceFabric -ManagementEndpoint <String[]> -ClientCertificateThumbprint <String>
 [-MaxPartitionResolutionRetry <Int32>] [-ServerX509Name <Hashtable>] [-ServerCertificateThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdbfa-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fdbfa-105">DESCRIPTION</span></span>

<span data-ttu-id="fdbfa-106">A **New-AzApiManagementBackendServiceFabric** parancsmag létrehoz egy objektumot, amely a `PsApiManagementServiceFabric` **New-AzApiManagementBackend** és a **Set-AzApiManagementBackend** parancsmagban használható.</span><span class="sxs-lookup"><span data-stu-id="fdbfa-106">The **New-AzApiManagementBackendServiceFabric** cmdlet creates an object of `PsApiManagementServiceFabric` to be used in cmdlet **New-AzApiManagementBackend** and **Set-AzApiManagementBackend**.</span></span>

## <span data-ttu-id="fdbfa-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fdbfa-107">EXAMPLES</span></span>

### <span data-ttu-id="fdbfa-108">1. példa: Backend Service Fabric In-Memory objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="fdbfa-108">Example 1: Create a Backend Service Fabric In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$ManagementEndpoints = 'https://sfbackend-01.net:443', 'https://sfbackend-02.net:443'
PS C:\>$ServerCertificateThumbprints = '33CC47C6FCA848DC9B14A6F071C1EF7C'
PS C:\>$serviceFabric = New-AzApiManagementBackendServiceFabric -ManagementEndpoint  $ManagementEndpoints -ClientCertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C" -ServerX509Name @{"CN=foobar.net" = @('33CC47C6FCA848DC9B14A6F071C1EF7C'); } -ServerCertificateThumbprint $ServerCertificateThumbprints

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -ServiceFabricCluster $serviceFabric -Description "service fabric backend" -PassThru
```

<span data-ttu-id="fdbfa-109">Backend Service Fabric Contract (Backend Service Fabric Contract) hoz létre</span><span class="sxs-lookup"><span data-stu-id="fdbfa-109">Creates a Backend Service Fabric Contract</span></span>

## <span data-ttu-id="fdbfa-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fdbfa-110">PARAMETERS</span></span>

### <span data-ttu-id="fdbfa-111">-ClientCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="fdbfa-111">-ClientCertificateThumbprint</span></span>
<span data-ttu-id="fdbfa-112">Client Certificate Thumbprint for the management endpoint.</span><span class="sxs-lookup"><span data-stu-id="fdbfa-112">Client Certificate Thumbprint for the management endpoint.</span></span>
<span data-ttu-id="fdbfa-113">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="fdbfa-113">This parameter is required.</span></span>

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

### <span data-ttu-id="fdbfa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdbfa-114">-DefaultProfile</span></span>
<span data-ttu-id="fdbfa-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fdbfa-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdbfa-116">-ManagementEndpoint</span><span class="sxs-lookup"><span data-stu-id="fdbfa-116">-ManagementEndpoint</span></span>
<span data-ttu-id="fdbfa-117">Service Fabric Cluster management Endpoints.</span><span class="sxs-lookup"><span data-stu-id="fdbfa-117">Service Fabric Cluster management Endpoints.</span></span>
<span data-ttu-id="fdbfa-118">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="fdbfa-118">This parameter is required.</span></span>

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

### <span data-ttu-id="fdbfa-119">-MaxPartitionResolutionRetry</span><span class="sxs-lookup"><span data-stu-id="fdbfa-119">-MaxPartitionResolutionRetry</span></span>
<span data-ttu-id="fdbfa-120">Retries maximális száma Service Fabric partíció feloldásakor.</span><span class="sxs-lookup"><span data-stu-id="fdbfa-120">Maximum number of retries when resolving a Service Fabric partition.</span></span>
<span data-ttu-id="fdbfa-121">Ez a paraméter nem kötelező, az alapértelmezett érték pedig 5.</span><span class="sxs-lookup"><span data-stu-id="fdbfa-121">This parameter is optional and default value is 5.</span></span>

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

### <span data-ttu-id="fdbfa-122">-ServerCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="fdbfa-122">-ServerCertificateThumbprint</span></span>
<span data-ttu-id="fdbfa-123">A tanúsítványok fürtkezelési szolgáltatásának thumbprint of certificates cluster management service uses for tls communication. Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="fdbfa-123">Thumbprint of certificates cluster management service uses for tls communication.This parameter is optional.</span></span>

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

### <span data-ttu-id="fdbfa-124">-ServerX509Name</span><span class="sxs-lookup"><span data-stu-id="fdbfa-124">-ServerX509Name</span></span>
<span data-ttu-id="fdbfa-125">Server X509 Certificate Names Collection.</span><span class="sxs-lookup"><span data-stu-id="fdbfa-125">Server X509 Certificate Names Collection.</span></span>
<span data-ttu-id="fdbfa-126">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="fdbfa-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="fdbfa-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdbfa-127">CommonParameters</span></span>
<span data-ttu-id="fdbfa-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdbfa-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdbfa-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fdbfa-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdbfa-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fdbfa-130">INPUTS</span></span>

### <span data-ttu-id="fdbfa-131">System.String</span><span class="sxs-lookup"><span data-stu-id="fdbfa-131">System.String</span></span>

## <span data-ttu-id="fdbfa-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fdbfa-132">OUTPUTS</span></span>

### <span data-ttu-id="fdbfa-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fdbfa-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="fdbfa-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fdbfa-134">NOTES</span></span>

## <span data-ttu-id="fdbfa-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fdbfa-135">RELATED LINKS</span></span>

[<span data-ttu-id="fdbfa-136">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="fdbfa-136">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="fdbfa-137">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="fdbfa-137">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="fdbfa-138">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="fdbfa-138">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="fdbfa-139">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="fdbfa-139">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="fdbfa-140">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="fdbfa-140">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
