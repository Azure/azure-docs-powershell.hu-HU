---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
ms.openlocfilehash: 3fccd2becf08ee78ca928bd17043d83b0a277af9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668130"
---
# <span data-ttu-id="cca30-101">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cca30-101">Get-AzApiManagementApi</span></span>

## <span data-ttu-id="cca30-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cca30-102">SYNOPSIS</span></span>
<span data-ttu-id="cca30-103">Megkapja az API-t.</span><span class="sxs-lookup"><span data-stu-id="cca30-103">Gets an API.</span></span>

## <span data-ttu-id="cca30-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cca30-104">SYNTAX</span></span>

### <span data-ttu-id="cca30-105">GetAllApis (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cca30-105">GetAllApis (Default)</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cca30-106">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="cca30-106">GetByApiId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cca30-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="cca30-107">GetByName</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cca30-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="cca30-108">GetByProductId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cca30-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="cca30-109">DESCRIPTION</span></span>
<span data-ttu-id="cca30-110">A **Get-AzApiManagementApi** parancsmag egy vagy több Azure API-kezelési API-t kap.</span><span class="sxs-lookup"><span data-stu-id="cca30-110">The **Get-AzApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="cca30-111">Példák</span><span class="sxs-lookup"><span data-stu-id="cca30-111">EXAMPLES</span></span>

### <span data-ttu-id="cca30-112">Példa 1: az összes felügyeleti API beszerzése</span><span class="sxs-lookup"><span data-stu-id="cca30-112">Example 1: Get all management APIs</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="cca30-113">Ez a parancs a megadott környezet összes API-t megkapja.</span><span class="sxs-lookup"><span data-stu-id="cca30-113">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="cca30-114">2. példa: felügyeleti API beszerzése AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="cca30-114">Example 2: Get a management API by ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="cca30-115">Ez a parancs a megadott AZONOSÍTÓJÚ API-t kapja.</span><span class="sxs-lookup"><span data-stu-id="cca30-115">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="cca30-116">3. példa: felügyeleti API beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="cca30-116">Example 3: Get a management API by name</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="cca30-117">Ez a parancs a megadott nevű API-t kapja.</span><span class="sxs-lookup"><span data-stu-id="cca30-117">This command gets the API with the specified name.</span></span>

## <span data-ttu-id="cca30-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cca30-118">PARAMETERS</span></span>

### <span data-ttu-id="cca30-119">-ApiId</span><span class="sxs-lookup"><span data-stu-id="cca30-119">-ApiId</span></span>
<span data-ttu-id="cca30-120">A beolvasott API AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cca30-120">Specifies the ID of the API to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cca30-121">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="cca30-121">-ApiRevision</span></span>
<span data-ttu-id="cca30-122">Az adott API-verzió verziószámának verziószáma.</span><span class="sxs-lookup"><span data-stu-id="cca30-122">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="cca30-123">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="cca30-123">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByApiId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cca30-124">-Környezet</span><span class="sxs-lookup"><span data-stu-id="cca30-124">-Context</span></span>
<span data-ttu-id="cca30-125">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="cca30-125">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="cca30-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cca30-126">-DefaultProfile</span></span>
<span data-ttu-id="cca30-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cca30-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cca30-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cca30-128">-Name</span></span>
<span data-ttu-id="cca30-129">A beolvasott API nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cca30-129">Specifies the name of the API to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cca30-130">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="cca30-130">-ProductId</span></span>
<span data-ttu-id="cca30-131">Annak a termékeknek az AZONOSÍTÓját adja meg, amelynek az API-t be kell szereznie.</span><span class="sxs-lookup"><span data-stu-id="cca30-131">Specifies the ID of the product for which to get the API.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cca30-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cca30-132">CommonParameters</span></span>
<span data-ttu-id="cca30-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cca30-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cca30-134">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cca30-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cca30-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cca30-135">INPUTS</span></span>

### <span data-ttu-id="cca30-136">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="cca30-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="cca30-137">System. String</span><span class="sxs-lookup"><span data-stu-id="cca30-137">System.String</span></span>

## <span data-ttu-id="cca30-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cca30-138">OUTPUTS</span></span>

### <span data-ttu-id="cca30-139">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cca30-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="cca30-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cca30-140">NOTES</span></span>

## <span data-ttu-id="cca30-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cca30-141">RELATED LINKS</span></span>

[<span data-ttu-id="cca30-142">Exportálás – AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cca30-142">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="cca30-143">Importálás – AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cca30-143">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="cca30-144">Új – AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cca30-144">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="cca30-145">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cca30-145">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="cca30-146">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cca30-146">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


