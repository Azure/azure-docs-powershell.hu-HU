---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 7C86B385-D784-45FD-9B57-31C895115A2C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementapitoproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToProduct.md
ms.openlocfilehash: 01767d80f0925647b2161dd26f504465d7f1d8e1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479053"
---
# <span data-ttu-id="0144d-101">Add-AzApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="0144d-101">Add-AzApiManagementApiToProduct</span></span>

## <span data-ttu-id="0144d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0144d-102">SYNOPSIS</span></span>
<span data-ttu-id="0144d-103">Hozzáad egy API-t egy termékhez.</span><span class="sxs-lookup"><span data-stu-id="0144d-103">Adds an API to a product.</span></span>

## <span data-ttu-id="0144d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0144d-104">SYNTAX</span></span>

```
Add-AzApiManagementApiToProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0144d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0144d-105">DESCRIPTION</span></span>
<span data-ttu-id="0144d-106">Az **Add-AzApiManagementApiToProduct** parancsmag hozzáad egy Azure API Management API-t egy termékhez.</span><span class="sxs-lookup"><span data-stu-id="0144d-106">The **Add-AzApiManagementApiToProduct** cmdlet adds an Azure API Management API to a product.</span></span>

## <span data-ttu-id="0144d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0144d-107">EXAMPLES</span></span>

### <span data-ttu-id="0144d-108">1. példa: API hozzáadása termékhez</span><span class="sxs-lookup"><span data-stu-id="0144d-108">Example 1: Add an API to a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementApiToProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001"
```

<span data-ttu-id="0144d-109">Ez a parancs hozzáadja a megadott API-t a megadott termékhez.</span><span class="sxs-lookup"><span data-stu-id="0144d-109">This command adds the specified API to the specified product.</span></span>

## <span data-ttu-id="0144d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0144d-110">PARAMETERS</span></span>

### <span data-ttu-id="0144d-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="0144d-111">-ApiId</span></span>
<span data-ttu-id="0144d-112">Egy termékhez hozzáadni fog egy API azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0144d-112">Specifies the ID of an API to add to a product.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0144d-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="0144d-113">-Context</span></span>
<span data-ttu-id="0144d-114">Egy **PsApiManagementContext objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="0144d-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0144d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0144d-115">-DefaultProfile</span></span>
<span data-ttu-id="0144d-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0144d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0144d-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0144d-117">-PassThru</span></span>
<span data-ttu-id="0144d-118">passthru</span><span class="sxs-lookup"><span data-stu-id="0144d-118">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0144d-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="0144d-119">-ProductId</span></span>
<span data-ttu-id="0144d-120">Annak a terméknek az azonosítója, amelyhez hozzá kell adni az API-t.</span><span class="sxs-lookup"><span data-stu-id="0144d-120">Specifies the ID of the product to which to add the API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0144d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0144d-121">CommonParameters</span></span>
<span data-ttu-id="0144d-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0144d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0144d-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0144d-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0144d-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0144d-124">INPUTS</span></span>

### <span data-ttu-id="0144d-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0144d-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0144d-126">System.String</span><span class="sxs-lookup"><span data-stu-id="0144d-126">System.String</span></span>

### <span data-ttu-id="0144d-127">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0144d-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0144d-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0144d-128">OUTPUTS</span></span>

### <span data-ttu-id="0144d-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0144d-129">System.Boolean</span></span>

## <span data-ttu-id="0144d-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0144d-130">NOTES</span></span>

## <span data-ttu-id="0144d-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0144d-131">RELATED LINKS</span></span>

[<span data-ttu-id="0144d-132">Remove-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="0144d-132">Remove-AzApiManagementApiFromProduct</span></span>](./Remove-AzApiManagementApiFromProduct.md)


