---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
ms.openlocfilehash: 9b2eb9f45f04b858e0773215ee1ed9fd98f20ff5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665674"
---
# <span data-ttu-id="5d2cb-101">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="5d2cb-101">Get-AzApiManagementProduct</span></span>

## <span data-ttu-id="5d2cb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5d2cb-102">SYNOPSIS</span></span>
<span data-ttu-id="5d2cb-103">Egy lista vagy egy adott terméket kap.</span><span class="sxs-lookup"><span data-stu-id="5d2cb-103">Gets a list or a particular product.</span></span>

## <span data-ttu-id="5d2cb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5d2cb-104">SYNTAX</span></span>

### <span data-ttu-id="5d2cb-105">GetAllProducts (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5d2cb-105">GetAllProducts (Default)</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5d2cb-106">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="5d2cb-106">GetByProductId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d2cb-107">GetByTitle</span><span class="sxs-lookup"><span data-stu-id="5d2cb-107">GetByTitle</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d2cb-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5d2cb-108">DESCRIPTION</span></span>
<span data-ttu-id="5d2cb-109">A **Get-AzApiManagementProduct** parancsmag egy listát vagy egy adott terméket kap.</span><span class="sxs-lookup"><span data-stu-id="5d2cb-109">The **Get-AzApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="5d2cb-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5d2cb-110">EXAMPLES</span></span>

### <span data-ttu-id="5d2cb-111">Példa 1: a termékek beszerzése</span><span class="sxs-lookup"><span data-stu-id="5d2cb-111">Example 1: Get all products</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext
```

<span data-ttu-id="5d2cb-112">Ez a parancs minden API-kezelési terméket beolvassa.</span><span class="sxs-lookup"><span data-stu-id="5d2cb-112">This command get all API Management products.</span></span>

### <span data-ttu-id="5d2cb-113">2. példa: a termékek beszerzése AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="5d2cb-113">Example 2: Get a product by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="5d2cb-114">Ez a parancs egy API-kezelési terméket AZONOSÍTÓval kap.</span><span class="sxs-lookup"><span data-stu-id="5d2cb-114">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="5d2cb-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5d2cb-115">PARAMETERS</span></span>

### <span data-ttu-id="5d2cb-116">-Környezet</span><span class="sxs-lookup"><span data-stu-id="5d2cb-116">-Context</span></span>
<span data-ttu-id="5d2cb-117">Egy **PsApiManagementContext** -objektum példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5d2cb-117">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="5d2cb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d2cb-118">-DefaultProfile</span></span>
<span data-ttu-id="5d2cb-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5d2cb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d2cb-120">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="5d2cb-120">-ProductId</span></span>
<span data-ttu-id="5d2cb-121">A keresett terméktípus azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5d2cb-121">Specifies the identifier of the product to search for.</span></span>

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

### <span data-ttu-id="5d2cb-122">-Cím</span><span class="sxs-lookup"><span data-stu-id="5d2cb-122">-Title</span></span>
<span data-ttu-id="5d2cb-123">Annak a termékeknek a címét adja meg, amelyet keresni szeretne.</span><span class="sxs-lookup"><span data-stu-id="5d2cb-123">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="5d2cb-124">Ha meg van adva, a parancsmag megpróbálja a terméket cím szerint beszerezni.</span><span class="sxs-lookup"><span data-stu-id="5d2cb-124">If specified, the cmdlet attempts to get the product by title.</span></span>

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

### <span data-ttu-id="5d2cb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d2cb-125">CommonParameters</span></span>
<span data-ttu-id="5d2cb-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5d2cb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d2cb-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d2cb-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d2cb-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d2cb-128">INPUTS</span></span>

### <span data-ttu-id="5d2cb-129">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5d2cb-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5d2cb-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5d2cb-130">System.String</span></span>

## <span data-ttu-id="5d2cb-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d2cb-131">OUTPUTS</span></span>

### <span data-ttu-id="5d2cb-132">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="5d2cb-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="5d2cb-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5d2cb-133">NOTES</span></span>

## <span data-ttu-id="5d2cb-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5d2cb-134">RELATED LINKS</span></span>

[<span data-ttu-id="5d2cb-135">Új – AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="5d2cb-135">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="5d2cb-136">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="5d2cb-136">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="5d2cb-137">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="5d2cb-137">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


