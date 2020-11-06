---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
ms.openlocfilehash: 10b17f60ae100004c23a16f341924de6de11b0eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492092"
---
# <span data-ttu-id="27137-101">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="27137-101">Get-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="27137-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="27137-102">SYNOPSIS</span></span>
<span data-ttu-id="27137-103">Egy lista vagy egy adott terméket kap.</span><span class="sxs-lookup"><span data-stu-id="27137-103">Gets a list or a particular product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27137-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="27137-104">SYNTAX</span></span>

### <span data-ttu-id="27137-105">GetAllProducts (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="27137-105">GetAllProducts (Default)</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="27137-106">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="27137-106">GetByProductId</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27137-107">GetByTitle</span><span class="sxs-lookup"><span data-stu-id="27137-107">GetByTitle</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27137-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="27137-108">DESCRIPTION</span></span>
<span data-ttu-id="27137-109">A **Get-AzureRmApiManagementProduct** parancsmag egy listát vagy egy adott terméket kap.</span><span class="sxs-lookup"><span data-stu-id="27137-109">The **Get-AzureRmApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="27137-110">Példák</span><span class="sxs-lookup"><span data-stu-id="27137-110">EXAMPLES</span></span>

### <span data-ttu-id="27137-111">Példa 1: a termékek beszerzése</span><span class="sxs-lookup"><span data-stu-id="27137-111">Example 1: Get all products</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProduct -Context $apimContext
```

<span data-ttu-id="27137-112">Ez a parancs minden API-kezelési terméket beolvassa.</span><span class="sxs-lookup"><span data-stu-id="27137-112">This command get all API Management products.</span></span>

### <span data-ttu-id="27137-113">2. példa: a termékek beszerzése AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="27137-113">Example 2: Get a product by ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProduct -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="27137-114">Ez a parancs egy API-kezelési terméket AZONOSÍTÓval kap.</span><span class="sxs-lookup"><span data-stu-id="27137-114">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="27137-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="27137-115">PARAMETERS</span></span>

### <span data-ttu-id="27137-116">-Környezet</span><span class="sxs-lookup"><span data-stu-id="27137-116">-Context</span></span>
<span data-ttu-id="27137-117">Egy **PsApiManagementContext** -objektum példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="27137-117">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="27137-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27137-118">-DefaultProfile</span></span>
<span data-ttu-id="27137-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="27137-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27137-120">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="27137-120">-ProductId</span></span>
<span data-ttu-id="27137-121">A keresett terméktípus azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="27137-121">Specifies the identifier of the product to search for.</span></span>

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

### <span data-ttu-id="27137-122">-Cím</span><span class="sxs-lookup"><span data-stu-id="27137-122">-Title</span></span>
<span data-ttu-id="27137-123">Annak a termékeknek a címét adja meg, amelyet keresni szeretne.</span><span class="sxs-lookup"><span data-stu-id="27137-123">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="27137-124">Ha meg van adva, a parancsmag megpróbálja a terméket cím szerint beszerezni.</span><span class="sxs-lookup"><span data-stu-id="27137-124">If specified, the cmdlet attempts to get the product by title.</span></span>

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

### <span data-ttu-id="27137-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27137-125">CommonParameters</span></span>
<span data-ttu-id="27137-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="27137-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27137-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27137-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27137-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="27137-128">INPUTS</span></span>

### <span data-ttu-id="27137-129">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="27137-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="27137-130">System. String</span><span class="sxs-lookup"><span data-stu-id="27137-130">System.String</span></span>

## <span data-ttu-id="27137-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="27137-131">OUTPUTS</span></span>

### <span data-ttu-id="27137-132">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="27137-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="27137-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="27137-133">NOTES</span></span>

## <span data-ttu-id="27137-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="27137-134">RELATED LINKS</span></span>

[<span data-ttu-id="27137-135">Új – AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="27137-135">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="27137-136">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="27137-136">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)

[<span data-ttu-id="27137-137">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="27137-137">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


