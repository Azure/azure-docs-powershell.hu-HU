---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementpipelinediagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
ms.openlocfilehash: 7e6f6515b24a7cefabd40a6fdfaedfda430f69d0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025831"
---
# <span data-ttu-id="6ff56-101">New-AzApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="6ff56-101">New-AzApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="6ff56-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6ff56-102">SYNOPSIS</span></span>
<span data-ttu-id="6ff56-103">Diagnosztikai beállítások létrehozása a bejövő és kimenő HTTP-üzenetekhez az átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="6ff56-103">Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="6ff56-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6ff56-104">SYNTAX</span></span>

```
New-AzApiManagementPipelineDiagnosticSetting [-Request <PsApiManagementHttpMessageDiagnostic>]
 [-Response <PsApiManagementHttpMessageDiagnostic>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6ff56-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6ff56-105">DESCRIPTION</span></span>
<span data-ttu-id="6ff56-106">A **New-AzApiManagementPipelineDiagnosticSetting** parancsmag létrehozza a bejövő/kimenő HTTP-üzenetek diagnosztikai beállításait az átjárónak.</span><span class="sxs-lookup"><span data-stu-id="6ff56-106">The cmdlet **New-AzApiManagementPipelineDiagnosticSetting** creates the Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="6ff56-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6ff56-107">EXAMPLES</span></span>

### <span data-ttu-id="6ff56-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6ff56-108">Example 1</span></span>
```powershell
PS c:\> $httpMessageDiagnostic = New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100
PS c:\> New-AzApiManagementPipelineDiagnosticSetting -Request $httpMessageDiagnostic -Response $httpMessageDiagnostic

Request                                                                                              Response
-------                                                                                              --------
Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
```

<span data-ttu-id="6ff56-109">Hozzon létre egy olyan csővezeték-diagnosztikai felületet, amelyet a diagnosztikai szervezetben a FrontEndben vagy a Backendben szeretne használni.</span><span class="sxs-lookup"><span data-stu-id="6ff56-109">Create a pipeline diagnostic to be used in either FrontEnd or Backend in the Diagnostic Entity.</span></span>

## <span data-ttu-id="6ff56-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6ff56-110">PARAMETERS</span></span>

### <span data-ttu-id="6ff56-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ff56-111">-DefaultProfile</span></span>
<span data-ttu-id="6ff56-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6ff56-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ff56-113">-Request (kérés)</span><span class="sxs-lookup"><span data-stu-id="6ff56-113">-Request</span></span>
<span data-ttu-id="6ff56-114">Diagnosztikai beállítás kéréshez.</span><span class="sxs-lookup"><span data-stu-id="6ff56-114">Diagnostic setting for Request.</span></span>
<span data-ttu-id="6ff56-115">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="6ff56-115">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ff56-116">– Válasz</span><span class="sxs-lookup"><span data-stu-id="6ff56-116">-Response</span></span>
<span data-ttu-id="6ff56-117">A válasz diagnosztikai beállításai.</span><span class="sxs-lookup"><span data-stu-id="6ff56-117">Diagnostic setting for Response.</span></span>
<span data-ttu-id="6ff56-118">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="6ff56-118">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ff56-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ff56-119">CommonParameters</span></span>
<span data-ttu-id="6ff56-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6ff56-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ff56-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6ff56-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ff56-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ff56-122">INPUTS</span></span>

### <span data-ttu-id="6ff56-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="6ff56-123">None</span></span>

## <span data-ttu-id="6ff56-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ff56-124">OUTPUTS</span></span>

### <span data-ttu-id="6ff56-125">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="6ff56-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="6ff56-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6ff56-126">NOTES</span></span>

## <span data-ttu-id="6ff56-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6ff56-127">RELATED LINKS</span></span>

[<span data-ttu-id="6ff56-128">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="6ff56-128">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="6ff56-129">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="6ff56-129">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="6ff56-130">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="6ff56-130">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="6ff56-131">Új – AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="6ff56-131">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)


