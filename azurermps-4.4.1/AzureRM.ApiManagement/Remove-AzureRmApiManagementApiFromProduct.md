---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 2457C7F5-7FB9-4712-AD7C-438E88F591A8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiFromProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiFromProduct.md
ms.openlocfilehash: 957a2fbecc588f9b04400571e587c6ba56e16df5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492611"
---
# <span data-ttu-id="18d37-101">Remove-AzureRmApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="18d37-101">Remove-AzureRmApiManagementApiFromProduct</span></span>

## <span data-ttu-id="18d37-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="18d37-102">SYNOPSIS</span></span>
<span data-ttu-id="18d37-103">Egy API eltávolítása a termékekből.</span><span class="sxs-lookup"><span data-stu-id="18d37-103">Removes an API from a product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18d37-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="18d37-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementApiFromProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18d37-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="18d37-105">DESCRIPTION</span></span>
<span data-ttu-id="18d37-106">A **Remove-AzureRmApiManagementApiFromProduct** parancsmag egy Azure API-kezelési API-t távolít el egy termékekből.</span><span class="sxs-lookup"><span data-stu-id="18d37-106">The **Remove-AzureRmApiManagementApiFromProduct** cmdlet removes an Azure API Management API from a product.</span></span>

## <span data-ttu-id="18d37-107">Példák</span><span class="sxs-lookup"><span data-stu-id="18d37-107">EXAMPLES</span></span>

### <span data-ttu-id="18d37-108">1. példa: az API eltávolítása a termékekből</span><span class="sxs-lookup"><span data-stu-id="18d37-108">Example 1: Remove an API from a product</span></span>
```
PS C:\>Remove-AzureRmApiManagementApiFromProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="18d37-109">Ez a vessző eltávolítja a megadott API-t egy terméket.</span><span class="sxs-lookup"><span data-stu-id="18d37-109">This commnd removes the specified API from a product.</span></span>

## <span data-ttu-id="18d37-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="18d37-110">PARAMETERS</span></span>

### <span data-ttu-id="18d37-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="18d37-111">-ApiId</span></span>
<span data-ttu-id="18d37-112">A termékekből eltávolítandó API AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="18d37-112">Specifies the ID of the API to remove from the product.</span></span>

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

### <span data-ttu-id="18d37-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="18d37-113">-Context</span></span>
<span data-ttu-id="18d37-114">Megadja a **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="18d37-114">Specifies a **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="18d37-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="18d37-115">-PassThru</span></span>
<span data-ttu-id="18d37-116">Jelzi, hogy ez a parancsmag az $True értékét adja eredményül, ha a művelet sikeres, vagy $False.</span><span class="sxs-lookup"><span data-stu-id="18d37-116">Indicates that this cmdlet returns a value of $True if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="18d37-117">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="18d37-117">-ProductId</span></span>
<span data-ttu-id="18d37-118">Annak a termékeknek az AZONOSÍTÓját adja meg, amelyből el szeretné távolítani az API-t.</span><span class="sxs-lookup"><span data-stu-id="18d37-118">Specifies the ID of the product from which to remove the API.</span></span>

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

### <span data-ttu-id="18d37-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18d37-119">-DefaultProfile</span></span>
<span data-ttu-id="18d37-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="18d37-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18d37-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18d37-121">CommonParameters</span></span>
<span data-ttu-id="18d37-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="18d37-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18d37-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18d37-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18d37-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="18d37-124">INPUTS</span></span>

## <span data-ttu-id="18d37-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="18d37-125">OUTPUTS</span></span>

### <span data-ttu-id="18d37-126">bool</span><span class="sxs-lookup"><span data-stu-id="18d37-126">bool</span></span>

## <span data-ttu-id="18d37-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="18d37-127">NOTES</span></span>

## <span data-ttu-id="18d37-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="18d37-128">RELATED LINKS</span></span>

[<span data-ttu-id="18d37-129">Add-AzureRmApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="18d37-129">Add-AzureRmApiManagementApiToProduct</span></span>](./Add-AzureRmApiManagementApiToProduct.md)


