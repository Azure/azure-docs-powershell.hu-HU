---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
ms.openlocfilehash: 589338afde60e069646cb677205da11e322ba7da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012869"
---
# <span data-ttu-id="e0f66-101">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="e0f66-101">Get-AzApiManagementProduct</span></span>

## <span data-ttu-id="e0f66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0f66-102">SYNOPSIS</span></span>
<span data-ttu-id="e0f66-103">Listát vagy adott terméket kap.</span><span class="sxs-lookup"><span data-stu-id="e0f66-103">Gets a list or a particular product.</span></span>

## <span data-ttu-id="e0f66-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e0f66-104">SYNTAX</span></span>

### <span data-ttu-id="e0f66-105">GetAllProducts (Default)</span><span class="sxs-lookup"><span data-stu-id="e0f66-105">GetAllProducts (Default)</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e0f66-106">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="e0f66-106">GetByProductId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0f66-107">GetByTitle</span><span class="sxs-lookup"><span data-stu-id="e0f66-107">GetByTitle</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0f66-108">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="e0f66-108">GetByApiId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0f66-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e0f66-109">DESCRIPTION</span></span>
<span data-ttu-id="e0f66-110">A **Get-AzApiManagementProduct** parancsmag kap egy listát vagy egy adott terméket.</span><span class="sxs-lookup"><span data-stu-id="e0f66-110">The **Get-AzApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="e0f66-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e0f66-111">EXAMPLES</span></span>

### <span data-ttu-id="e0f66-112">1. példa: Az összes termék lekérte</span><span class="sxs-lookup"><span data-stu-id="e0f66-112">Example 1: Get all products</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext
```

<span data-ttu-id="e0f66-113">Ez a parancs az összes API-kezelési terméket beveszi.</span><span class="sxs-lookup"><span data-stu-id="e0f66-113">This command get all API Management products.</span></span>

### <span data-ttu-id="e0f66-114">2. példa: Termék lekérte azonosító szerint</span><span class="sxs-lookup"><span data-stu-id="e0f66-114">Example 2: Get a product by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="e0f66-115">Ez a parancs azonosító szerint kap egy API-kezelési terméket.</span><span class="sxs-lookup"><span data-stu-id="e0f66-115">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="e0f66-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0f66-116">PARAMETERS</span></span>

### <span data-ttu-id="e0f66-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="e0f66-117">-ApiId</span></span>
<span data-ttu-id="e0f66-118">Az Api ApiId-ját használva megkeresi a relált termékeket.</span><span class="sxs-lookup"><span data-stu-id="e0f66-118">ApiId of the Api to find the correlated products.</span></span> <span data-ttu-id="e0f66-119">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="e0f66-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="e0f66-120">-Környezet</span><span class="sxs-lookup"><span data-stu-id="e0f66-120">-Context</span></span>
<span data-ttu-id="e0f66-121">Egy **PsApiManagementContext objektum** egy példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0f66-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e0f66-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0f66-122">-DefaultProfile</span></span>
<span data-ttu-id="e0f66-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e0f66-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0f66-124">-ProductId</span><span class="sxs-lookup"><span data-stu-id="e0f66-124">-ProductId</span></span>
<span data-ttu-id="e0f66-125">A keresett termék azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e0f66-125">Specifies the identifier of the product to search for.</span></span>

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

### <span data-ttu-id="e0f66-126">-Title</span><span class="sxs-lookup"><span data-stu-id="e0f66-126">-Title</span></span>
<span data-ttu-id="e0f66-127">A keresve keresve megadott termék címe.</span><span class="sxs-lookup"><span data-stu-id="e0f66-127">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="e0f66-128">Ha meg van adva, a parancsmag megpróbálja cím szerint lekérte a terméket.</span><span class="sxs-lookup"><span data-stu-id="e0f66-128">If specified, the cmdlet attempts to get the product by title.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByTitle
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0f66-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0f66-129">CommonParameters</span></span>
<span data-ttu-id="e0f66-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0f66-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0f66-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0f66-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0f66-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e0f66-132">INPUTS</span></span>

### <span data-ttu-id="e0f66-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e0f66-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e0f66-134">System.String</span><span class="sxs-lookup"><span data-stu-id="e0f66-134">System.String</span></span>

## <span data-ttu-id="e0f66-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0f66-135">OUTPUTS</span></span>

### <span data-ttu-id="e0f66-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="e0f66-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="e0f66-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e0f66-137">NOTES</span></span>

## <span data-ttu-id="e0f66-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0f66-138">RELATED LINKS</span></span>

[<span data-ttu-id="e0f66-139">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="e0f66-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="e0f66-140">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="e0f66-140">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="e0f66-141">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="e0f66-141">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


