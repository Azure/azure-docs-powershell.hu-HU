---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementpipelinediagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
ms.openlocfilehash: 7e6f6515b24a7cefabd40a6fdfaedfda430f69d0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382436"
---
# <span data-ttu-id="8e686-101">New-AzApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="8e686-101">New-AzApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="8e686-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e686-102">SYNOPSIS</span></span>
<span data-ttu-id="8e686-103">Hozzon létre diagnosztikai beállításokat az átjáróba érkező és kimenő HTTP-üzenetekhez.</span><span class="sxs-lookup"><span data-stu-id="8e686-103">Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="8e686-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8e686-104">SYNTAX</span></span>

```
New-AzApiManagementPipelineDiagnosticSetting [-Request <PsApiManagementHttpMessageDiagnostic>]
 [-Response <PsApiManagementHttpMessageDiagnostic>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e686-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8e686-105">DESCRIPTION</span></span>
<span data-ttu-id="8e686-106">A **New-AzApiManagementPipelineDiagnosticSetting** parancsmag létrehozza a bejövő/kimenő HTTP-üzenetek diagnosztikai beállításait az átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="8e686-106">The cmdlet **New-AzApiManagementPipelineDiagnosticSetting** creates the Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="8e686-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8e686-107">EXAMPLES</span></span>

### <span data-ttu-id="8e686-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="8e686-108">Example 1</span></span>
```powershell
PS c:\> $httpMessageDiagnostic = New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100
PS c:\> New-AzApiManagementPipelineDiagnosticSetting -Request $httpMessageDiagnostic -Response $httpMessageDiagnostic

Request                                                                                              Response
-------                                                                                              --------
Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
```

<span data-ttu-id="8e686-109">Létrehozhat egy pipeline diagnostic to be used in the FrontEnd or Backend in the Diagnostic Entity.</span><span class="sxs-lookup"><span data-stu-id="8e686-109">Create a pipeline diagnostic to be used in either FrontEnd or Backend in the Diagnostic Entity.</span></span>

## <span data-ttu-id="8e686-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e686-110">PARAMETERS</span></span>

### <span data-ttu-id="8e686-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e686-111">-DefaultProfile</span></span>
<span data-ttu-id="8e686-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8e686-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e686-113">-Request</span><span class="sxs-lookup"><span data-stu-id="8e686-113">-Request</span></span>
<span data-ttu-id="8e686-114">A Request diagnosztikai beállítása.</span><span class="sxs-lookup"><span data-stu-id="8e686-114">Diagnostic setting for Request.</span></span>
<span data-ttu-id="8e686-115">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="8e686-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="8e686-116">-Response</span><span class="sxs-lookup"><span data-stu-id="8e686-116">-Response</span></span>
<span data-ttu-id="8e686-117">A Válasz diagnosztikai beállítása.</span><span class="sxs-lookup"><span data-stu-id="8e686-117">Diagnostic setting for Response.</span></span>
<span data-ttu-id="8e686-118">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="8e686-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="8e686-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e686-119">CommonParameters</span></span>
<span data-ttu-id="8e686-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e686-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e686-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e686-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e686-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8e686-122">INPUTS</span></span>

### <span data-ttu-id="8e686-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="8e686-123">None</span></span>

## <span data-ttu-id="8e686-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e686-124">OUTPUTS</span></span>

### <span data-ttu-id="8e686-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="8e686-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="8e686-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8e686-126">NOTES</span></span>

## <span data-ttu-id="8e686-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e686-127">RELATED LINKS</span></span>

[<span data-ttu-id="8e686-128">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8e686-128">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="8e686-129">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8e686-129">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="8e686-130">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8e686-130">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="8e686-131">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8e686-131">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)


