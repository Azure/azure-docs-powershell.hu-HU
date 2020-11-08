---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementhttpmessagediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
ms.openlocfilehash: 10c84654bb5d074ee9f668062d1fa7a18d92f8b0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180663"
---
# <span data-ttu-id="4c835-101">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="4c835-101">New-AzApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="4c835-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4c835-102">SYNOPSIS</span></span>
<span data-ttu-id="4c835-103">A **PsApiManagementHttpMessageDiagnostic** egy példányát hozza létre, amely a diagnosztikai rendszer http-üzenet diagnosztikai beállítása</span><span class="sxs-lookup"><span data-stu-id="4c835-103">Creates an instance of **PsApiManagementHttpMessageDiagnostic** which is an Http Message diagnostic setting of the Diagnostic</span></span>

## <span data-ttu-id="4c835-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4c835-104">SYNTAX</span></span>

```
New-AzApiManagementHttpMessageDiagnostic [-HeadersToLog <String[]>] [-BodyBytesToLog <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c835-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4c835-105">DESCRIPTION</span></span>
<span data-ttu-id="4c835-106">A **New-AzApiManagementHttpMessageDiagnostic** parancsmag a http-üzenet diagnosztikai beállítását hozza létre.</span><span class="sxs-lookup"><span data-stu-id="4c835-106">The cmdlet **New-AzApiManagementHttpMessageDiagnostic** creates the Http Message diagnostic setting.</span></span>

## <span data-ttu-id="4c835-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4c835-107">EXAMPLES</span></span>

### <span data-ttu-id="4c835-108">Példa 1: alapvető http-üzenet diagnosztikai beállításainak létrehozása</span><span class="sxs-lookup"><span data-stu-id="4c835-108">Example 1: Create a Basic Http Message diagnostic Setting</span></span>
```powershell
PS C:\>  New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100

Headers                   Body
-------                   ----
{Content-Type, UserAgent} Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBodyDiagnosticSetting
```

<span data-ttu-id="4c835-109">Http-üzenet diagnosztikai beállításának létrehozása a naplózás `Content-Type` és a `User-Agent` fejlécek 100 bájtjaival együtt `body`</span><span class="sxs-lookup"><span data-stu-id="4c835-109">Create a http message diagnostic setting to log `Content-Type` and `User-Agent` headers along with 100 bytes of `body`</span></span>

## <span data-ttu-id="4c835-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4c835-110">PARAMETERS</span></span>

### <span data-ttu-id="4c835-111">-BodyBytesToLog</span><span class="sxs-lookup"><span data-stu-id="4c835-111">-BodyBytesToLog</span></span>
<span data-ttu-id="4c835-112">A naplózni kívánt beolvasási törzs bájtjainak száma.</span><span class="sxs-lookup"><span data-stu-id="4c835-112">Number of request body bytes to log.</span></span> <span data-ttu-id="4c835-113">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="4c835-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="4c835-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c835-114">-DefaultProfile</span></span>
<span data-ttu-id="4c835-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4c835-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c835-116">-HeadersToLog</span><span class="sxs-lookup"><span data-stu-id="4c835-116">-HeadersToLog</span></span>
<span data-ttu-id="4c835-117">A naplózni kívánt fejlécek sora.</span><span class="sxs-lookup"><span data-stu-id="4c835-117">The array of headers to log.</span></span> <span data-ttu-id="4c835-118">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="4c835-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="4c835-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c835-119">CommonParameters</span></span>
<span data-ttu-id="4c835-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4c835-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c835-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4c835-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c835-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c835-122">INPUTS</span></span>

### <span data-ttu-id="4c835-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="4c835-123">None</span></span>

## <span data-ttu-id="4c835-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c835-124">OUTPUTS</span></span>

### <span data-ttu-id="4c835-125">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="4c835-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="4c835-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4c835-126">NOTES</span></span>

## <span data-ttu-id="4c835-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4c835-127">RELATED LINKS</span></span>

[<span data-ttu-id="4c835-128">Új – AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="4c835-128">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="4c835-129">Új – AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="4c835-129">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)