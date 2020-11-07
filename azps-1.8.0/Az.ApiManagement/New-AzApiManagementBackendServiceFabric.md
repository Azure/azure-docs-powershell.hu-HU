---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendservicefabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendServiceFabric.md
ms.openlocfilehash: 193f8f64abee3514d94a0f825beb7190c8ea7fa6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665640"
---
# <span data-ttu-id="4dc1c-101">New-AzApiManagementBackendServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4dc1c-101">New-AzApiManagementBackendServiceFabric</span></span>

## <span data-ttu-id="4dc1c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4dc1c-102">SYNOPSIS</span></span>
<span data-ttu-id="4dc1c-103">Objektum létrehozása `PsApiManagementServiceFabric`</span><span class="sxs-lookup"><span data-stu-id="4dc1c-103">Creates an object of `PsApiManagementServiceFabric`</span></span>

## <span data-ttu-id="4dc1c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4dc1c-104">SYNTAX</span></span>

```
New-AzApiManagementBackendServiceFabric -ManagementEndpoint <String[]> -ClientCertificateThumbprint <String>
 [-MaxPartitionResolutionRetry <Int32>] [-ServerX509Name <Hashtable>] [-ServerCertificateThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4dc1c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4dc1c-105">DESCRIPTION</span></span>

<span data-ttu-id="4dc1c-106">A **New-AzApiManagementBackendServiceFabric** parancsmag létrehoz egy olyan objektumot, amelyet `PsApiManagementServiceFabric` az **új AzApiManagementBackend** és a **set-AzApiManagementBackend**.</span><span class="sxs-lookup"><span data-stu-id="4dc1c-106">The **New-AzApiManagementBackendServiceFabric** cmdlet creates an object of `PsApiManagementServiceFabric` to be used in cmdlet **New-AzApiManagementBackend** and **Set-AzApiManagementBackend**.</span></span>

## <span data-ttu-id="4dc1c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4dc1c-107">EXAMPLES</span></span>

### <span data-ttu-id="4dc1c-108">1. példa: a backend-szolgáltatás In-Memory objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="4dc1c-108">Example 1: Create a Backend Service Fabric In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$ManagementEndpoints = 'https://sfbackend-01.net:443', 'https://sfbackend-02.net:443'
PS C:\>$ServerCertificateThumbprints = '33CC47C6FCA848DC9B14A6F071C1EF7C'
PS C:\>$serviceFabric = New-AzApiManagementBackendServiceFabric -ManagementEndpoint  $ManagementEndpoints -ClientCertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C" -ServerX509Name @{"CN=foobar.net" = @('33CC47C6FCA848DC9B14A6F071C1EF7C'); } -ServerCertificateThumbprint $ServerCertificateThumbprints

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -ServiceFabricCluster $serviceFabric -Description "service fabric backend" -PassThru
```

<span data-ttu-id="4dc1c-109">A háttér-szolgáltatási szövet szerződés létrehozása</span><span class="sxs-lookup"><span data-stu-id="4dc1c-109">Creates a Backend Service Fabric Contract</span></span>

## <span data-ttu-id="4dc1c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4dc1c-110">PARAMETERS</span></span>

### <span data-ttu-id="4dc1c-111">-ClientCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="4dc1c-111">-ClientCertificateThumbprint</span></span>
<span data-ttu-id="4dc1c-112">Ügyféltanúsítvány-ujjlenyomat a kezelési végponthoz.</span><span class="sxs-lookup"><span data-stu-id="4dc1c-112">Client Certificate Thumbprint for the management endpoint.</span></span>
<span data-ttu-id="4dc1c-113">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="4dc1c-113">This parameter is required.</span></span>

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

### <span data-ttu-id="4dc1c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dc1c-114">-DefaultProfile</span></span>
<span data-ttu-id="4dc1c-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4dc1c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dc1c-116">-ManagementEndpoint</span><span class="sxs-lookup"><span data-stu-id="4dc1c-116">-ManagementEndpoint</span></span>
<span data-ttu-id="4dc1c-117">Szolgáltatás szövet cluster Management végpontok.</span><span class="sxs-lookup"><span data-stu-id="4dc1c-117">Service Fabric Cluster management Endpoints.</span></span>
<span data-ttu-id="4dc1c-118">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="4dc1c-118">This parameter is required.</span></span>

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

### <span data-ttu-id="4dc1c-119">-MaxPartitionResolutionRetry</span><span class="sxs-lookup"><span data-stu-id="4dc1c-119">-MaxPartitionResolutionRetry</span></span>
<span data-ttu-id="4dc1c-120">Az újbóli próbálkozások maximális száma a Service Fabric-partíciók feloldásakor.</span><span class="sxs-lookup"><span data-stu-id="4dc1c-120">Maximum number of retries when resolving a Service Fabric partition.</span></span>
<span data-ttu-id="4dc1c-121">Ez a paraméter nem kötelező, és az alapértelmezett érték 5.</span><span class="sxs-lookup"><span data-stu-id="4dc1c-121">This parameter is optional and default value is 5.</span></span>

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

### <span data-ttu-id="4dc1c-122">-ServerCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="4dc1c-122">-ServerCertificateThumbprint</span></span>
<span data-ttu-id="4dc1c-123">A tanúsítványok fürtözési szolgáltatásának ujjlenyomata TLS-kommunikációt használ. Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="4dc1c-123">Thumbprint of certificates cluster management service uses for tls communication.This parameter is optional.</span></span>

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

### <span data-ttu-id="4dc1c-124">-ServerX509Name</span><span class="sxs-lookup"><span data-stu-id="4dc1c-124">-ServerX509Name</span></span>
<span data-ttu-id="4dc1c-125">A kiszolgálói X509 a tanúsítványok neveinek gyűjteménye.</span><span class="sxs-lookup"><span data-stu-id="4dc1c-125">Server X509 Certificate Names Collection.</span></span>
<span data-ttu-id="4dc1c-126">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="4dc1c-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="4dc1c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dc1c-127">CommonParameters</span></span>
<span data-ttu-id="4dc1c-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4dc1c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dc1c-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dc1c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dc1c-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4dc1c-130">INPUTS</span></span>

### <span data-ttu-id="4dc1c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="4dc1c-131">System.String</span></span>

## <span data-ttu-id="4dc1c-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4dc1c-132">OUTPUTS</span></span>

### <span data-ttu-id="4dc1c-133">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4dc1c-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="4dc1c-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4dc1c-134">NOTES</span></span>

## <span data-ttu-id="4dc1c-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4dc1c-135">RELATED LINKS</span></span>

[<span data-ttu-id="4dc1c-136">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="4dc1c-136">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="4dc1c-137">Új – AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="4dc1c-137">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="4dc1c-138">Új – AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="4dc1c-138">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="4dc1c-139">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="4dc1c-139">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="4dc1c-140">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="4dc1c-140">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
