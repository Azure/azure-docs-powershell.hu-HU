---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
ms.openlocfilehash: 435e167b713934962daf0cf27fc0d844caee8dcc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493295"
---
# <span data-ttu-id="857a0-101">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="857a0-101">Get-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="857a0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="857a0-102">SYNOPSIS</span></span>
<span data-ttu-id="857a0-103">Megkapja az API-t.</span><span class="sxs-lookup"><span data-stu-id="857a0-103">Gets an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="857a0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="857a0-104">SYNTAX</span></span>

### <span data-ttu-id="857a0-105">GetAllApis (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="857a0-105">GetAllApis (Default)</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="857a0-106">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="857a0-106">GetByApiId</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="857a0-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="857a0-107">GetByName</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="857a0-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="857a0-108">GetByProductId</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="857a0-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="857a0-109">DESCRIPTION</span></span>
<span data-ttu-id="857a0-110">A **Get-AzureRmApiManagementApi** parancsmag egy vagy több Azure API-kezelési API-t kap.</span><span class="sxs-lookup"><span data-stu-id="857a0-110">The **Get-AzureRmApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="857a0-111">Példák</span><span class="sxs-lookup"><span data-stu-id="857a0-111">EXAMPLES</span></span>

### <span data-ttu-id="857a0-112">Példa 1: az összes felügyeleti API beszerzése</span><span class="sxs-lookup"><span data-stu-id="857a0-112">Example 1: Get all management APIs</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="857a0-113">Ez a parancs a megadott környezet összes API-t megkapja.</span><span class="sxs-lookup"><span data-stu-id="857a0-113">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="857a0-114">2. példa: felügyeleti API beszerzése AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="857a0-114">Example 2: Get a management API by ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="857a0-115">Ez a parancs a megadott AZONOSÍTÓJÚ API-t kapja.</span><span class="sxs-lookup"><span data-stu-id="857a0-115">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="857a0-116">3. példa: felügyeleti API beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="857a0-116">Example 3: Get a management API by name</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="857a0-117">Ez a parancs a megadott nevű API-t kapja.</span><span class="sxs-lookup"><span data-stu-id="857a0-117">This command gets the API with the specified name.</span></span>

## <span data-ttu-id="857a0-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="857a0-118">PARAMETERS</span></span>

### <span data-ttu-id="857a0-119">-ApiId</span><span class="sxs-lookup"><span data-stu-id="857a0-119">-ApiId</span></span>
<span data-ttu-id="857a0-120">A beolvasott API AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="857a0-120">Specifies the ID of the API to get.</span></span>

```yaml
Type: String
Parameter Sets: GetByApiId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="857a0-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="857a0-121">-Context</span></span>
<span data-ttu-id="857a0-122">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="857a0-122">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="857a0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="857a0-123">-DefaultProfile</span></span>
<span data-ttu-id="857a0-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="857a0-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="857a0-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="857a0-125">-Name</span></span>
<span data-ttu-id="857a0-126">A beolvasott API nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="857a0-126">Specifies the name of the API to get.</span></span>

```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="857a0-127">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="857a0-127">-ProductId</span></span>
<span data-ttu-id="857a0-128">Annak a termékeknek az AZONOSÍTÓját adja meg, amelynek az API-t be kell szereznie.</span><span class="sxs-lookup"><span data-stu-id="857a0-128">Specifies the ID of the product for which to get the API.</span></span>

```yaml
Type: String
Parameter Sets: GetByProductId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="857a0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="857a0-129">CommonParameters</span></span>
<span data-ttu-id="857a0-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="857a0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="857a0-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="857a0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="857a0-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="857a0-132">INPUTS</span></span>

### <span data-ttu-id="857a0-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="857a0-133">None</span></span>
<span data-ttu-id="857a0-134">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="857a0-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="857a0-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="857a0-135">OUTPUTS</span></span>

### <span data-ttu-id="857a0-136">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="857a0-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="857a0-137">Egy adott ApiManagement-szolgáltatás API-adatának részletei</span><span class="sxs-lookup"><span data-stu-id="857a0-137">The details of the Api in a given ApiManagement service</span></span>

### <span data-ttu-id="857a0-138">IList<Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApi></span><span class="sxs-lookup"><span data-stu-id="857a0-138">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi></span></span>
<span data-ttu-id="857a0-139">Az API-k listája az adott ApiManagement szolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="857a0-139">The list of Apis in a given ApiManagement service</span></span>

## <span data-ttu-id="857a0-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="857a0-140">NOTES</span></span>

## <span data-ttu-id="857a0-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="857a0-141">RELATED LINKS</span></span>

[<span data-ttu-id="857a0-142">Exportálás – AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="857a0-142">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="857a0-143">Importálás – AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="857a0-143">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="857a0-144">Új – AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="857a0-144">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="857a0-145">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="857a0-145">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="857a0-146">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="857a0-146">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


