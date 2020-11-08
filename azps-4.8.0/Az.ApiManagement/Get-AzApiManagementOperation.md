---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
ms.openlocfilehash: 568e3562a199a3fc247de41a30a4383bdb37adac
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183401"
---
# <span data-ttu-id="41658-101">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="41658-101">Get-AzApiManagementOperation</span></span>

## <span data-ttu-id="41658-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="41658-102">SYNOPSIS</span></span>
<span data-ttu-id="41658-103">Megadhat egy listát vagy egy megadott API-műveletet.</span><span class="sxs-lookup"><span data-stu-id="41658-103">Gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="41658-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="41658-104">SYNTAX</span></span>

### <span data-ttu-id="41658-105">GetAllApiOperations (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="41658-105">GetAllApiOperations (Default)</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41658-106">GetById</span><span class="sxs-lookup"><span data-stu-id="41658-106">GetById</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41658-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="41658-107">DESCRIPTION</span></span>
<span data-ttu-id="41658-108">A **Get-AzApiManagementOperation** egy listát vagy egy megadott API-műveletet kap.</span><span class="sxs-lookup"><span data-stu-id="41658-108">The **Get-AzApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="41658-109">Példák</span><span class="sxs-lookup"><span data-stu-id="41658-109">EXAMPLES</span></span>

### <span data-ttu-id="41658-110">Példa 1: az API-kezelési műveletek beolvasása</span><span class="sxs-lookup"><span data-stu-id="41658-110">Example 1: Get all API management operations</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId
```

<span data-ttu-id="41658-111">Ez a parancs minden API-kezelési műveletet beolvas.</span><span class="sxs-lookup"><span data-stu-id="41658-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="41658-112">2. példa: API-kezelési művelet beszerzése műveleti AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="41658-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="41658-113">Ez a parancs az API-kezelési műveletet a Operation0003 nevű műveleti AZONOSÍTÓval kapja meg.</span><span class="sxs-lookup"><span data-stu-id="41658-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="41658-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="41658-114">PARAMETERS</span></span>

### <span data-ttu-id="41658-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="41658-115">-ApiId</span></span>
<span data-ttu-id="41658-116">Az API-művelet azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="41658-116">Specifies the identifier of the API Operation.</span></span>

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

### <span data-ttu-id="41658-117">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="41658-117">-ApiRevision</span></span>
<span data-ttu-id="41658-118">Az API-módosítás azonosítója</span><span class="sxs-lookup"><span data-stu-id="41658-118">Identifier of API Revision.</span></span> <span data-ttu-id="41658-119">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="41658-119">This parameter is optional.</span></span> <span data-ttu-id="41658-120">Ha nem adja meg, a művelet a jelenleg aktív API-verzióból lesz beolvasva.</span><span class="sxs-lookup"><span data-stu-id="41658-120">If not specified, the operation will be retrieved from the currently active api revision.</span></span>

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

### <span data-ttu-id="41658-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="41658-121">-Context</span></span>
<span data-ttu-id="41658-122">A **PsApiManagementContext** objektum példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="41658-122">Specifies the instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41658-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41658-123">-DefaultProfile</span></span>
<span data-ttu-id="41658-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="41658-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41658-125">-OperationId</span><span class="sxs-lookup"><span data-stu-id="41658-125">-OperationId</span></span>
<span data-ttu-id="41658-126">A műveleti azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="41658-126">Specifies the operation identifier.</span></span>

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

### <span data-ttu-id="41658-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41658-127">CommonParameters</span></span>
<span data-ttu-id="41658-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="41658-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41658-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="41658-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41658-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="41658-130">INPUTS</span></span>

### <span data-ttu-id="41658-131">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="41658-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="41658-132">System. String</span><span class="sxs-lookup"><span data-stu-id="41658-132">System.String</span></span>

## <span data-ttu-id="41658-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="41658-133">OUTPUTS</span></span>

### <span data-ttu-id="41658-134">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="41658-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="41658-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="41658-135">NOTES</span></span>

## <span data-ttu-id="41658-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="41658-136">RELATED LINKS</span></span>

[<span data-ttu-id="41658-137">Új – AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="41658-137">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="41658-138">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="41658-138">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)

[<span data-ttu-id="41658-139">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="41658-139">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


