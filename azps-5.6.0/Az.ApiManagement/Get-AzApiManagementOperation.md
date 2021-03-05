---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
ms.openlocfilehash: 5807925c302f951f9e48c89afcb62634bd774c89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014357"
---
# <span data-ttu-id="d9f3f-101">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d9f3f-101">Get-AzApiManagementOperation</span></span>

## <span data-ttu-id="d9f3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9f3f-102">SYNOPSIS</span></span>
<span data-ttu-id="d9f3f-103">Listát vagy adott API-műveletet kap.</span><span class="sxs-lookup"><span data-stu-id="d9f3f-103">Gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="d9f3f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d9f3f-104">SYNTAX</span></span>

### <span data-ttu-id="d9f3f-105">GetAllApiOperations (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d9f3f-105">GetAllApiOperations (Default)</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9f3f-106">GetById</span><span class="sxs-lookup"><span data-stu-id="d9f3f-106">GetById</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9f3f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d9f3f-107">DESCRIPTION</span></span>
<span data-ttu-id="d9f3f-108">A **Get-AzApiManagementOperation** kap egy listát vagy egy megadott API-műveletet.</span><span class="sxs-lookup"><span data-stu-id="d9f3f-108">The **Get-AzApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="d9f3f-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d9f3f-109">EXAMPLES</span></span>

### <span data-ttu-id="d9f3f-110">1. példa: Az összes API-kezelési művelet levezetése</span><span class="sxs-lookup"><span data-stu-id="d9f3f-110">Example 1: Get all API management operations</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId
```

<span data-ttu-id="d9f3f-111">Ez a parancs az összes API-kezelési műveletet beveszi.</span><span class="sxs-lookup"><span data-stu-id="d9f3f-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="d9f3f-112">2. példa: API-kezelési művelet levezetése műveletazonosító alapján</span><span class="sxs-lookup"><span data-stu-id="d9f3f-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="d9f3f-113">Ez a parancs egy Művelet0003 nevű műveletazonosítójú API-kezelési műveletet kap.</span><span class="sxs-lookup"><span data-stu-id="d9f3f-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="d9f3f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9f3f-114">PARAMETERS</span></span>

### <span data-ttu-id="d9f3f-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d9f3f-115">-ApiId</span></span>
<span data-ttu-id="d9f3f-116">Az API-művelet azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9f3f-116">Specifies the identifier of the API Operation.</span></span>

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

### <span data-ttu-id="d9f3f-117">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="d9f3f-117">-ApiRevision</span></span>
<span data-ttu-id="d9f3f-118">Az API-változat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d9f3f-118">Identifier of API Revision.</span></span> <span data-ttu-id="d9f3f-119">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="d9f3f-119">This parameter is optional.</span></span> <span data-ttu-id="d9f3f-120">Ha nincs megadva, a művelet beolvasható az aktuálisan aktív API-változatból.</span><span class="sxs-lookup"><span data-stu-id="d9f3f-120">If not specified, the operation will be retrieved from the currently active api revision.</span></span>

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

### <span data-ttu-id="d9f3f-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="d9f3f-121">-Context</span></span>
<span data-ttu-id="d9f3f-122">A **PsApiManagementContext** objektum példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9f3f-122">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d9f3f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9f3f-123">-DefaultProfile</span></span>
<span data-ttu-id="d9f3f-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d9f3f-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9f3f-125">-OperationId</span><span class="sxs-lookup"><span data-stu-id="d9f3f-125">-OperationId</span></span>
<span data-ttu-id="d9f3f-126">Megadja a művelet azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="d9f3f-126">Specifies the operation identifier.</span></span>

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

### <span data-ttu-id="d9f3f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9f3f-127">CommonParameters</span></span>
<span data-ttu-id="d9f3f-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9f3f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9f3f-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d9f3f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9f3f-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d9f3f-130">INPUTS</span></span>

### <span data-ttu-id="d9f3f-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d9f3f-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d9f3f-132">System.String</span><span class="sxs-lookup"><span data-stu-id="d9f3f-132">System.String</span></span>

## <span data-ttu-id="d9f3f-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9f3f-133">OUTPUTS</span></span>

### <span data-ttu-id="d9f3f-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d9f3f-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="d9f3f-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d9f3f-135">NOTES</span></span>

## <span data-ttu-id="d9f3f-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d9f3f-136">RELATED LINKS</span></span>

[<span data-ttu-id="d9f3f-137">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d9f3f-137">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="d9f3f-138">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d9f3f-138">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)

[<span data-ttu-id="d9f3f-139">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d9f3f-139">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


