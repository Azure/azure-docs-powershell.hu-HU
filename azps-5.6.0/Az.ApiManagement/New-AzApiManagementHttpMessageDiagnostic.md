---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementhttpmessagediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
ms.openlocfilehash: 3475778104655e6b27061edf08ced376f192ea34
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937185"
---
# <span data-ttu-id="82223-101">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="82223-101">New-AzApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="82223-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82223-102">SYNOPSIS</span></span>
<span data-ttu-id="82223-103">Létrehozza a **PsApiManagementHttpMessageDiagnostic** példányát, amely a diagnosztikai eszköz http-üzenet diagnosztikai beállítása.</span><span class="sxs-lookup"><span data-stu-id="82223-103">Creates an instance of **PsApiManagementHttpMessageDiagnostic** which is an Http Message diagnostic setting of the Diagnostic</span></span>

## <span data-ttu-id="82223-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="82223-104">SYNTAX</span></span>

```
New-AzApiManagementHttpMessageDiagnostic [-HeadersToLog <String[]>] [-BodyBytesToLog <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82223-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="82223-105">DESCRIPTION</span></span>
<span data-ttu-id="82223-106">A **New-AzApiManagementHttpMessageDiagnostic** parancsmag létrehozza a http-üzenet diagnosztikai beállítását.</span><span class="sxs-lookup"><span data-stu-id="82223-106">The cmdlet **New-AzApiManagementHttpMessageDiagnostic** creates the Http Message diagnostic setting.</span></span>

## <span data-ttu-id="82223-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="82223-107">EXAMPLES</span></span>

### <span data-ttu-id="82223-108">1. példa: Egyszerű http-üzenet diagnosztikai beállításának létrehozása</span><span class="sxs-lookup"><span data-stu-id="82223-108">Example 1: Create a Basic Http Message diagnostic Setting</span></span>
```powershell
PS C:\>  New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100

Headers                   Body
-------                   ----
{Content-Type, UserAgent} Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBodyDiagnosticSetting
```

<span data-ttu-id="82223-109">Http-üzenet diagnosztikai beállításának létrehozása a naplóhoz és a fejléchez `Content-Type` `User-Agent` 100 bájt `body`</span><span class="sxs-lookup"><span data-stu-id="82223-109">Create a http message diagnostic setting to log `Content-Type` and `User-Agent` headers along with 100 bytes of `body`</span></span>

## <span data-ttu-id="82223-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82223-110">PARAMETERS</span></span>

### <span data-ttu-id="82223-111">-BodyBytesToLog</span><span class="sxs-lookup"><span data-stu-id="82223-111">-BodyBytesToLog</span></span>
<span data-ttu-id="82223-112">A naplózni kért bájtok száma.</span><span class="sxs-lookup"><span data-stu-id="82223-112">Number of request body bytes to log.</span></span> <span data-ttu-id="82223-113">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="82223-113">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82223-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82223-114">-DefaultProfile</span></span>
<span data-ttu-id="82223-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="82223-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82223-116">-HeadersToLog</span><span class="sxs-lookup"><span data-stu-id="82223-116">-HeadersToLog</span></span>
<span data-ttu-id="82223-117">A naplózandó fejlécek tömbje.</span><span class="sxs-lookup"><span data-stu-id="82223-117">The array of headers to log.</span></span> <span data-ttu-id="82223-118">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="82223-118">This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82223-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82223-119">CommonParameters</span></span>
<span data-ttu-id="82223-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82223-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82223-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="82223-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82223-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="82223-122">INPUTS</span></span>

### <span data-ttu-id="82223-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="82223-123">None</span></span>

## <span data-ttu-id="82223-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="82223-124">OUTPUTS</span></span>

### <span data-ttu-id="82223-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="82223-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="82223-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="82223-126">NOTES</span></span>

## <span data-ttu-id="82223-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="82223-127">RELATED LINKS</span></span>

[<span data-ttu-id="82223-128">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="82223-128">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="82223-129">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="82223-129">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)