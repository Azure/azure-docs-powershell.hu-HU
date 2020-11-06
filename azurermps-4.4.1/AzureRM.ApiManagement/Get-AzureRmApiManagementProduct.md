---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
ms.openlocfilehash: ab0aeb77bd5f28520e39548f539d07516cd17ac8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498099"
---
# <span data-ttu-id="23773-101">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="23773-101">Get-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="23773-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="23773-102">SYNOPSIS</span></span>
<span data-ttu-id="23773-103">Egy lista vagy egy adott terméket kap.</span><span class="sxs-lookup"><span data-stu-id="23773-103">Gets a list or a particular product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23773-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="23773-104">SYNTAX</span></span>

### <span data-ttu-id="23773-105">Az összes producst beszerzése (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="23773-105">Get all producst (Default)</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="23773-106">Beolvasás azonosítóval</span><span class="sxs-lookup"><span data-stu-id="23773-106">Get by Id</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23773-107">A cím beszerzése</span><span class="sxs-lookup"><span data-stu-id="23773-107">Get by Title</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23773-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="23773-108">DESCRIPTION</span></span>
<span data-ttu-id="23773-109">A **Get-AzureRmApiManagementProduct** parancsmag egy listát vagy egy adott terméket kap.</span><span class="sxs-lookup"><span data-stu-id="23773-109">The **Get-AzureRmApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="23773-110">Példák</span><span class="sxs-lookup"><span data-stu-id="23773-110">EXAMPLES</span></span>

### <span data-ttu-id="23773-111">Példa 1: a termékek beszerzése</span><span class="sxs-lookup"><span data-stu-id="23773-111">Example 1: Get all products</span></span>
```
PS C:\>Get-AzureRmApiManagementProduct -Context $APImContext
```

<span data-ttu-id="23773-112">Ez a parancs minden API-kezelési terméket beolvassa.</span><span class="sxs-lookup"><span data-stu-id="23773-112">This command get all API Management products.</span></span>

### <span data-ttu-id="23773-113">2. példa: a termékek beszerzése AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="23773-113">Example 2: Get a product by ID</span></span>
```
PS C:\>Get-AzureRmApiManagementProduct -Context $APImContext -ProductId "0123456789"
```

<span data-ttu-id="23773-114">Ez a parancs egy API-kezelési terméket AZONOSÍTÓval kap.</span><span class="sxs-lookup"><span data-stu-id="23773-114">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="23773-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="23773-115">PARAMETERS</span></span>

### <span data-ttu-id="23773-116">-Környezet</span><span class="sxs-lookup"><span data-stu-id="23773-116">-Context</span></span>
<span data-ttu-id="23773-117">Egy **PsApiManagementContext** -objektum példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="23773-117">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="23773-118">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="23773-118">-ProductId</span></span>
<span data-ttu-id="23773-119">A keresett terméktípus azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="23773-119">Specifies the identifier of the product to search for.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by Id
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23773-120">-Cím</span><span class="sxs-lookup"><span data-stu-id="23773-120">-Title</span></span>
<span data-ttu-id="23773-121">Annak a termékeknek a címét adja meg, amelyet keresni szeretne.</span><span class="sxs-lookup"><span data-stu-id="23773-121">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="23773-122">Ha meg van adva, a parancsmag megpróbálja a terméket cím szerint beszerezni.</span><span class="sxs-lookup"><span data-stu-id="23773-122">If specified, the cmdlet attempts to get the product by title.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by Title
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23773-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23773-123">-DefaultProfile</span></span>
<span data-ttu-id="23773-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="23773-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23773-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23773-125">CommonParameters</span></span>
<span data-ttu-id="23773-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="23773-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23773-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23773-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23773-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="23773-128">INPUTS</span></span>

## <span data-ttu-id="23773-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="23773-129">OUTPUTS</span></span>

### <span data-ttu-id="23773-130">IList<Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementProduct></span><span class="sxs-lookup"><span data-stu-id="23773-130">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct></span></span>

## <span data-ttu-id="23773-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="23773-131">NOTES</span></span>

## <span data-ttu-id="23773-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="23773-132">RELATED LINKS</span></span>

[<span data-ttu-id="23773-133">Új – AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="23773-133">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="23773-134">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="23773-134">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)

[<span data-ttu-id="23773-135">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="23773-135">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


