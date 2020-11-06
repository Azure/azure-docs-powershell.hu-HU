---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
ms.openlocfilehash: b2c623d46dcc2d84e2c90ae5f3d94cfb54f7224a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498111"
---
# <span data-ttu-id="be9e3-101">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="be9e3-101">Get-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="be9e3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="be9e3-102">SYNOPSIS</span></span>
<span data-ttu-id="be9e3-103">Megadhat egy listát vagy egy megadott API-műveletet.</span><span class="sxs-lookup"><span data-stu-id="be9e3-103">Gets a list or a specified API Operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be9e3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="be9e3-104">SYNTAX</span></span>

### <span data-ttu-id="be9e3-105">Minden API-művelet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="be9e3-105">All API Operations (Default)</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be9e3-106">Keresés azonosító szerint</span><span class="sxs-lookup"><span data-stu-id="be9e3-106">Find by ID</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be9e3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="be9e3-107">DESCRIPTION</span></span>
<span data-ttu-id="be9e3-108">A **Get-AzureRmApiManagementOperation** egy listát vagy egy megadott API-műveletet kap.</span><span class="sxs-lookup"><span data-stu-id="be9e3-108">The **Get-AzureRmApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="be9e3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="be9e3-109">EXAMPLES</span></span>

### <span data-ttu-id="be9e3-110">Példa 1: az API-kezelési műveletek beolvasása</span><span class="sxs-lookup"><span data-stu-id="be9e3-110">Example 1: Get all API management operations</span></span>
```
PS C:\>Get-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIId
```

<span data-ttu-id="be9e3-111">Ez a parancs minden API-kezelési műveletet beolvas.</span><span class="sxs-lookup"><span data-stu-id="be9e3-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="be9e3-112">2. példa: API-kezelési művelet beszerzése műveleti AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="be9e3-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>Get-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="be9e3-113">Ez a parancs az API-kezelési műveletet a Operation0003 nevű műveleti AZONOSÍTÓval kapja meg.</span><span class="sxs-lookup"><span data-stu-id="be9e3-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="be9e3-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="be9e3-114">PARAMETERS</span></span>

### <span data-ttu-id="be9e3-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="be9e3-115">-ApiId</span></span>
<span data-ttu-id="be9e3-116">Az API-művelet azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="be9e3-116">Specifies the identifier of the API Operation.</span></span>

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

### <span data-ttu-id="be9e3-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="be9e3-117">-Context</span></span>
<span data-ttu-id="be9e3-118">A **PsApiManagementContext** objektum példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="be9e3-118">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="be9e3-119">-OperationId</span><span class="sxs-lookup"><span data-stu-id="be9e3-119">-OperationId</span></span>
<span data-ttu-id="be9e3-120">A műveleti azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="be9e3-120">Specifies the operation identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be9e3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be9e3-121">-DefaultProfile</span></span>
<span data-ttu-id="be9e3-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="be9e3-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be9e3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be9e3-123">CommonParameters</span></span>
<span data-ttu-id="be9e3-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="be9e3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be9e3-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be9e3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be9e3-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="be9e3-126">INPUTS</span></span>

## <span data-ttu-id="be9e3-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="be9e3-127">OUTPUTS</span></span>

### <span data-ttu-id="be9e3-128">IList<Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementOperation></span><span class="sxs-lookup"><span data-stu-id="be9e3-128">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation></span></span>

## <span data-ttu-id="be9e3-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="be9e3-129">NOTES</span></span>

## <span data-ttu-id="be9e3-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="be9e3-130">RELATED LINKS</span></span>

[<span data-ttu-id="be9e3-131">Új – AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="be9e3-131">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="be9e3-132">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="be9e3-132">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)

[<span data-ttu-id="be9e3-133">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="be9e3-133">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


