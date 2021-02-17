---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCache.md
ms.openlocfilehash: fee978a1500c0fc472ec8015a3e8dbbbdc8015bd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205806"
---
# <span data-ttu-id="9366a-101">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="9366a-101">Get-AzApiManagementCache</span></span>

## <span data-ttu-id="9366a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9366a-102">SYNOPSIS</span></span>
<span data-ttu-id="9366a-103">A gyorsítótár részleteinek megtekintése.</span><span class="sxs-lookup"><span data-stu-id="9366a-103">Get the details of the Cache.</span></span>

## <span data-ttu-id="9366a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9366a-104">SYNTAX</span></span>

### <span data-ttu-id="9366a-105">ContextParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9366a-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9366a-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9366a-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementCache -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9366a-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9366a-107">DESCRIPTION</span></span>
<span data-ttu-id="9366a-108">Az Api Management szolgáltatásban konfigurált gyorsítótár részleteinek megtekintése.</span><span class="sxs-lookup"><span data-stu-id="9366a-108">Get the details of the Cache configured in Api Management service.</span></span>

## <span data-ttu-id="9366a-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9366a-109">EXAMPLES</span></span>

### <span data-ttu-id="9366a-110">1. példa: Az összes gyorsítótár lekérte</span><span class="sxs-lookup"><span data-stu-id="9366a-110">Example 1: Get all Caches</span></span>
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

<span data-ttu-id="9366a-111">Az Api Management szolgáltatásban konfigurált összes gyorsítótár listáját lekérte.</span><span class="sxs-lookup"><span data-stu-id="9366a-111">Gets a list of all the Caches configured in the Api Management service.</span></span>

### <span data-ttu-id="9366a-112">2. példa: A westus azonosító által megadott gyorsítótár lekérte</span><span class="sxs-lookup"><span data-stu-id="9366a-112">Example 2: Get the Cache specified by the Identifier westus</span></span>
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

<span data-ttu-id="9366a-113">A westushoz konfigurált gyorsítótár részleteinek megtekintése</span><span class="sxs-lookup"><span data-stu-id="9366a-113">Get the details of the specified Cache configured for westus</span></span>

## <span data-ttu-id="9366a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9366a-114">PARAMETERS</span></span>

### <span data-ttu-id="9366a-115">-CacheId</span><span class="sxs-lookup"><span data-stu-id="9366a-115">-CacheId</span></span>
<span data-ttu-id="9366a-116">Gyorsítótár azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9366a-116">Identifier of a cache.</span></span>
<span data-ttu-id="9366a-117">Ha meg van adva, a rendszer megpróbálja megtalálni a gyorsítótárat az azonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="9366a-117">If specified will try to find cache by the identifier.</span></span>
<span data-ttu-id="9366a-118">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="9366a-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="9366a-119">-Környezet</span><span class="sxs-lookup"><span data-stu-id="9366a-119">-Context</span></span>
<span data-ttu-id="9366a-120">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="9366a-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9366a-121">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="9366a-121">This parameter is required.</span></span>

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

### <span data-ttu-id="9366a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9366a-122">-DefaultProfile</span></span>
<span data-ttu-id="9366a-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9366a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9366a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9366a-124">-ResourceId</span></span>
<span data-ttu-id="9366a-125">Gyorsítótár erőforrás-azonosítójának felkarazása</span><span class="sxs-lookup"><span data-stu-id="9366a-125">Arm Resource Identifier of a cache.</span></span> <span data-ttu-id="9366a-126">Ha meg van adva, a rendszer megpróbálja megtalálni a gyorsítótárat az azonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="9366a-126">If specified will try to find cache by the identifier.</span></span> <span data-ttu-id="9366a-127">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="9366a-127">This parameter is required.</span></span>

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

### <span data-ttu-id="9366a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9366a-128">CommonParameters</span></span>
<span data-ttu-id="9366a-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9366a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9366a-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9366a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9366a-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9366a-131">INPUTS</span></span>

### <span data-ttu-id="9366a-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9366a-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9366a-133">System.String</span><span class="sxs-lookup"><span data-stu-id="9366a-133">System.String</span></span>

## <span data-ttu-id="9366a-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9366a-134">OUTPUTS</span></span>

### <span data-ttu-id="9366a-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="9366a-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="9366a-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9366a-136">NOTES</span></span>

## <span data-ttu-id="9366a-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9366a-137">RELATED LINKS</span></span>

[<span data-ttu-id="9366a-138">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="9366a-138">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="9366a-139">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="9366a-139">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)

[<span data-ttu-id="9366a-140">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="9366a-140">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
