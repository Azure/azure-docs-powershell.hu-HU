---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
ms.openlocfilehash: d34a7666e10fe678d49194887d9b58e7c1ba0aa7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494220"
---
# <span data-ttu-id="5dd3e-101">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="5dd3e-101">New-AzureRmApiManagementBackendCredential</span></span>

## <span data-ttu-id="5dd3e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5dd3e-102">SYNOPSIS</span></span>
<span data-ttu-id="5dd3e-103">Létrehoz egy új backend hitelesítő adatokat tartalmazó szerződést.</span><span class="sxs-lookup"><span data-stu-id="5dd3e-103">Creates a new Backend Credential contract.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5dd3e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5dd3e-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5dd3e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5dd3e-105">DESCRIPTION</span></span>
<span data-ttu-id="5dd3e-106">Létrehoz egy új backend hitelesítő adatokat tartalmazó szerződést.</span><span class="sxs-lookup"><span data-stu-id="5dd3e-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="5dd3e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5dd3e-107">EXAMPLES</span></span>

### <span data-ttu-id="5dd3e-108">Backend-hitelesítő adatok In-Memory objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="5dd3e-108">Create a Backend Credentials In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="5dd3e-109">A backend-hitelesítő adatokkal rendelkező szerződés létrehozása</span><span class="sxs-lookup"><span data-stu-id="5dd3e-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="5dd3e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5dd3e-110">PARAMETERS</span></span>

### <span data-ttu-id="5dd3e-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="5dd3e-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="5dd3e-112">A backendhez használt engedélyezési fejléc.</span><span class="sxs-lookup"><span data-stu-id="5dd3e-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="5dd3e-113">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="5dd3e-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="5dd3e-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="5dd3e-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="5dd3e-115">A backendhez használt engedélyezési séma.</span><span class="sxs-lookup"><span data-stu-id="5dd3e-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="5dd3e-116">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="5dd3e-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="5dd3e-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="5dd3e-117">-CertificateThumbprint</span></span>
<span data-ttu-id="5dd3e-118">Ügyféltanúsítvány-Thumbprints</span><span class="sxs-lookup"><span data-stu-id="5dd3e-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="5dd3e-119">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="5dd3e-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="5dd3e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dd3e-120">-DefaultProfile</span></span>
<span data-ttu-id="5dd3e-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5dd3e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5dd3e-122">-Header</span><span class="sxs-lookup"><span data-stu-id="5dd3e-122">-Header</span></span>
<span data-ttu-id="5dd3e-123">A backend által elfogadott fejléc paraméter-értékek</span><span class="sxs-lookup"><span data-stu-id="5dd3e-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="5dd3e-124">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="5dd3e-124">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dd3e-125">-Query</span><span class="sxs-lookup"><span data-stu-id="5dd3e-125">-Query</span></span>
<span data-ttu-id="5dd3e-126">A lekérdezés paramétereit a backend által elfogadott értékekkel.</span><span class="sxs-lookup"><span data-stu-id="5dd3e-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="5dd3e-127">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="5dd3e-127">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dd3e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dd3e-128">CommonParameters</span></span>
<span data-ttu-id="5dd3e-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5dd3e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dd3e-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5dd3e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dd3e-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5dd3e-131">INPUTS</span></span>

### <span data-ttu-id="5dd3e-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="5dd3e-132">None</span></span>

## <span data-ttu-id="5dd3e-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5dd3e-133">OUTPUTS</span></span>

### <span data-ttu-id="5dd3e-134">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="5dd3e-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="5dd3e-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5dd3e-135">NOTES</span></span>

## <span data-ttu-id="5dd3e-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5dd3e-136">RELATED LINKS</span></span>

[<span data-ttu-id="5dd3e-137">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="5dd3e-137">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="5dd3e-138">Új – AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="5dd3e-138">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="5dd3e-139">Új – AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="5dd3e-139">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="5dd3e-140">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="5dd3e-140">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="5dd3e-141">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="5dd3e-141">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
