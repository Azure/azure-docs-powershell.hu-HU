---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendproxy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
ms.openlocfilehash: d7757e277c6465622279937f72c45a1bec07684a
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398155"
---
# <span data-ttu-id="b0e25-101">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="b0e25-101">New-AzApiManagementBackendProxy</span></span>

## <span data-ttu-id="b0e25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0e25-102">SYNOPSIS</span></span>
<span data-ttu-id="b0e25-103">Létrehoz egy új backend proxyobjektumot.</span><span class="sxs-lookup"><span data-stu-id="b0e25-103">Creates a new Backend Proxy Object.</span></span>

## <span data-ttu-id="b0e25-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b0e25-104">SYNTAX</span></span>

```
New-AzApiManagementBackendProxy -Url <String> [-ProxyCredential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0e25-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b0e25-105">DESCRIPTION</span></span>
<span data-ttu-id="b0e25-106">Létrehoz egy új backend proxyobjektumot, amely egy új backend entitás létrehozásakor be lehet ásni.</span><span class="sxs-lookup"><span data-stu-id="b0e25-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="b0e25-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b0e25-107">EXAMPLES</span></span>

### <span data-ttu-id="b0e25-108">Backend Proxy In-Memory objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="b0e25-108">Create a Backend Proxy In-Memory Object</span></span>
```powershell
PS C:\>$secpassword = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\>$proxyCreds = New-Object System.Management.Automation.PSCredential ("foo", $secpassword)
PS C:\>$credential = New-AzApiManagementBackendProxy -Url "http://12.168.1.1:8080" -ProxyCredential $proxyCreds

PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Proxy $credential -Description "backend with proxy server"
```

<span data-ttu-id="b0e25-109">Backend proxyobjektum létrehozása és a Backend beállítása</span><span class="sxs-lookup"><span data-stu-id="b0e25-109">Creates a Backend Proxy Object and sets up Backend</span></span>

## <span data-ttu-id="b0e25-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0e25-110">PARAMETERS</span></span>

### <span data-ttu-id="b0e25-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0e25-111">-DefaultProfile</span></span>
<span data-ttu-id="b0e25-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b0e25-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0e25-113">-ProxyCredential</span><span class="sxs-lookup"><span data-stu-id="b0e25-113">-ProxyCredential</span></span>
<span data-ttu-id="b0e25-114">A backend proxyhoz való csatlakozáshoz használt hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="b0e25-114">Credentials used to connect to Backend Proxy.</span></span> <span data-ttu-id="b0e25-115">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="b0e25-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="b0e25-116">-Url</span><span class="sxs-lookup"><span data-stu-id="b0e25-116">-Url</span></span>
<span data-ttu-id="b0e25-117">A hívások backendbe való továbbító proxykiszolgálójának URL-címe.</span><span class="sxs-lookup"><span data-stu-id="b0e25-117">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="b0e25-118">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="b0e25-118">This parameter is required.</span></span>

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

### <span data-ttu-id="b0e25-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0e25-119">CommonParameters</span></span>
<span data-ttu-id="b0e25-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0e25-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0e25-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0e25-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0e25-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b0e25-122">INPUTS</span></span>

### <span data-ttu-id="b0e25-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="b0e25-123">None</span></span>

## <span data-ttu-id="b0e25-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0e25-124">OUTPUTS</span></span>

### <span data-ttu-id="b0e25-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="b0e25-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="b0e25-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b0e25-126">NOTES</span></span>

## <span data-ttu-id="b0e25-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b0e25-127">RELATED LINKS</span></span>

[<span data-ttu-id="b0e25-128">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b0e25-128">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="b0e25-129">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b0e25-129">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="b0e25-130">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="b0e25-130">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="b0e25-131">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b0e25-131">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="b0e25-132">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b0e25-132">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
