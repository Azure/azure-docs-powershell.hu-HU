---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
ms.openlocfilehash: 3d9a462a034c5c1e65ff6b22fe92b14421582392
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401266"
---
# <span data-ttu-id="e6c2a-101">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="e6c2a-101">New-AzApiManagementBackendCredential</span></span>

## <span data-ttu-id="e6c2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6c2a-102">SYNOPSIS</span></span>
<span data-ttu-id="e6c2a-103">Létrehoz egy új backend hitelesítőadat-szerződést.</span><span class="sxs-lookup"><span data-stu-id="e6c2a-103">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="e6c2a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e6c2a-104">SYNTAX</span></span>

```
New-AzApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6c2a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e6c2a-105">DESCRIPTION</span></span>
<span data-ttu-id="e6c2a-106">Létrehoz egy új backend hitelesítőadat-szerződést.</span><span class="sxs-lookup"><span data-stu-id="e6c2a-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="e6c2a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e6c2a-107">EXAMPLES</span></span>

### <span data-ttu-id="e6c2a-108">Backend Credentials In-Memory objektum</span><span class="sxs-lookup"><span data-stu-id="e6c2a-108">Create a Backend Credentials In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="e6c2a-109">Háttéradat-hitelesítő adatokra vonatkozó szerződést hoz létre</span><span class="sxs-lookup"><span data-stu-id="e6c2a-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="e6c2a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6c2a-110">PARAMETERS</span></span>

### <span data-ttu-id="e6c2a-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="e6c2a-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="e6c2a-112">A Backendhez használt engedélyezési fejléc.</span><span class="sxs-lookup"><span data-stu-id="e6c2a-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="e6c2a-113">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="e6c2a-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="e6c2a-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="e6c2a-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="e6c2a-115">A Backendhez használt engedélyezési séma.</span><span class="sxs-lookup"><span data-stu-id="e6c2a-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="e6c2a-116">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="e6c2a-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="e6c2a-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="e6c2a-117">-CertificateThumbprint</span></span>
<span data-ttu-id="e6c2a-118">Ügyfél tanúsítványának thumbprints.</span><span class="sxs-lookup"><span data-stu-id="e6c2a-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="e6c2a-119">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="e6c2a-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="e6c2a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6c2a-120">-DefaultProfile</span></span>
<span data-ttu-id="e6c2a-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e6c2a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6c2a-122">-Header</span><span class="sxs-lookup"><span data-stu-id="e6c2a-122">-Header</span></span>
<span data-ttu-id="e6c2a-123">A Backend által elfogadott fejlécparaméter-értékek.</span><span class="sxs-lookup"><span data-stu-id="e6c2a-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="e6c2a-124">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="e6c2a-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="e6c2a-125">-Query</span><span class="sxs-lookup"><span data-stu-id="e6c2a-125">-Query</span></span>
<span data-ttu-id="e6c2a-126">A Backend által elfogadott lekérdezési paraméterértékek.</span><span class="sxs-lookup"><span data-stu-id="e6c2a-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="e6c2a-127">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="e6c2a-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="e6c2a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6c2a-128">CommonParameters</span></span>
<span data-ttu-id="e6c2a-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6c2a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6c2a-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6c2a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6c2a-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e6c2a-131">INPUTS</span></span>

### <span data-ttu-id="e6c2a-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="e6c2a-132">None</span></span>

## <span data-ttu-id="e6c2a-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6c2a-133">OUTPUTS</span></span>

### <span data-ttu-id="e6c2a-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="e6c2a-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="e6c2a-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e6c2a-135">NOTES</span></span>

## <span data-ttu-id="e6c2a-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e6c2a-136">RELATED LINKS</span></span>

[<span data-ttu-id="e6c2a-137">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e6c2a-137">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="e6c2a-138">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e6c2a-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="e6c2a-139">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="e6c2a-139">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="e6c2a-140">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e6c2a-140">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="e6c2a-141">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e6c2a-141">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
