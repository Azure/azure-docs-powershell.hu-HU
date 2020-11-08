---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCache.md
ms.openlocfilehash: fee978a1500c0fc472ec8015a3e8dbbbdc8015bd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194841"
---
# <span data-ttu-id="4fa24-101">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="4fa24-101">Get-AzApiManagementCache</span></span>

## <span data-ttu-id="4fa24-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4fa24-102">SYNOPSIS</span></span>
<span data-ttu-id="4fa24-103">A gyorsítótár részleteinek beszerzése.</span><span class="sxs-lookup"><span data-stu-id="4fa24-103">Get the details of the Cache.</span></span>

## <span data-ttu-id="4fa24-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4fa24-104">SYNTAX</span></span>

### <span data-ttu-id="4fa24-105">ContextParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4fa24-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fa24-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fa24-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementCache -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fa24-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4fa24-107">DESCRIPTION</span></span>
<span data-ttu-id="4fa24-108">Ismerje meg az API-kezelési szolgáltatásban konfigurált gyorsítótár adatait.</span><span class="sxs-lookup"><span data-stu-id="4fa24-108">Get the details of the Cache configured in Api Management service.</span></span>

## <span data-ttu-id="4fa24-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4fa24-109">EXAMPLES</span></span>

### <span data-ttu-id="4fa24-110">Példa 1: az összes gyorsítótár beolvasása</span><span class="sxs-lookup"><span data-stu-id="4fa24-110">Example 1: Get all Caches</span></span>
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

<span data-ttu-id="4fa24-111">Az API-kezelési szolgáltatásban konfigurált összes gyorsítótár listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="4fa24-111">Gets a list of all the Caches configured in the Api Management service.</span></span>

### <span data-ttu-id="4fa24-112">2. példa: az azonosító westus megadott gyorsítótár beolvasása</span><span class="sxs-lookup"><span data-stu-id="4fa24-112">Example 2: Get the Cache specified by the Identifier westus</span></span>
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

<span data-ttu-id="4fa24-113">A westus-ra konfigurált megadott gyorsítótár részleteinek beszerzése</span><span class="sxs-lookup"><span data-stu-id="4fa24-113">Get the details of the specified Cache configured for westus</span></span>

## <span data-ttu-id="4fa24-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4fa24-114">PARAMETERS</span></span>

### <span data-ttu-id="4fa24-115">-CacheId</span><span class="sxs-lookup"><span data-stu-id="4fa24-115">-CacheId</span></span>
<span data-ttu-id="4fa24-116">A gyorsítótár azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4fa24-116">Identifier of a cache.</span></span>
<span data-ttu-id="4fa24-117">Ha meg van adva a gyorsítótár megkeresése az azonosítóval, a program megpróbálja megkeresni.</span><span class="sxs-lookup"><span data-stu-id="4fa24-117">If specified will try to find cache by the identifier.</span></span>
<span data-ttu-id="4fa24-118">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="4fa24-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="4fa24-119">-Környezet</span><span class="sxs-lookup"><span data-stu-id="4fa24-119">-Context</span></span>
<span data-ttu-id="4fa24-120">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="4fa24-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="4fa24-121">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="4fa24-121">This parameter is required.</span></span>

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

### <span data-ttu-id="4fa24-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fa24-122">-DefaultProfile</span></span>
<span data-ttu-id="4fa24-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4fa24-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fa24-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4fa24-124">-ResourceId</span></span>
<span data-ttu-id="4fa24-125">A gyorsítótár ARM erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4fa24-125">Arm Resource Identifier of a cache.</span></span> <span data-ttu-id="4fa24-126">Ha meg van adva a gyorsítótár megkeresése az azonosítóval, a program megpróbálja megkeresni.</span><span class="sxs-lookup"><span data-stu-id="4fa24-126">If specified will try to find cache by the identifier.</span></span> <span data-ttu-id="4fa24-127">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="4fa24-127">This parameter is required.</span></span>

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

### <span data-ttu-id="4fa24-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fa24-128">CommonParameters</span></span>
<span data-ttu-id="4fa24-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4fa24-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fa24-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4fa24-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fa24-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fa24-131">INPUTS</span></span>

### <span data-ttu-id="4fa24-132">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4fa24-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4fa24-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4fa24-133">System.String</span></span>

## <span data-ttu-id="4fa24-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fa24-134">OUTPUTS</span></span>

### <span data-ttu-id="4fa24-135">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="4fa24-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="4fa24-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4fa24-136">NOTES</span></span>

## <span data-ttu-id="4fa24-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4fa24-137">RELATED LINKS</span></span>

[<span data-ttu-id="4fa24-138">Új – AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="4fa24-138">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="4fa24-139">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="4fa24-139">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)

[<span data-ttu-id="4fa24-140">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="4fa24-140">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
