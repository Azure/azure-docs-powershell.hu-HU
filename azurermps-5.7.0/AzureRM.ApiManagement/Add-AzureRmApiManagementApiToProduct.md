---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 7C86B385-D784-45FD-9B57-31C895115A2C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementapitoproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementApiToProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementApiToProduct.md
ms.openlocfilehash: 08d6d8e5ecbcaa8b6810bd173062c5bb244ec5e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673066"
---
# <span data-ttu-id="6f25a-101">Add-AzureRmApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="6f25a-101">Add-AzureRmApiManagementApiToProduct</span></span>

## <span data-ttu-id="6f25a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6f25a-102">SYNOPSIS</span></span>
<span data-ttu-id="6f25a-103">API-t ad hozzá a termékekhez.</span><span class="sxs-lookup"><span data-stu-id="6f25a-103">Adds an API to a product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f25a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6f25a-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementApiToProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f25a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6f25a-105">DESCRIPTION</span></span>
<span data-ttu-id="6f25a-106">Az **Add-AzureRmApiManagementApiToProduct** parancsmag egy Azure API-kezelési API-t ad hozzá egy termékekhez.</span><span class="sxs-lookup"><span data-stu-id="6f25a-106">The **Add-AzureRmApiManagementApiToProduct** cmdlet adds an Azure API Management API to a product.</span></span>

## <span data-ttu-id="6f25a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6f25a-107">EXAMPLES</span></span>

### <span data-ttu-id="6f25a-108">1. példa: API hozzáadása a termékekhez</span><span class="sxs-lookup"><span data-stu-id="6f25a-108">Example 1: Add an API to a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzureRmApiManagementApiToProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001"
```

<span data-ttu-id="6f25a-109">Ez a parancs hozzáadja a megadott API-t a megadott termékekhez.</span><span class="sxs-lookup"><span data-stu-id="6f25a-109">This command adds the specified API to the specified product.</span></span>

## <span data-ttu-id="6f25a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6f25a-110">PARAMETERS</span></span>

### <span data-ttu-id="6f25a-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="6f25a-111">-ApiId</span></span>
<span data-ttu-id="6f25a-112">A termékekhez hozzáadni kívánt API AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6f25a-112">Specifies the ID of an API to add to a product.</span></span>

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

### <span data-ttu-id="6f25a-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="6f25a-113">-Context</span></span>
<span data-ttu-id="6f25a-114">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="6f25a-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="6f25a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f25a-115">-DefaultProfile</span></span>
<span data-ttu-id="6f25a-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6f25a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f25a-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f25a-117">-PassThru</span></span>
<span data-ttu-id="6f25a-118">passthru</span><span class="sxs-lookup"><span data-stu-id="6f25a-118">passthru</span></span>

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

### <span data-ttu-id="6f25a-119">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="6f25a-119">-ProductId</span></span>
<span data-ttu-id="6f25a-120">Annak a termékeknek az AZONOSÍTÓját adja meg, amelyhez hozzá szeretné adni az API-t.</span><span class="sxs-lookup"><span data-stu-id="6f25a-120">Specifies the ID of the product to which to add the API.</span></span>

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

### <span data-ttu-id="6f25a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f25a-121">CommonParameters</span></span>
<span data-ttu-id="6f25a-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6f25a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f25a-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f25a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f25a-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f25a-124">INPUTS</span></span>

### <span data-ttu-id="6f25a-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="6f25a-125">None</span></span>
<span data-ttu-id="6f25a-126">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="6f25a-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6f25a-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f25a-127">OUTPUTS</span></span>

### <span data-ttu-id="6f25a-128">Logikai</span><span class="sxs-lookup"><span data-stu-id="6f25a-128">Boolean</span></span>

## <span data-ttu-id="6f25a-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6f25a-129">NOTES</span></span>

## <span data-ttu-id="6f25a-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6f25a-130">RELATED LINKS</span></span>

[<span data-ttu-id="6f25a-131">Remove-AzureRmApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="6f25a-131">Remove-AzureRmApiManagementApiFromProduct</span></span>](./Remove-AzureRmApiManagementApiFromProduct.md)


