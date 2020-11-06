---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
ms.openlocfilehash: 469d10303f286a0feca162e628a1564826b850d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492094"
---
# <span data-ttu-id="d1913-101">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d1913-101">Get-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="d1913-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d1913-102">SYNOPSIS</span></span>
<span data-ttu-id="d1913-103">Megadhat egy listát vagy egy megadott API-műveletet.</span><span class="sxs-lookup"><span data-stu-id="d1913-103">Gets a list or a specified API Operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1913-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d1913-104">SYNTAX</span></span>

### <span data-ttu-id="d1913-105">GetAllApiOperations (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d1913-105">GetAllApiOperations (Default)</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1913-106">GetById</span><span class="sxs-lookup"><span data-stu-id="d1913-106">GetById</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1913-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d1913-107">DESCRIPTION</span></span>
<span data-ttu-id="d1913-108">A **Get-AzureRmApiManagementOperation** egy listát vagy egy megadott API-műveletet kap.</span><span class="sxs-lookup"><span data-stu-id="d1913-108">The **Get-AzureRmApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="d1913-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d1913-109">EXAMPLES</span></span>

### <span data-ttu-id="d1913-110">Példa 1: az API-kezelési műveletek beolvasása</span><span class="sxs-lookup"><span data-stu-id="d1913-110">Example 1: Get all API management operations</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId
```

<span data-ttu-id="d1913-111">Ez a parancs minden API-kezelési műveletet beolvas.</span><span class="sxs-lookup"><span data-stu-id="d1913-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="d1913-112">2. példa: API-kezelési művelet beszerzése műveleti AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="d1913-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="d1913-113">Ez a parancs az API-kezelési műveletet a Operation0003 nevű műveleti AZONOSÍTÓval kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d1913-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="d1913-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d1913-114">PARAMETERS</span></span>

### <span data-ttu-id="d1913-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d1913-115">-ApiId</span></span>
<span data-ttu-id="d1913-116">Az API-művelet azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1913-116">Specifies the identifier of the API Operation.</span></span>

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

### <span data-ttu-id="d1913-117">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="d1913-117">-ApiRevision</span></span>
<span data-ttu-id="d1913-118">Az API-módosítás azonosítója</span><span class="sxs-lookup"><span data-stu-id="d1913-118">Identifier of API Revision.</span></span> <span data-ttu-id="d1913-119">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="d1913-119">This parameter is optional.</span></span> <span data-ttu-id="d1913-120">Ha nem adja meg, a művelet a jelenleg aktív API-verzióból lesz beolvasva.</span><span class="sxs-lookup"><span data-stu-id="d1913-120">If not specified, the operation will be retrieved from the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1913-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="d1913-121">-Context</span></span>
<span data-ttu-id="d1913-122">A **PsApiManagementContext** objektum példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1913-122">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d1913-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1913-123">-DefaultProfile</span></span>
<span data-ttu-id="d1913-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d1913-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1913-125">-OperationId</span><span class="sxs-lookup"><span data-stu-id="d1913-125">-OperationId</span></span>
<span data-ttu-id="d1913-126">A műveleti azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1913-126">Specifies the operation identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1913-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1913-127">CommonParameters</span></span>
<span data-ttu-id="d1913-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d1913-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1913-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1913-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1913-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1913-130">INPUTS</span></span>

### <span data-ttu-id="d1913-131">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d1913-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d1913-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d1913-132">System.String</span></span>

## <span data-ttu-id="d1913-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1913-133">OUTPUTS</span></span>

### <span data-ttu-id="d1913-134">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d1913-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="d1913-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d1913-135">NOTES</span></span>

## <span data-ttu-id="d1913-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d1913-136">RELATED LINKS</span></span>

[<span data-ttu-id="d1913-137">Új – AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d1913-137">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="d1913-138">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d1913-138">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)

[<span data-ttu-id="d1913-139">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d1913-139">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


