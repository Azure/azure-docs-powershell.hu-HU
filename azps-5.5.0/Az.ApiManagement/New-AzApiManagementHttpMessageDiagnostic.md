---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementhttpmessagediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
ms.openlocfilehash: 10c84654bb5d074ee9f668062d1fa7a18d92f8b0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168539"
---
# <span data-ttu-id="7b9a1-101">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="7b9a1-101">New-AzApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="7b9a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b9a1-102">SYNOPSIS</span></span>
<span data-ttu-id="7b9a1-103">A **PsApiManagementHttpMessageDiagnostic** példányának létrehozása, amely a diagnosztikai eszköz http-üzenet diagnosztikai beállítása</span><span class="sxs-lookup"><span data-stu-id="7b9a1-103">Creates an instance of **PsApiManagementHttpMessageDiagnostic** which is an Http Message diagnostic setting of the Diagnostic</span></span>

## <span data-ttu-id="7b9a1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7b9a1-104">SYNTAX</span></span>

```
New-AzApiManagementHttpMessageDiagnostic [-HeadersToLog <String[]>] [-BodyBytesToLog <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b9a1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7b9a1-105">DESCRIPTION</span></span>
<span data-ttu-id="7b9a1-106">A **New-AzApiManagementHttpMessageDiagnostic** parancsmag létrehozza a http-üzenet diagnosztikai beállítását.</span><span class="sxs-lookup"><span data-stu-id="7b9a1-106">The cmdlet **New-AzApiManagementHttpMessageDiagnostic** creates the Http Message diagnostic setting.</span></span>

## <span data-ttu-id="7b9a1-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7b9a1-107">EXAMPLES</span></span>

### <span data-ttu-id="7b9a1-108">1. példa: Egyszerű http-üzenet diagnosztikai beállításának létrehozása</span><span class="sxs-lookup"><span data-stu-id="7b9a1-108">Example 1: Create a Basic Http Message diagnostic Setting</span></span>
```powershell
PS C:\>  New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100

Headers                   Body
-------                   ----
{Content-Type, UserAgent} Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBodyDiagnosticSetting
```

<span data-ttu-id="7b9a1-109">Http-üzenet diagnosztikai beállításának létrehozása a naplóhoz és a fejléchez `Content-Type` `User-Agent` 100 bájt `body`</span><span class="sxs-lookup"><span data-stu-id="7b9a1-109">Create a http message diagnostic setting to log `Content-Type` and `User-Agent` headers along with 100 bytes of `body`</span></span>

## <span data-ttu-id="7b9a1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b9a1-110">PARAMETERS</span></span>

### <span data-ttu-id="7b9a1-111">-BodyBytesToLog</span><span class="sxs-lookup"><span data-stu-id="7b9a1-111">-BodyBytesToLog</span></span>
<span data-ttu-id="7b9a1-112">A naplózni kért bájtok száma.</span><span class="sxs-lookup"><span data-stu-id="7b9a1-112">Number of request body bytes to log.</span></span> <span data-ttu-id="7b9a1-113">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="7b9a1-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="7b9a1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b9a1-114">-DefaultProfile</span></span>
<span data-ttu-id="7b9a1-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7b9a1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b9a1-116">-HeadersToLog</span><span class="sxs-lookup"><span data-stu-id="7b9a1-116">-HeadersToLog</span></span>
<span data-ttu-id="7b9a1-117">A naplózandó fejlécek tömbje.</span><span class="sxs-lookup"><span data-stu-id="7b9a1-117">The array of headers to log.</span></span> <span data-ttu-id="7b9a1-118">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="7b9a1-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="7b9a1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b9a1-119">CommonParameters</span></span>
<span data-ttu-id="7b9a1-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b9a1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b9a1-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7b9a1-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b9a1-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7b9a1-122">INPUTS</span></span>

### <span data-ttu-id="7b9a1-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="7b9a1-123">None</span></span>

## <span data-ttu-id="7b9a1-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7b9a1-124">OUTPUTS</span></span>

### <span data-ttu-id="7b9a1-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="7b9a1-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="7b9a1-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7b9a1-126">NOTES</span></span>

## <span data-ttu-id="7b9a1-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7b9a1-127">RELATED LINKS</span></span>

[<span data-ttu-id="7b9a1-128">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="7b9a1-128">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="7b9a1-129">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="7b9a1-129">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)