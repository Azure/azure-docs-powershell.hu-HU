---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
ms.openlocfilehash: 9ad3c6b149e58bcd81ec8ce9c15ddc27fff85878
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668099"
---
# <span data-ttu-id="ab142-101">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="ab142-101">Get-AzApiManagementProduct</span></span>

## <span data-ttu-id="ab142-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ab142-102">SYNOPSIS</span></span>
<span data-ttu-id="ab142-103">Egy lista vagy egy adott terméket kap.</span><span class="sxs-lookup"><span data-stu-id="ab142-103">Gets a list or a particular product.</span></span>

## <span data-ttu-id="ab142-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ab142-104">SYNTAX</span></span>

### <span data-ttu-id="ab142-105">GetAllProducts (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ab142-105">GetAllProducts (Default)</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ab142-106">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="ab142-106">GetByProductId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab142-107">GetByTitle</span><span class="sxs-lookup"><span data-stu-id="ab142-107">GetByTitle</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab142-108">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="ab142-108">GetByApiId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab142-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="ab142-109">DESCRIPTION</span></span>
<span data-ttu-id="ab142-110">A **Get-AzApiManagementProduct** parancsmag egy listát vagy egy adott terméket kap.</span><span class="sxs-lookup"><span data-stu-id="ab142-110">The **Get-AzApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="ab142-111">Példák</span><span class="sxs-lookup"><span data-stu-id="ab142-111">EXAMPLES</span></span>

### <span data-ttu-id="ab142-112">Példa 1: a termékek beszerzése</span><span class="sxs-lookup"><span data-stu-id="ab142-112">Example 1: Get all products</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext
```

<span data-ttu-id="ab142-113">Ez a parancs minden API-kezelési terméket beolvassa.</span><span class="sxs-lookup"><span data-stu-id="ab142-113">This command get all API Management products.</span></span>

### <span data-ttu-id="ab142-114">2. példa: a termékek beszerzése AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="ab142-114">Example 2: Get a product by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="ab142-115">Ez a parancs egy API-kezelési terméket AZONOSÍTÓval kap.</span><span class="sxs-lookup"><span data-stu-id="ab142-115">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="ab142-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ab142-116">PARAMETERS</span></span>

### <span data-ttu-id="ab142-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="ab142-117">-ApiId</span></span>
<span data-ttu-id="ab142-118">ApiId az API-t a korrelált termékek megtalálásához.</span><span class="sxs-lookup"><span data-stu-id="ab142-118">ApiId of the Api to find the correlated products.</span></span> <span data-ttu-id="ab142-119">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="ab142-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="ab142-120">-Környezet</span><span class="sxs-lookup"><span data-stu-id="ab142-120">-Context</span></span>
<span data-ttu-id="ab142-121">Egy **PsApiManagementContext** -objektum példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ab142-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ab142-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab142-122">-DefaultProfile</span></span>
<span data-ttu-id="ab142-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ab142-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab142-124">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="ab142-124">-ProductId</span></span>
<span data-ttu-id="ab142-125">A keresett terméktípus azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ab142-125">Specifies the identifier of the product to search for.</span></span>

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

### <span data-ttu-id="ab142-126">-Cím</span><span class="sxs-lookup"><span data-stu-id="ab142-126">-Title</span></span>
<span data-ttu-id="ab142-127">Annak a termékeknek a címét adja meg, amelyet keresni szeretne.</span><span class="sxs-lookup"><span data-stu-id="ab142-127">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="ab142-128">Ha meg van adva, a parancsmag megpróbálja a terméket cím szerint beszerezni.</span><span class="sxs-lookup"><span data-stu-id="ab142-128">If specified, the cmdlet attempts to get the product by title.</span></span>

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

### <span data-ttu-id="ab142-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab142-129">CommonParameters</span></span>
<span data-ttu-id="ab142-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ab142-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab142-131">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ab142-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab142-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab142-132">INPUTS</span></span>

### <span data-ttu-id="ab142-133">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ab142-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ab142-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ab142-134">System.String</span></span>

## <span data-ttu-id="ab142-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab142-135">OUTPUTS</span></span>

### <span data-ttu-id="ab142-136">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="ab142-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="ab142-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ab142-137">NOTES</span></span>

## <span data-ttu-id="ab142-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ab142-138">RELATED LINKS</span></span>

[<span data-ttu-id="ab142-139">Új – AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="ab142-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="ab142-140">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="ab142-140">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="ab142-141">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="ab142-141">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


