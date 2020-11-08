---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementpipelinediagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
ms.openlocfilehash: 7e6f6515b24a7cefabd40a6fdfaedfda430f69d0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012222"
---
# <span data-ttu-id="76eec-101">New-AzApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="76eec-101">New-AzApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="76eec-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="76eec-102">SYNOPSIS</span></span>
<span data-ttu-id="76eec-103">Diagnosztikai beállítások létrehozása a bejövő és kimenő HTTP-üzenetekhez az átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="76eec-103">Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="76eec-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="76eec-104">SYNTAX</span></span>

```
New-AzApiManagementPipelineDiagnosticSetting [-Request <PsApiManagementHttpMessageDiagnostic>]
 [-Response <PsApiManagementHttpMessageDiagnostic>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="76eec-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="76eec-105">DESCRIPTION</span></span>
<span data-ttu-id="76eec-106">A **New-AzApiManagementPipelineDiagnosticSetting** parancsmag létrehozza a bejövő/kimenő HTTP-üzenetek diagnosztikai beállításait az átjárónak.</span><span class="sxs-lookup"><span data-stu-id="76eec-106">The cmdlet **New-AzApiManagementPipelineDiagnosticSetting** creates the Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="76eec-107">Példák</span><span class="sxs-lookup"><span data-stu-id="76eec-107">EXAMPLES</span></span>

### <span data-ttu-id="76eec-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="76eec-108">Example 1</span></span>
```powershell
PS c:\> $httpMessageDiagnostic = New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100
PS c:\> New-AzApiManagementPipelineDiagnosticSetting -Request $httpMessageDiagnostic -Response $httpMessageDiagnostic

Request                                                                                              Response
-------                                                                                              --------
Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
```

<span data-ttu-id="76eec-109">Hozzon létre egy olyan csővezeték-diagnosztikai felületet, amelyet a diagnosztikai szervezetben a FrontEndben vagy a Backendben szeretne használni.</span><span class="sxs-lookup"><span data-stu-id="76eec-109">Create a pipeline diagnostic to be used in either FrontEnd or Backend in the Diagnostic Entity.</span></span>

## <span data-ttu-id="76eec-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="76eec-110">PARAMETERS</span></span>

### <span data-ttu-id="76eec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76eec-111">-DefaultProfile</span></span>
<span data-ttu-id="76eec-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="76eec-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76eec-113">-Request (kérés)</span><span class="sxs-lookup"><span data-stu-id="76eec-113">-Request</span></span>
<span data-ttu-id="76eec-114">Diagnosztikai beállítás kéréshez.</span><span class="sxs-lookup"><span data-stu-id="76eec-114">Diagnostic setting for Request.</span></span>
<span data-ttu-id="76eec-115">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="76eec-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="76eec-116">– Válasz</span><span class="sxs-lookup"><span data-stu-id="76eec-116">-Response</span></span>
<span data-ttu-id="76eec-117">A válasz diagnosztikai beállításai.</span><span class="sxs-lookup"><span data-stu-id="76eec-117">Diagnostic setting for Response.</span></span>
<span data-ttu-id="76eec-118">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="76eec-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="76eec-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76eec-119">CommonParameters</span></span>
<span data-ttu-id="76eec-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="76eec-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76eec-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="76eec-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76eec-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="76eec-122">INPUTS</span></span>

### <span data-ttu-id="76eec-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="76eec-123">None</span></span>

## <span data-ttu-id="76eec-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="76eec-124">OUTPUTS</span></span>

### <span data-ttu-id="76eec-125">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="76eec-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="76eec-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="76eec-126">NOTES</span></span>

## <span data-ttu-id="76eec-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="76eec-127">RELATED LINKS</span></span>

[<span data-ttu-id="76eec-128">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="76eec-128">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="76eec-129">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="76eec-129">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="76eec-130">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="76eec-130">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="76eec-131">Új – AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="76eec-131">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)


