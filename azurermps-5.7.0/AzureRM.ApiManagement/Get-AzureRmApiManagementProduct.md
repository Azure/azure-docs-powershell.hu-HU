---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
ms.openlocfilehash: a4bbc330b5cd4d7eaeec1d2e68252ceb5dd261f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495502"
---
# <span data-ttu-id="285fb-101">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="285fb-101">Get-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="285fb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="285fb-102">SYNOPSIS</span></span>
<span data-ttu-id="285fb-103">Egy lista vagy egy adott terméket kap.</span><span class="sxs-lookup"><span data-stu-id="285fb-103">Gets a list or a particular product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="285fb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="285fb-104">SYNTAX</span></span>

### <span data-ttu-id="285fb-105">GetAllProducts (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="285fb-105">GetAllProducts (Default)</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="285fb-106">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="285fb-106">GetByProductId</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="285fb-107">GetByTitle</span><span class="sxs-lookup"><span data-stu-id="285fb-107">GetByTitle</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="285fb-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="285fb-108">DESCRIPTION</span></span>
<span data-ttu-id="285fb-109">A **Get-AzureRmApiManagementProduct** parancsmag egy listát vagy egy adott terméket kap.</span><span class="sxs-lookup"><span data-stu-id="285fb-109">The **Get-AzureRmApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="285fb-110">Példák</span><span class="sxs-lookup"><span data-stu-id="285fb-110">EXAMPLES</span></span>

### <span data-ttu-id="285fb-111">Példa 1: a termékek beszerzése</span><span class="sxs-lookup"><span data-stu-id="285fb-111">Example 1: Get all products</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProduct -Context $apimContext
```

<span data-ttu-id="285fb-112">Ez a parancs minden API-kezelési terméket beolvassa.</span><span class="sxs-lookup"><span data-stu-id="285fb-112">This command get all API Management products.</span></span>

### <span data-ttu-id="285fb-113">2. példa: a termékek beszerzése AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="285fb-113">Example 2: Get a product by ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProduct -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="285fb-114">Ez a parancs egy API-kezelési terméket AZONOSÍTÓval kap.</span><span class="sxs-lookup"><span data-stu-id="285fb-114">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="285fb-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="285fb-115">PARAMETERS</span></span>

### <span data-ttu-id="285fb-116">-Környezet</span><span class="sxs-lookup"><span data-stu-id="285fb-116">-Context</span></span>
<span data-ttu-id="285fb-117">Egy **PsApiManagementContext** -objektum példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="285fb-117">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="285fb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="285fb-118">-DefaultProfile</span></span>
<span data-ttu-id="285fb-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="285fb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="285fb-120">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="285fb-120">-ProductId</span></span>
<span data-ttu-id="285fb-121">A keresett terméktípus azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="285fb-121">Specifies the identifier of the product to search for.</span></span>

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

### <span data-ttu-id="285fb-122">-Cím</span><span class="sxs-lookup"><span data-stu-id="285fb-122">-Title</span></span>
<span data-ttu-id="285fb-123">Annak a termékeknek a címét adja meg, amelyet keresni szeretne.</span><span class="sxs-lookup"><span data-stu-id="285fb-123">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="285fb-124">Ha meg van adva, a parancsmag megpróbálja a terméket cím szerint beszerezni.</span><span class="sxs-lookup"><span data-stu-id="285fb-124">If specified, the cmdlet attempts to get the product by title.</span></span>

```yaml
Type: String
Parameter Sets: GetByTitle
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="285fb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="285fb-125">CommonParameters</span></span>
<span data-ttu-id="285fb-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="285fb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="285fb-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="285fb-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="285fb-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="285fb-128">INPUTS</span></span>

### <span data-ttu-id="285fb-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="285fb-129">None</span></span>
<span data-ttu-id="285fb-130">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="285fb-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="285fb-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="285fb-131">OUTPUTS</span></span>

### <span data-ttu-id="285fb-132">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="285fb-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>
<span data-ttu-id="285fb-133">A termékek adatai az API-menedzsment szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="285fb-133">The details of the Product in API Management service.</span></span>

### <span data-ttu-id="285fb-134">IList<Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementProduct></span><span class="sxs-lookup"><span data-stu-id="285fb-134">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct></span></span>
<span data-ttu-id="285fb-135">A termékek listája az API-menedzsment szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="285fb-135">The list of Product in API Management service.</span></span>

## <span data-ttu-id="285fb-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="285fb-136">NOTES</span></span>

## <span data-ttu-id="285fb-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="285fb-137">RELATED LINKS</span></span>

[<span data-ttu-id="285fb-138">Új – AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="285fb-138">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="285fb-139">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="285fb-139">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)

[<span data-ttu-id="285fb-140">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="285fb-140">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


