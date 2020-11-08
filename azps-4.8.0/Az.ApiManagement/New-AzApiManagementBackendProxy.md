---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendproxy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
ms.openlocfilehash: fe4d94bb438d3180ed0a77bb7129b46c65d5edbc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024948"
---
# <span data-ttu-id="a088c-101">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="a088c-101">New-AzApiManagementBackendProxy</span></span>

## <span data-ttu-id="a088c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a088c-102">SYNOPSIS</span></span>
<span data-ttu-id="a088c-103">Új backend-proxy objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="a088c-103">Creates a new Backend Proxy Object.</span></span>

## <span data-ttu-id="a088c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a088c-104">SYNTAX</span></span>

```
New-AzApiManagementBackendProxy -Url <String> [-ProxyCredential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a088c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a088c-105">DESCRIPTION</span></span>
<span data-ttu-id="a088c-106">Új backend-proxy objektumot hoz létre, melyet egy új backend-entitás létrehozásakor lehet átirányítani.</span><span class="sxs-lookup"><span data-stu-id="a088c-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="a088c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a088c-107">EXAMPLES</span></span>

### <span data-ttu-id="a088c-108">Példa 1: backend proxy In-Memory objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="a088c-108">Example 1: Create a Backend Proxy In-Memory Object</span></span>
```powershell
PS C:\>$secpassword = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\>$proxyCreds = New-Object System.Management.Automation.PSCredential ("foo", $secpassword)
PS C:\>$credential = New-AzApiManagementBackendProxy -Url "http://12.168.1.1:8080" -ProxyCredential $proxyCreds

PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Proxy $credential -Description "backend with proxy server"
```

<span data-ttu-id="a088c-109">Backend-proxy objektum létrehozása és a backend beállítása</span><span class="sxs-lookup"><span data-stu-id="a088c-109">Creates a Backend Proxy Object and sets up Backend</span></span>

## <span data-ttu-id="a088c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a088c-110">PARAMETERS</span></span>

### <span data-ttu-id="a088c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a088c-111">-DefaultProfile</span></span>
<span data-ttu-id="a088c-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a088c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a088c-113">-ProxyCredential</span><span class="sxs-lookup"><span data-stu-id="a088c-113">-ProxyCredential</span></span>
<span data-ttu-id="a088c-114">A backend-proxyhoz való csatlakozáshoz használt hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="a088c-114">Credentials used to connect to Backend Proxy.</span></span> <span data-ttu-id="a088c-115">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="a088c-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="a088c-116">-URL</span><span class="sxs-lookup"><span data-stu-id="a088c-116">-Url</span></span>
<span data-ttu-id="a088c-117">A hívásoknak a backend-be való továbbításakor használandó proxykiszolgáló URL-címe.</span><span class="sxs-lookup"><span data-stu-id="a088c-117">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="a088c-118">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="a088c-118">This parameter is required.</span></span>

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

### <span data-ttu-id="a088c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a088c-119">CommonParameters</span></span>
<span data-ttu-id="a088c-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a088c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a088c-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a088c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a088c-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a088c-122">INPUTS</span></span>

### <span data-ttu-id="a088c-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="a088c-123">None</span></span>

## <span data-ttu-id="a088c-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a088c-124">OUTPUTS</span></span>

### <span data-ttu-id="a088c-125">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="a088c-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="a088c-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a088c-126">NOTES</span></span>

## <span data-ttu-id="a088c-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a088c-127">RELATED LINKS</span></span>

[<span data-ttu-id="a088c-128">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a088c-128">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="a088c-129">Új – AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a088c-129">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="a088c-130">Új – AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="a088c-130">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="a088c-131">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a088c-131">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="a088c-132">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a088c-132">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
