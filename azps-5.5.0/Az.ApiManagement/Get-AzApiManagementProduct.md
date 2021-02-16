---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
ms.openlocfilehash: 8e59cbb9885587ee57103b78400ce8ece9aafd46
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154947"
---
# <span data-ttu-id="8185e-101">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="8185e-101">Get-AzApiManagementProduct</span></span>

## <span data-ttu-id="8185e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8185e-102">SYNOPSIS</span></span>
<span data-ttu-id="8185e-103">Listát vagy adott terméket kap.</span><span class="sxs-lookup"><span data-stu-id="8185e-103">Gets a list or a particular product.</span></span>

## <span data-ttu-id="8185e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8185e-104">SYNTAX</span></span>

### <span data-ttu-id="8185e-105">Összestermék bekészítése (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8185e-105">GetAllProducts (Default)</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8185e-106">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="8185e-106">GetByProductId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8185e-107">GetByTitle</span><span class="sxs-lookup"><span data-stu-id="8185e-107">GetByTitle</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8185e-108">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="8185e-108">GetByApiId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8185e-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8185e-109">DESCRIPTION</span></span>
<span data-ttu-id="8185e-110">A **Get-AzApiManagementProduct** parancsmag kap egy listát vagy egy adott terméket.</span><span class="sxs-lookup"><span data-stu-id="8185e-110">The **Get-AzApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="8185e-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8185e-111">EXAMPLES</span></span>

### <span data-ttu-id="8185e-112">1. példa: Az összes termék lekérte</span><span class="sxs-lookup"><span data-stu-id="8185e-112">Example 1: Get all products</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext
```

<span data-ttu-id="8185e-113">Ez a parancs az összes API-kezelési terméket beveszi.</span><span class="sxs-lookup"><span data-stu-id="8185e-113">This command get all API Management products.</span></span>

### <span data-ttu-id="8185e-114">2. példa: Termék lekérte azonosító szerint</span><span class="sxs-lookup"><span data-stu-id="8185e-114">Example 2: Get a product by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="8185e-115">Ez a parancs azonosító szerint kap egy API-kezelési terméket.</span><span class="sxs-lookup"><span data-stu-id="8185e-115">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="8185e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8185e-116">PARAMETERS</span></span>

### <span data-ttu-id="8185e-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="8185e-117">-ApiId</span></span>
<span data-ttu-id="8185e-118">Az Api ApiId-ját használva megkeresi a relált termékeket.</span><span class="sxs-lookup"><span data-stu-id="8185e-118">ApiId of the Api to find the correlated products.</span></span> <span data-ttu-id="8185e-119">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="8185e-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="8185e-120">-Környezet</span><span class="sxs-lookup"><span data-stu-id="8185e-120">-Context</span></span>
<span data-ttu-id="8185e-121">Egy **PsApiManagementContext objektum** egy példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8185e-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="8185e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8185e-122">-DefaultProfile</span></span>
<span data-ttu-id="8185e-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8185e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8185e-124">-ProductId</span><span class="sxs-lookup"><span data-stu-id="8185e-124">-ProductId</span></span>
<span data-ttu-id="8185e-125">A keresett termék azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8185e-125">Specifies the identifier of the product to search for.</span></span>

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

### <span data-ttu-id="8185e-126">-Title</span><span class="sxs-lookup"><span data-stu-id="8185e-126">-Title</span></span>
<span data-ttu-id="8185e-127">A keresve keresve megadott termék címe.</span><span class="sxs-lookup"><span data-stu-id="8185e-127">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="8185e-128">Ha meg van adva, a parancsmag megpróbálja cím szerint lekérte a terméket.</span><span class="sxs-lookup"><span data-stu-id="8185e-128">If specified, the cmdlet attempts to get the product by title.</span></span>

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

### <span data-ttu-id="8185e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8185e-129">CommonParameters</span></span>
<span data-ttu-id="8185e-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8185e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8185e-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8185e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8185e-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8185e-132">INPUTS</span></span>

### <span data-ttu-id="8185e-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8185e-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8185e-134">System.String</span><span class="sxs-lookup"><span data-stu-id="8185e-134">System.String</span></span>

## <span data-ttu-id="8185e-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8185e-135">OUTPUTS</span></span>

### <span data-ttu-id="8185e-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="8185e-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="8185e-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8185e-137">NOTES</span></span>

## <span data-ttu-id="8185e-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8185e-138">RELATED LINKS</span></span>

[<span data-ttu-id="8185e-139">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="8185e-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="8185e-140">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="8185e-140">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="8185e-141">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="8185e-141">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


