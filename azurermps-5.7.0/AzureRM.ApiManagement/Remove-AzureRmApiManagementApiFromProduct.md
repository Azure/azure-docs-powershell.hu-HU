---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 2457C7F5-7FB9-4712-AD7C-438E88F591A8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapifromproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiFromProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiFromProduct.md
ms.openlocfilehash: 413d03723ee2acdc162c1f1f5501d90156e16069
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504632"
---
# <span data-ttu-id="dd520-101">Remove-AzureRmApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="dd520-101">Remove-AzureRmApiManagementApiFromProduct</span></span>

## <span data-ttu-id="dd520-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dd520-102">SYNOPSIS</span></span>
<span data-ttu-id="dd520-103">Egy API eltávolítása a termékekből.</span><span class="sxs-lookup"><span data-stu-id="dd520-103">Removes an API from a product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd520-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dd520-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementApiFromProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd520-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dd520-105">DESCRIPTION</span></span>
<span data-ttu-id="dd520-106">A **Remove-AzureRmApiManagementApiFromProduct** parancsmag egy Azure API-kezelési API-t távolít el egy termékekből.</span><span class="sxs-lookup"><span data-stu-id="dd520-106">The **Remove-AzureRmApiManagementApiFromProduct** cmdlet removes an Azure API Management API from a product.</span></span>

## <span data-ttu-id="dd520-107">Példák</span><span class="sxs-lookup"><span data-stu-id="dd520-107">EXAMPLES</span></span>

### <span data-ttu-id="dd520-108">1. példa: az API eltávolítása a termékekből</span><span class="sxs-lookup"><span data-stu-id="dd520-108">Example 1: Remove an API from a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApiFromProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="dd520-109">Ez a vessző eltávolítja a megadott API-t egy terméket.</span><span class="sxs-lookup"><span data-stu-id="dd520-109">This commnd removes the specified API from a product.</span></span>

## <span data-ttu-id="dd520-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dd520-110">PARAMETERS</span></span>

### <span data-ttu-id="dd520-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="dd520-111">-ApiId</span></span>
<span data-ttu-id="dd520-112">A termékekből eltávolítandó API AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="dd520-112">Specifies the ID of the API to remove from the product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd520-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="dd520-113">-Context</span></span>
<span data-ttu-id="dd520-114">Megadja a **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="dd520-114">Specifies a **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="dd520-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd520-115">-DefaultProfile</span></span>
<span data-ttu-id="dd520-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dd520-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="dd520-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd520-117">-PassThru</span></span>
<span data-ttu-id="dd520-118">Jelzi, hogy ez a parancsmag az $True értékét adja eredményül, ha a művelet sikeres, vagy $False.</span><span class="sxs-lookup"><span data-stu-id="dd520-118">Indicates that this cmdlet returns a value of $True if it succeeds, or $False, otherwise.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd520-119">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="dd520-119">-ProductId</span></span>
<span data-ttu-id="dd520-120">Annak a termékeknek az AZONOSÍTÓját adja meg, amelyből el szeretné távolítani az API-t.</span><span class="sxs-lookup"><span data-stu-id="dd520-120">Specifies the ID of the product from which to remove the API.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd520-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd520-121">CommonParameters</span></span>
<span data-ttu-id="dd520-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dd520-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd520-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd520-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd520-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd520-124">INPUTS</span></span>

### <span data-ttu-id="dd520-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="dd520-125">None</span></span>
<span data-ttu-id="dd520-126">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="dd520-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dd520-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd520-127">OUTPUTS</span></span>

### <span data-ttu-id="dd520-128">bool</span><span class="sxs-lookup"><span data-stu-id="dd520-128">bool</span></span>

## <span data-ttu-id="dd520-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dd520-129">NOTES</span></span>

## <span data-ttu-id="dd520-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dd520-130">RELATED LINKS</span></span>

[<span data-ttu-id="dd520-131">Add-AzureRmApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="dd520-131">Add-AzureRmApiManagementApiToProduct</span></span>](./Add-AzureRmApiManagementApiToProduct.md)


