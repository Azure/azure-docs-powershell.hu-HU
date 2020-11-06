---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
ms.openlocfilehash: d3699347d21f17452d521afb3bc5524f8e68e40b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498060"
---
# <span data-ttu-id="60952-101">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="60952-101">New-AzureRmApiManagementBackendProxy</span></span>

## <span data-ttu-id="60952-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="60952-102">SYNOPSIS</span></span>
<span data-ttu-id="60952-103">Új backend-proxy objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="60952-103">Creates a new Backend Proxy Object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60952-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="60952-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendProxy -Url <String> [-UserName <String>] [-Password <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60952-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="60952-105">DESCRIPTION</span></span>
<span data-ttu-id="60952-106">Új backend-proxy objektumot hoz létre, melyet egy új backend-entitás létrehozásakor lehet átirányítani.</span><span class="sxs-lookup"><span data-stu-id="60952-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="60952-107">Példák</span><span class="sxs-lookup"><span data-stu-id="60952-107">EXAMPLES</span></span>

### <span data-ttu-id="60952-108">Backend-proxy In-Memory objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="60952-108">Create a Backend Proxy In-Memory Object</span></span>
```
$proxy= New-AzureRmApiManagementBackendProxy -Url "https://abbc.def.g" -UserName "apim" -Password "password"
```

<span data-ttu-id="60952-109">Backend-proxy objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="60952-109">Creates a Backend Proxy Object</span></span>

## <span data-ttu-id="60952-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="60952-110">PARAMETERS</span></span>

### <span data-ttu-id="60952-111">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="60952-111">-Password</span></span>
<span data-ttu-id="60952-112">A backend-proxyhoz való csatlakozáshoz használt proxy-jelszó.</span><span class="sxs-lookup"><span data-stu-id="60952-112">Proxy Password used to connect to Backend Proxy.</span></span>
<span data-ttu-id="60952-113">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="60952-113">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60952-114">-URL</span><span class="sxs-lookup"><span data-stu-id="60952-114">-Url</span></span>
<span data-ttu-id="60952-115">A hívásoknak a backend-be való továbbításakor használandó proxykiszolgáló URL-címe.</span><span class="sxs-lookup"><span data-stu-id="60952-115">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="60952-116">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="60952-116">This parameter is required.</span></span>

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

### <span data-ttu-id="60952-117">-Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="60952-117">-UserName</span></span>
<span data-ttu-id="60952-118">A backend-proxyhoz való csatlakozáshoz használt proxy-Felhasználónév.</span><span class="sxs-lookup"><span data-stu-id="60952-118">Proxy UserName used to connect to Backend Proxy.</span></span>
<span data-ttu-id="60952-119">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="60952-119">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60952-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60952-120">-DefaultProfile</span></span>
<span data-ttu-id="60952-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="60952-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60952-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60952-122">CommonParameters</span></span>
<span data-ttu-id="60952-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="60952-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60952-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60952-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60952-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="60952-125">INPUTS</span></span>

## <span data-ttu-id="60952-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="60952-126">OUTPUTS</span></span>

### <span data-ttu-id="60952-127">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="60952-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="60952-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="60952-128">NOTES</span></span>

## <span data-ttu-id="60952-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="60952-129">RELATED LINKS</span></span>

[<span data-ttu-id="60952-130">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="60952-130">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="60952-131">Új – AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="60952-131">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="60952-132">Új – AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="60952-132">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="60952-133">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="60952-133">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="60952-134">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="60952-134">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
