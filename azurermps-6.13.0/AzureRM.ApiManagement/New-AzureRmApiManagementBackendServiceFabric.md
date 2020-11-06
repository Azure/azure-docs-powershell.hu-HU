---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackendservicefabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendServiceFabric.md
ms.openlocfilehash: 925e4949b444c9338fad3f88cf5066430e1b5a75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494218"
---
# <span data-ttu-id="9e5bc-101">New-AzureRmApiManagementBackendServiceFabric</span><span class="sxs-lookup"><span data-stu-id="9e5bc-101">New-AzureRmApiManagementBackendServiceFabric</span></span>

## <span data-ttu-id="9e5bc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9e5bc-102">SYNOPSIS</span></span>
<span data-ttu-id="9e5bc-103">Objektum létrehozása `PsApiManagementServiceFabric`</span><span class="sxs-lookup"><span data-stu-id="9e5bc-103">Creates an object of `PsApiManagementServiceFabric`</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e5bc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9e5bc-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendServiceFabric -ManagementEndpoint <String[]>
 -ClientCertificateThumbprint <String> [-MaxPartitionResolutionRetry <Int32>] [-ServerX509Name <Hashtable>]
 [-ServerCertificateThumbprint <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e5bc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9e5bc-105">DESCRIPTION</span></span>

<span data-ttu-id="9e5bc-106">A **New-AzureRmApiManagementBackendServiceFabric** parancsmag létrehoz egy olyan objektumot, amelyet `PsApiManagementServiceFabric` az **új AzureRmApiManagementBackend** és a **set-AzureRmApiManagementBackend**.</span><span class="sxs-lookup"><span data-stu-id="9e5bc-106">The **New-AzureRmApiManagementBackendServiceFabric** cmdlet creates an object of `PsApiManagementServiceFabric` to be used in cmdlet **New-AzureRmApiManagementBackend** and **Set-AzureRmApiManagementBackend**.</span></span>

## <span data-ttu-id="9e5bc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9e5bc-107">EXAMPLES</span></span>

### <span data-ttu-id="9e5bc-108">1. példa: a backend-szolgáltatás In-Memory objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="9e5bc-108">Example 1: Create a Backend Service Fabric In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$ManagementEndpoints = 'https://sfbackend-01.net:443', 'https://sfbackend-02.net:443'
PS C:\>$ServerCertificateThumbprints = '33CC47C6FCA848DC9B14A6F071C1EF7C'
PS C:\>$serviceFabric = New-AzureRmApiManagementBackendServiceFabric -ManagementEndpoint  $ManagementEndpoints -ClientCertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C" -ServerX509Name @{"CN=foobar.net" = @('33CC47C6FCA848DC9B14A6F071C1EF7C'); } -ServerCertificateThumbprint $ServerCertificateThumbprints

PS C:\>$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -ServiceFabricCluster $serviceFabric -Description "service fabric backend" -PassThru
```

<span data-ttu-id="9e5bc-109">A háttér-szolgáltatási szövet szerződés létrehozása</span><span class="sxs-lookup"><span data-stu-id="9e5bc-109">Creates a Backend Service Fabric Contract</span></span>

## <span data-ttu-id="9e5bc-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9e5bc-110">PARAMETERS</span></span>

### <span data-ttu-id="9e5bc-111">-ClientCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="9e5bc-111">-ClientCertificateThumbprint</span></span>
<span data-ttu-id="9e5bc-112">Ügyféltanúsítvány-ujjlenyomat a kezelési végponthoz.</span><span class="sxs-lookup"><span data-stu-id="9e5bc-112">Client Certificate Thumbprint for the management endpoint.</span></span>
<span data-ttu-id="9e5bc-113">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="9e5bc-113">This parameter is required.</span></span>

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

### <span data-ttu-id="9e5bc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e5bc-114">-DefaultProfile</span></span>
<span data-ttu-id="9e5bc-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9e5bc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e5bc-116">-ManagementEndpoint</span><span class="sxs-lookup"><span data-stu-id="9e5bc-116">-ManagementEndpoint</span></span>
<span data-ttu-id="9e5bc-117">Szolgáltatás szövet cluster Management végpontok.</span><span class="sxs-lookup"><span data-stu-id="9e5bc-117">Service Fabric Cluster management Endpoints.</span></span>
<span data-ttu-id="9e5bc-118">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="9e5bc-118">This parameter is required.</span></span>

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

### <span data-ttu-id="9e5bc-119">-MaxPartitionResolutionRetry</span><span class="sxs-lookup"><span data-stu-id="9e5bc-119">-MaxPartitionResolutionRetry</span></span>
<span data-ttu-id="9e5bc-120">Az újbóli próbálkozások maximális száma a Service Fabric-partíciók feloldásakor.</span><span class="sxs-lookup"><span data-stu-id="9e5bc-120">Maximum number of retries when resolving a Service Fabric partition.</span></span>
<span data-ttu-id="9e5bc-121">Ez a paraméter nem kötelező, és az alapértelmezett érték 5.</span><span class="sxs-lookup"><span data-stu-id="9e5bc-121">This parameter is optional and default value is 5.</span></span>

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

### <span data-ttu-id="9e5bc-122">-ServerCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="9e5bc-122">-ServerCertificateThumbprint</span></span>
<span data-ttu-id="9e5bc-123">A tanúsítványok fürtözési szolgáltatásának ujjlenyomata TLS-kommunikációt használ. Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="9e5bc-123">Thumbprint of certificates cluster management service uses for tls communication.This parameter is optional.</span></span>

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

### <span data-ttu-id="9e5bc-124">-ServerX509Name</span><span class="sxs-lookup"><span data-stu-id="9e5bc-124">-ServerX509Name</span></span>
<span data-ttu-id="9e5bc-125">A kiszolgálói X509 a tanúsítványok neveinek gyűjteménye.</span><span class="sxs-lookup"><span data-stu-id="9e5bc-125">Server X509 Certificate Names Collection.</span></span>
<span data-ttu-id="9e5bc-126">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="9e5bc-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="9e5bc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e5bc-127">CommonParameters</span></span>
<span data-ttu-id="9e5bc-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9e5bc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e5bc-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e5bc-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e5bc-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e5bc-130">INPUTS</span></span>

### <span data-ttu-id="9e5bc-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9e5bc-131">System.String</span></span>

## <span data-ttu-id="9e5bc-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e5bc-132">OUTPUTS</span></span>

### <span data-ttu-id="9e5bc-133">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="9e5bc-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="9e5bc-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9e5bc-134">NOTES</span></span>

## <span data-ttu-id="9e5bc-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9e5bc-135">RELATED LINKS</span></span>

[<span data-ttu-id="9e5bc-136">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="9e5bc-136">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="9e5bc-137">Új – AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="9e5bc-137">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="9e5bc-138">Új – AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="9e5bc-138">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="9e5bc-139">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="9e5bc-139">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="9e5bc-140">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="9e5bc-140">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
