---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCache.md
ms.openlocfilehash: fee978a1500c0fc472ec8015a3e8dbbbdc8015bd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478994"
---
# <span data-ttu-id="59c64-101">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="59c64-101">Get-AzApiManagementCache</span></span>

## <span data-ttu-id="59c64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59c64-102">SYNOPSIS</span></span>
<span data-ttu-id="59c64-103">A gyorsítótár részleteinek megtekintése.</span><span class="sxs-lookup"><span data-stu-id="59c64-103">Get the details of the Cache.</span></span>

## <span data-ttu-id="59c64-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="59c64-104">SYNTAX</span></span>

### <span data-ttu-id="59c64-105">ContextParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="59c64-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59c64-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="59c64-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementCache -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59c64-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="59c64-107">DESCRIPTION</span></span>
<span data-ttu-id="59c64-108">Az Api Management szolgáltatásban konfigurált gyorsítótár részleteinek megtekintése.</span><span class="sxs-lookup"><span data-stu-id="59c64-108">Get the details of the Cache configured in Api Management service.</span></span>

## <span data-ttu-id="59c64-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="59c64-109">EXAMPLES</span></span>

### <span data-ttu-id="59c64-110">1. példa: Az összes gyorsítótár lekérte</span><span class="sxs-lookup"><span data-stu-id="59c64-110">Example 1: Get all Caches</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCache -Context $apimContext
```

```
CacheId           : westus
Description       : apim.redis.cache.windows.net
ConnectionString  : {{5cc1848125a3f724dcf9a928}}
ResourceId        : https://management.azure.com/subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.Cache/Redis/apim
Id                : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/caches/westus
ResourceGroupName : Api-Default-West-US
ServiceName       : contoso
```

<span data-ttu-id="59c64-111">Az Api Management szolgáltatásban konfigurált összes gyorsítótár listáját lekérte.</span><span class="sxs-lookup"><span data-stu-id="59c64-111">Gets a list of all the Caches configured in the Api Management service.</span></span>

### <span data-ttu-id="59c64-112">2. példa: A westus azonosító által megadott gyorsítótár lekérte</span><span class="sxs-lookup"><span data-stu-id="59c64-112">Example 2: Get the Cache specified by the Identifier westus</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCache -Context $apimContext -cacheId westus
```

```
CacheId           : westus
Description       : apim.redis.cache.windows.net
ConnectionString  : {{5cc1848125a3f724dcf9a928}}
ResourceId        : https://management.azure.com/subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.Cache/Redis/apim
Id                : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/caches/westus
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="59c64-113">A westushoz konfigurált gyorsítótár részleteinek megtekintése</span><span class="sxs-lookup"><span data-stu-id="59c64-113">Get the details of the specified Cache configured for westus</span></span>

## <span data-ttu-id="59c64-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59c64-114">PARAMETERS</span></span>

### <span data-ttu-id="59c64-115">-CacheId</span><span class="sxs-lookup"><span data-stu-id="59c64-115">-CacheId</span></span>
<span data-ttu-id="59c64-116">Gyorsítótár azonosítója.</span><span class="sxs-lookup"><span data-stu-id="59c64-116">Identifier of a cache.</span></span>
<span data-ttu-id="59c64-117">Ha meg van adva, a rendszer megpróbálja megtalálni a gyorsítótárat az azonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="59c64-117">If specified will try to find cache by the identifier.</span></span>
<span data-ttu-id="59c64-118">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="59c64-118">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59c64-119">-Környezet</span><span class="sxs-lookup"><span data-stu-id="59c64-119">-Context</span></span>
<span data-ttu-id="59c64-120">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="59c64-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="59c64-121">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="59c64-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59c64-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59c64-122">-DefaultProfile</span></span>
<span data-ttu-id="59c64-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="59c64-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59c64-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59c64-124">-ResourceId</span></span>
<span data-ttu-id="59c64-125">Gyorsítótár erőforrás-azonosítójának felkarazása</span><span class="sxs-lookup"><span data-stu-id="59c64-125">Arm Resource Identifier of a cache.</span></span> <span data-ttu-id="59c64-126">Ha meg van adva, a rendszer megpróbálja megtalálni a gyorsítótárat az azonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="59c64-126">If specified will try to find cache by the identifier.</span></span> <span data-ttu-id="59c64-127">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="59c64-127">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59c64-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59c64-128">CommonParameters</span></span>
<span data-ttu-id="59c64-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59c64-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59c64-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="59c64-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59c64-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="59c64-131">INPUTS</span></span>

### <span data-ttu-id="59c64-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="59c64-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="59c64-133">System.String</span><span class="sxs-lookup"><span data-stu-id="59c64-133">System.String</span></span>

## <span data-ttu-id="59c64-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59c64-134">OUTPUTS</span></span>

### <span data-ttu-id="59c64-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="59c64-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="59c64-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="59c64-136">NOTES</span></span>

## <span data-ttu-id="59c64-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59c64-137">RELATED LINKS</span></span>

[<span data-ttu-id="59c64-138">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="59c64-138">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="59c64-139">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="59c64-139">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)

[<span data-ttu-id="59c64-140">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="59c64-140">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
