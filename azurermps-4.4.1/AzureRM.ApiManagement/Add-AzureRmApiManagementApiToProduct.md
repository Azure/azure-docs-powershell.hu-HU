---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 7C86B385-D784-45FD-9B57-31C895115A2C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementApiToProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementApiToProduct.md
ms.openlocfilehash: d5c9061921f6ab345a027eeec69b4d6cd7230211
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679125"
---
# <span data-ttu-id="0dab7-101">Add-AzureRmApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="0dab7-101">Add-AzureRmApiManagementApiToProduct</span></span>

## <span data-ttu-id="0dab7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0dab7-102">SYNOPSIS</span></span>
<span data-ttu-id="0dab7-103">API-t ad hozzá a termékekhez.</span><span class="sxs-lookup"><span data-stu-id="0dab7-103">Adds an API to a product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0dab7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0dab7-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementApiToProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0dab7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0dab7-105">DESCRIPTION</span></span>
<span data-ttu-id="0dab7-106">Az **Add-AzureRmApiManagementApiToProduct** parancsmag egy Azure API-kezelési API-t ad hozzá egy termékekhez.</span><span class="sxs-lookup"><span data-stu-id="0dab7-106">The **Add-AzureRmApiManagementApiToProduct** cmdlet adds an Azure API Management API to a product.</span></span>

## <span data-ttu-id="0dab7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0dab7-107">EXAMPLES</span></span>

### <span data-ttu-id="0dab7-108">1. példa: API hozzáadása a termékekhez</span><span class="sxs-lookup"><span data-stu-id="0dab7-108">Example 1: Add an API to a product</span></span>
```
PS C:\>Add-AzureRmApiManagementApiToProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001"
```

<span data-ttu-id="0dab7-109">Ez a parancs hozzáadja a megadott API-t a megadott termékekhez.</span><span class="sxs-lookup"><span data-stu-id="0dab7-109">This command adds the specified API to the specified product.</span></span>

## <span data-ttu-id="0dab7-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0dab7-110">PARAMETERS</span></span>

### <span data-ttu-id="0dab7-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="0dab7-111">-ApiId</span></span>
<span data-ttu-id="0dab7-112">A termékekhez hozzáadni kívánt API AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0dab7-112">Specifies the ID of an API to add to a product.</span></span>

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

### <span data-ttu-id="0dab7-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="0dab7-113">-Context</span></span>
<span data-ttu-id="0dab7-114">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="0dab7-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0dab7-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0dab7-115">-PassThru</span></span>
<span data-ttu-id="0dab7-116">passthru</span><span class="sxs-lookup"><span data-stu-id="0dab7-116">passthru</span></span>

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

### <span data-ttu-id="0dab7-117">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="0dab7-117">-ProductId</span></span>
<span data-ttu-id="0dab7-118">Annak a termékeknek az AZONOSÍTÓját adja meg, amelyhez hozzá szeretné adni az API-t.</span><span class="sxs-lookup"><span data-stu-id="0dab7-118">Specifies the ID of the product to which to add the API.</span></span>

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

### <span data-ttu-id="0dab7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dab7-119">-DefaultProfile</span></span>
<span data-ttu-id="0dab7-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0dab7-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0dab7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dab7-121">CommonParameters</span></span>
<span data-ttu-id="0dab7-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0dab7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dab7-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dab7-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dab7-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0dab7-124">INPUTS</span></span>

## <span data-ttu-id="0dab7-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0dab7-125">OUTPUTS</span></span>

### <span data-ttu-id="0dab7-126">Logikai</span><span class="sxs-lookup"><span data-stu-id="0dab7-126">Boolean</span></span>

## <span data-ttu-id="0dab7-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0dab7-127">NOTES</span></span>

## <span data-ttu-id="0dab7-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0dab7-128">RELATED LINKS</span></span>

[<span data-ttu-id="0dab7-129">Remove-AzureRmApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="0dab7-129">Remove-AzureRmApiManagementApiFromProduct</span></span>](./Remove-AzureRmApiManagementApiFromProduct.md)


