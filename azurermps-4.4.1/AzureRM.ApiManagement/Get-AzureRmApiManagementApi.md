---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
ms.openlocfilehash: 95784b084f6d106413c65b840dd73f313a47799e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679997"
---
# <span data-ttu-id="10b02-101">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="10b02-101">Get-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="10b02-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="10b02-102">SYNOPSIS</span></span>
<span data-ttu-id="10b02-103">Megkapja az API-t.</span><span class="sxs-lookup"><span data-stu-id="10b02-103">Gets an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10b02-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="10b02-104">SYNTAX</span></span>

### <span data-ttu-id="10b02-105">Minden API (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="10b02-105">All APIs (Default)</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="10b02-106">Keresés azonosító szerint</span><span class="sxs-lookup"><span data-stu-id="10b02-106">Find by ID</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10b02-107">Keresés név szerint</span><span class="sxs-lookup"><span data-stu-id="10b02-107">Find by Name</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10b02-108">Keresés termékazonosító szerint</span><span class="sxs-lookup"><span data-stu-id="10b02-108">Find by product ID</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10b02-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="10b02-109">DESCRIPTION</span></span>
<span data-ttu-id="10b02-110">A **Get-AzureRmApiManagementApi** parancsmag egy vagy több Azure API-kezelési API-t kap.</span><span class="sxs-lookup"><span data-stu-id="10b02-110">The **Get-AzureRmApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="10b02-111">Példák</span><span class="sxs-lookup"><span data-stu-id="10b02-111">EXAMPLES</span></span>

### <span data-ttu-id="10b02-112">Példa 1: az összes felügyeleti API beszerzése</span><span class="sxs-lookup"><span data-stu-id="10b02-112">Example 1: Get all management APIs</span></span>
```
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="10b02-113">Ez a parancs a megadott környezet összes API-t megkapja.</span><span class="sxs-lookup"><span data-stu-id="10b02-113">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="10b02-114">2. példa: felügyeleti API beszerzése AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="10b02-114">Example 2: Get a management API by ID</span></span>
```
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="10b02-115">Ez a parancs a megadott AZONOSÍTÓJÚ API-t kapja.</span><span class="sxs-lookup"><span data-stu-id="10b02-115">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="10b02-116">3. példa: felügyeleti API beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="10b02-116">Example 3: Get a management API by name</span></span>
```
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="10b02-117">Ez a parancs a megadott nevű API-t kapja.</span><span class="sxs-lookup"><span data-stu-id="10b02-117">This command gets the API with the specified name.</span></span>

## <span data-ttu-id="10b02-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="10b02-118">PARAMETERS</span></span>

### <span data-ttu-id="10b02-119">-ApiId</span><span class="sxs-lookup"><span data-stu-id="10b02-119">-ApiId</span></span>
<span data-ttu-id="10b02-120">A beolvasott API AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="10b02-120">Specifies the ID of the API to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10b02-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="10b02-121">-Context</span></span>
<span data-ttu-id="10b02-122">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="10b02-122">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10b02-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="10b02-123">-Name</span></span>
<span data-ttu-id="10b02-124">A beolvasott API nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="10b02-124">Specifies the name of the API to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by Name
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10b02-125">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="10b02-125">-ProductId</span></span>
<span data-ttu-id="10b02-126">Annak a termékeknek az AZONOSÍTÓját adja meg, amelynek az API-t be kell szereznie.</span><span class="sxs-lookup"><span data-stu-id="10b02-126">Specifies the ID of the product for which to get the API.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by product ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10b02-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10b02-127">-DefaultProfile</span></span>
<span data-ttu-id="10b02-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="10b02-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10b02-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10b02-129">CommonParameters</span></span>
<span data-ttu-id="10b02-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="10b02-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10b02-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10b02-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10b02-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="10b02-132">INPUTS</span></span>

## <span data-ttu-id="10b02-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="10b02-133">OUTPUTS</span></span>

### <span data-ttu-id="10b02-134">IList<Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApi></span><span class="sxs-lookup"><span data-stu-id="10b02-134">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi></span></span>

## <span data-ttu-id="10b02-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="10b02-135">NOTES</span></span>

## <span data-ttu-id="10b02-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="10b02-136">RELATED LINKS</span></span>

[<span data-ttu-id="10b02-137">Exportálás – AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="10b02-137">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="10b02-138">Importálás – AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="10b02-138">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="10b02-139">Új – AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="10b02-139">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="10b02-140">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="10b02-140">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="10b02-141">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="10b02-141">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


