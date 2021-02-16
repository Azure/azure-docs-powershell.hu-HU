---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendproxy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
ms.openlocfilehash: fe4d94bb438d3180ed0a77bb7129b46c65d5edbc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205686"
---
# <span data-ttu-id="e7c5d-101">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="e7c5d-101">New-AzApiManagementBackendProxy</span></span>

## <span data-ttu-id="e7c5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7c5d-102">SYNOPSIS</span></span>
<span data-ttu-id="e7c5d-103">Létrehoz egy új backend proxyobjektumot.</span><span class="sxs-lookup"><span data-stu-id="e7c5d-103">Creates a new Backend Proxy Object.</span></span>

## <span data-ttu-id="e7c5d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e7c5d-104">SYNTAX</span></span>

```
New-AzApiManagementBackendProxy -Url <String> [-ProxyCredential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7c5d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e7c5d-105">DESCRIPTION</span></span>
<span data-ttu-id="e7c5d-106">Létrehoz egy új backend proxyobjektumot, amely be lehet ásni egy új backend entitás létrehozásakor.</span><span class="sxs-lookup"><span data-stu-id="e7c5d-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="e7c5d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e7c5d-107">EXAMPLES</span></span>

### <span data-ttu-id="e7c5d-108">1. példa: Backend Proxy In-Memory objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="e7c5d-108">Example 1: Create a Backend Proxy In-Memory Object</span></span>
```powershell
PS C:\>$secpassword = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\>$proxyCreds = New-Object System.Management.Automation.PSCredential ("foo", $secpassword)
PS C:\>$credential = New-AzApiManagementBackendProxy -Url "http://12.168.1.1:8080" -ProxyCredential $proxyCreds

PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Proxy $credential -Description "backend with proxy server"
```

<span data-ttu-id="e7c5d-109">Backend proxyobjektum létrehozása és a Backend beállítása</span><span class="sxs-lookup"><span data-stu-id="e7c5d-109">Creates a Backend Proxy Object and sets up Backend</span></span>

## <span data-ttu-id="e7c5d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7c5d-110">PARAMETERS</span></span>

### <span data-ttu-id="e7c5d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7c5d-111">-DefaultProfile</span></span>
<span data-ttu-id="e7c5d-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e7c5d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7c5d-113">-ProxyCredential</span><span class="sxs-lookup"><span data-stu-id="e7c5d-113">-ProxyCredential</span></span>
<span data-ttu-id="e7c5d-114">A backend proxyhoz való csatlakozáshoz használt hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="e7c5d-114">Credentials used to connect to Backend Proxy.</span></span> <span data-ttu-id="e7c5d-115">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="e7c5d-115">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7c5d-116">-Url</span><span class="sxs-lookup"><span data-stu-id="e7c5d-116">-Url</span></span>
<span data-ttu-id="e7c5d-117">A hívások backendbe való továbbító proxykiszolgálójának URL-címe.</span><span class="sxs-lookup"><span data-stu-id="e7c5d-117">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="e7c5d-118">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="e7c5d-118">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7c5d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7c5d-119">CommonParameters</span></span>
<span data-ttu-id="e7c5d-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7c5d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7c5d-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7c5d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7c5d-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e7c5d-122">INPUTS</span></span>

### <span data-ttu-id="e7c5d-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="e7c5d-123">None</span></span>

## <span data-ttu-id="e7c5d-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7c5d-124">OUTPUTS</span></span>

### <span data-ttu-id="e7c5d-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="e7c5d-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="e7c5d-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e7c5d-126">NOTES</span></span>

## <span data-ttu-id="e7c5d-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e7c5d-127">RELATED LINKS</span></span>

[<span data-ttu-id="e7c5d-128">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e7c5d-128">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="e7c5d-129">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e7c5d-129">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="e7c5d-130">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="e7c5d-130">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="e7c5d-131">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e7c5d-131">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="e7c5d-132">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e7c5d-132">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
