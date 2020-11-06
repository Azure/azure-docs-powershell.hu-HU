---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackendproxy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
ms.openlocfilehash: 890f169c3fd497f7045522133e1e9e1f1d509aca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504635"
---
# <span data-ttu-id="34925-101">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="34925-101">New-AzureRmApiManagementBackendProxy</span></span>

## <span data-ttu-id="34925-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="34925-102">SYNOPSIS</span></span>
<span data-ttu-id="34925-103">Új backend-proxy objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="34925-103">Creates a new Backend Proxy Object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34925-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="34925-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendProxy -Url <String> [-ProxyCredential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34925-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="34925-105">DESCRIPTION</span></span>
<span data-ttu-id="34925-106">Új backend-proxy objektumot hoz létre, melyet egy új backend-entitás létrehozásakor lehet átirányítani.</span><span class="sxs-lookup"><span data-stu-id="34925-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="34925-107">Példák</span><span class="sxs-lookup"><span data-stu-id="34925-107">EXAMPLES</span></span>

### <span data-ttu-id="34925-108">Backend-proxy In-Memory objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="34925-108">Create a Backend Proxy In-Memory Object</span></span>
```
PS C:\>$secpassword = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\>$proxyCreds = New-Object System.Management.Automation.PSCredential ("foo", $secpassword)
PS C:\>$credential = New-AzureRmApiManagementBackendProxy -Url "http://12.168.1.1:8080" -ProxyCredential $proxyCreds
```

<span data-ttu-id="34925-109">Backend-proxy objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="34925-109">Creates a Backend Proxy Object</span></span>

## <span data-ttu-id="34925-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="34925-110">PARAMETERS</span></span>

### <span data-ttu-id="34925-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34925-111">-DefaultProfile</span></span>
<span data-ttu-id="34925-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="34925-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34925-113">-ProxyCredential</span><span class="sxs-lookup"><span data-stu-id="34925-113">-ProxyCredential</span></span>
<span data-ttu-id="34925-114">A backend-proxyhoz való csatlakozáshoz használt hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="34925-114">Credentials used to connect to Backend Proxy.</span></span> <span data-ttu-id="34925-115">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="34925-115">This parameter is optional.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34925-116">-URL</span><span class="sxs-lookup"><span data-stu-id="34925-116">-Url</span></span>
<span data-ttu-id="34925-117">A hívásoknak a backend-be való továbbításakor használandó proxykiszolgáló URL-címe.</span><span class="sxs-lookup"><span data-stu-id="34925-117">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="34925-118">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="34925-118">This parameter is required.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34925-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34925-119">CommonParameters</span></span>
<span data-ttu-id="34925-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="34925-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34925-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34925-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34925-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="34925-122">INPUTS</span></span>

### <span data-ttu-id="34925-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="34925-123">None</span></span>
<span data-ttu-id="34925-124">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="34925-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="34925-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="34925-125">OUTPUTS</span></span>

### <span data-ttu-id="34925-126">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="34925-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="34925-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="34925-127">NOTES</span></span>

## <span data-ttu-id="34925-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="34925-128">RELATED LINKS</span></span>

[<span data-ttu-id="34925-129">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="34925-129">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="34925-130">Új – AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="34925-130">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="34925-131">Új – AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="34925-131">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="34925-132">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="34925-132">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="34925-133">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="34925-133">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
